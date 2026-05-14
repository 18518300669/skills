---
name: distill
description: Strip UI and flows to their essence by removing redundant structure, visual noise, and unnecessary choices while preserving accessibility and required functionality. Use when the user wants simplification, less clutter, a calmer interface, fewer steps, or ruthless editing after feature bloat. Pairs with project-local polish and design-guideline skills; not for removing legally or operationally required disclosures.
license: Apache-2.0. See LICENSE.txt; upstream attribution in NOTICE.md.
---

# Distill (ruthless simplification)

This skill is the **distill** workflow from the [skills.sh catalog](https://skills.sh/pbakaus/impeccable/distill) (sourced from [pbakaus/impeccable](https://github.com/pbakaus/impeccable), installable with `npx skills add https://github.com/pbakaus/impeccable --skill distill`).

## Mandatory preparation

Before distilling:

1. Confirm you know the **primary user goal** for the surface being simplified (one main job per pass).
2. Read project-local design guidance:
   - `skills/frontend-design/SKILL.md` — composition and visual craft.
   - `skills/web-design-guidelines/SKILL.md` — interaction, spacing, typography, accessibility.
3. Optional: read `skills/impeccable/SKILL.md` for shared design laws and context-gathering when the repo uses the full impeccable harness.

Distill removes obstacles and noise; it does **not** mean stripping required affordances, labels, or accessible patterns.

## Procedure

Follow **`reference/distill.md`** end to end. It covers assessing complexity, planning cuts, simplifying IA/visual/layout/interaction/content/code, verification, and documenting removed scope.

When simplification is structurally complete, hand off to **`skills/polish/SKILL.md`** for the final alignment-and-detail pass.

## Supporting references

- `reference/distill.md` — main workflow (vendored from upstream `distill.md`).
