---
name: clarify
description: Identify and improve unclear interface text (errors, labels, buttons, help text, empty states, confirmations) so products are easier to understand and use. Use when UX copy is vague, jargon-heavy, passive, or missing context; pairs with project-local impeccable and polish skills.
license: Apache-2.0. See LICENSE.txt; upstream attribution in NOTICE.md.
---

# Clarify (UX copy)

This skill is the **clarify** workflow from the [skills.sh catalog](https://skills.sh/pbakaus/impeccable/clarify) (sourced from [pbakaus/impeccable](https://github.com/pbakaus/impeccable), installable with `npx skills add https://github.com/pbakaus/impeccable --skill clarify`).

## Mandatory preparation

Before rewriting interface copy:

1. **Load design law context**: Read `skills/impeccable/SKILL.md` (shared design laws, absolute bans, context gathering). For wording that must align with visual and accessibility expectations, also read `skills/frontend-design/SKILL.md` and `skills/web-design-guidelines/SKILL.md`.
2. **Gather audience and state**: Confirm technical level of the audience and the user’s mental state in the situation (errors, payments, destructive actions, onboarding).
3. **Optional harness**: If the repo has `PRODUCT.md` / `DESIGN.md`, run `node skills/impeccable/scripts/load-context.mjs` when you need full impeccable voice and constraints.

If no product or audience foundation exists yet, run the **teach** flow described in `skills/impeccable/SKILL.md` (or capture equivalent notes) before large copy rewrites.

## Procedure

Follow **`reference/clarify.md`** end to end. It covers assessing unclear copy, planning improvements, systematic rewrites across common UI surfaces, clarity principles, verification, and handoff to **polish**.

## Supporting references

- `reference/clarify.md` — main workflow (vendored from upstream `skill/reference/clarify.md`, adapted for project-local polish paths)
