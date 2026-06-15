---
name: extract
description: Extract and consolidate reusable components, design tokens, and patterns into your design system. Identifies opportunities for systematic reuse and enriches your component library. Use when the user asks to create components, refactor repeated UI patterns, build a design system, or extract tokens.
license: Apache-2.0. See LICENSE.txt; upstream attribution in NOTICE.md.
user-invocable: true
argument-hint: "[target]"
---

# Extract (design system growth)

This skill is the **extract** workflow from the [skills.sh leaderboard #265](https://skills.sh/pbakaus/impeccable/extract) (sourced from [pbakaus/impeccable](https://github.com/pbakaus/impeccable); catalog install: `npx skills add https://github.com/pbakaus/impeccable --skill extract`). It identifies repeated UI patterns, hard-coded values, and inconsistent variations, then extracts reusable components and tokens into the design system with a migration path.

## Mandatory preparation

Before extracting:

1. Read **`skills/impeccable/SKILL.md`** for design principles, anti-patterns, and the Context Gathering Protocol when the repo uses the full impeccable harness.
2. Read **`skills/frontend-design/SKILL.md`** and **`skills/web-design-guidelines/SKILL.md`** for aesthetic direction, accessibility, and interaction guardrails.
3. Search the repository for an existing design system, component library, token files, and style guides (`design system`, `components.json`, `tokens`, `ui`, etc.).

**CRITICAL**: If no design system exists, ask before creating one. Understand the preferred location, naming conventions, and structure first.

## Procedure

Follow **`reference/extract.md`** end to end: discover the system and patterns, plan extraction, build components and tokens, migrate existing uses, and document additions.

Pair with **`skills/normalize/SKILL.md`** when the goal is aligning an existing feature to system standards rather than growing the library. Hand off to **`skills/polish/SKILL.md`** after migration when the surface needs a final craft pass.

## Supporting references

- **`reference/extract.md`** — full discover → plan → extract → migrate → document workflow (upstream impeccable reference).
