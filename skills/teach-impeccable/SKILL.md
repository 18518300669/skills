---
name: teach-impeccable
description: One-time design context setup for impeccable-style UI work. Scans the codebase, interviews on users/brand/register/accessibility, and writes PRODUCT.md (and optionally DESIGN.md) at the project root. Use when the user mentions teach-impeccable, impeccable teach, design context setup, PRODUCT.md, DESIGN.md, .impeccable.md, or needs persistent design context before polish/craft/onboard flows.
license: Apache-2.0. See LICENSE.txt; upstream attribution in NOTICE.md.
user-invocable: true
argument-hint: "[project or surface]"
---

# Teach impeccable (design context setup)

This skill is the **teach-impeccable** workflow from the [skills.sh leaderboard #369](https://skills.sh/pbakaus/impeccable/teach-impeccable) (sourced from [pbakaus/impeccable](https://github.com/pbakaus/impeccable); catalog install: `npx skills add https://github.com/pbakaus/impeccable --skill teach-impeccable`). Upstream has renamed the CLI entry to **`impeccable teach`**; follow this skill's procedure either way.

It gathers strategic and visual design context once, then persists it for later impeccable sub-skills (`polish`, `onboard`, `craft`, etc.).

## Distinctions

- **`skills/teach/SKILL.md`** (mattpocock) — multi-session **learning workspace** with lessons and `MISSION.md`; not design-context setup.
- **`skills/impeccable/SKILL.md`** — full impeccable harness; its `teach` subcommand uses the same procedure as this skill.

## Mandatory preparation

Before teaching:

1. Confirm whether `PRODUCT.md` and/or `DESIGN.md` already exist at the project root (or legacy `.impeccable.md` pending migration).
2. Read project-local design guidance when available:
   - `skills/frontend-design/SKILL.md` — composition and visual craft expectations.
   - `skills/web-design-guidelines/SKILL.md` — interaction, accessibility, and UX guardrails.
3. When this repo vendors impeccable scripts, prefer `node skills/impeccable/scripts/load-context.mjs` per **`reference/teach.md`**.

## Procedure

Follow **`reference/teach.md`** end to end: load state, explore the codebase, interview on register/users/brand/accessibility, write `PRODUCT.md`, offer `DESIGN.md` via document flow, confirm, and re-run the context loader.

When design context is complete, hand off to the user's original impeccable task (`polish`, `craft`, `onboard`, etc.) or to **`skills/impeccable/SKILL.md`** for broader workflows.

## Supporting references

- **`reference/teach.md`** — full teach flow (upstream impeccable reference).
