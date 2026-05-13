# Cursor agent tool mapping

Skills often reference Claude Code tool names. In Cursor Cloud and Cursor agent sessions, use the equivalents below when a skill names a Claude Code tool.

| Skill references | Cursor agent equivalent |
|------------------|-------------------------|
| `Read` (file reading) | `Read` |
| `Write` (file creation) | `Write` |
| `Edit` / search-replace | `StrReplace` (or `Write` for new files) |
| `Bash` (run commands) | `Shell` |
| `Grep` | `Grep` |
| `Glob` | `Glob` |
| `Skill` tool (invoke a skill) | Read the skill’s `SKILL.md` from the path listed in `AGENTS.md` or the workspace skill list, then follow it |
| `TodoWrite` | `TodoWrite` |
| `Task` (subagent) | `Task` |
| `WebSearch` | `WebSearch` |
| `WebFetch` | `WebFetch` |

When `AGENTS.md` points at `skills/<name>/SKILL.md`, loading that file is the correct way to “invoke” the skill in this repository.
