---
name: lark-openapi-explorer
version: 1.0.0
description: "Feishu/Lark native OpenAPI exploration: excavate undocumented native OpenAPI endpoints from the official markdown documentation library when existing lark-* skills or registered lark-cli commands cannot satisfy the request."
metadata:
  requires:
    bins: ["lark-cli"]
---

# OpenAPI Explorer

> **Prerequisite:** Read [`../lark-shared/SKILL.md`](../lark-shared/SKILL.md) first for authentication, identity switching (`--as user/bot`), and safety rules.

Use this skill when the user's need **cannot be covered by an existing skill or a registered CLI API**. Excavate native OpenAPI endpoints layer by layer from Feishu/Lark's official markdown documentation library, then complete the task via raw `lark-cli api` calls.

## Documentation library structure

Feishu OpenAPI docs are organized as markdown hierarchies:

```text
llms.txt                          ← top-level index listing module doc links
  └─ llms-<module>.txt            ← module overview + links to individual API docs
       └─ <api-doc>.md            ← full API spec (method/path/params/response/errors)
```

Documentation entry points:

| Brand | Entry URL |
|-------|-----------|
| Feishu | `https://open.feishu.cn/llms.txt` |
| Lark | `https://open.larksuite.com/llms.txt` |

> All documentation is written in **Chinese**. If the user communicates in English, translate doc content to English in your output.

## Excavation workflow

Follow these steps strictly, layer by layer. **Do not skip steps or guess APIs.**

### Step 1: Confirm existing capabilities are insufficient

```bash
# Check whether a skill or registered API already covers the need
lark-cli <likely-service> --help
```

If a command or shortcut already exists, use it directly — **do not continue excavating**.

### Step 2: Locate the module from the top-level index

Use WebFetch on the top-level index and find module doc links related to the request:

```text
WebFetch https://open.feishu.cn/llms.txt
  → extraction prompt: "List all module doc links and find those related to <user need keywords>"
```

- Feishu brand: `open.feishu.cn`
- Lark brand: `open.larksuite.com`
- If the brand is unclear, default to Feishu

### Step 3: Locate the specific API from module docs

Use WebFetch on the module doc and find links to individual API specifications:

```text
WebFetch https://open.feishu.cn/llms-docs/zh-CN/llms-<module>.txt
  → extraction prompt: "Find API descriptions and doc links related to <user need>"
```

### Step 4: Fetch the full API specification

Use WebFetch on the specific API doc and extract the complete calling contract:

```text
WebFetch https://open.feishu.cn/document/server-docs/.../<api>.md
  → extraction prompt: "Return the full API spec: HTTP method, URL path, path params, query params, request body fields (name/type/required/description), response fields, required scopes, error codes"
```

### Step 5: Call the API via CLI

Use `lark-cli api` for raw calls:

```bash
# GET
lark-cli api GET /open-apis/<path> --params '{"key":"value"}'

# POST
lark-cli api POST /open-apis/<path> --data '{"key":"value"}'

# PUT
lark-cli api PUT /open-apis/<path> --data '{"key":"value"}'

# DELETE
lark-cli api DELETE /open-apis/<path>
```

## Output format

When presenting excavation results to the user, organize as:

1. **API name and purpose** — one-sentence description
2. **HTTP method and path** — `METHOD /open-apis/...`
3. **Key parameters** — required and commonly used optional params
4. **Required scopes** — scope list
5. **Call example** — complete `lark-cli api` command
6. **Notes** — rate limits, special constraints, etc.

If the user communicates in English, translate all of the above to English.

## Safety rules

- **Write/delete APIs** (POST/PUT/DELETE/PATCH): confirm user intent before calling
- Prefer `--dry-run` to preview requests when supported
- Never guess API paths or parameters — they must come from documentation
- For sensitive operations (delete group, remove members, etc.), explain impact scope to the user

## Example scenarios

### Scenario 1: Add members to a chat (not wrapped by CLI)

```bash
# Step 1: Confirm CLI has no wrapper
lark-cli im --help
# → no chat_members create command

# Steps 2-4: Excavate from docs
# → POST /open-apis/im/v1/chats/:chat_id/members

# Step 5: Call
lark-cli api POST /open-apis/im/v1/chats/oc_xxx/members \
  --data '{"id_list":["ou_xxx","ou_yyy"]}' \
  --params '{"member_id_type":"open_id"}'
```

### Scenario 2: Set a group announcement

```bash
# Step 1: Confirm CLI has no wrapper
lark-cli im --help
# → no announcement command

# Steps 2-4: Excavate from docs
# → PATCH /open-apis/im/v1/chats/:chat_id/announcement

# Step 5: Call
lark-cli api PATCH /open-apis/im/v1/chats/oc_xxx/announcement \
  --data '{"revision":"0","requests":["<html>announcement content</html>"]}'
```

## References

- [`lark-shared`](../lark-shared/SKILL.md) — authentication and global parameters
- [`lark-skill-maker`](../lark-skill-maker/SKILL.md) — wrap excavated APIs into a new skill
