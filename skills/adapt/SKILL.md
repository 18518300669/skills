---
name: adapt
description: Rethink layouts and interactions for different screens, devices, and contexts (mobile, tablet, desktop, print, email) without treating adaptation as simple scaling. Use when a design works in one context but breaks on touch, narrow widths, or other platforms; pairs with impeccable, frontend-design, web-design-guidelines, and polish.
license: Apache-2.0. See LICENSE.txt; upstream attribution in NOTICE.md.
---

# Adapt (cross-context design)

This skill is the **adapt** workflow from the [skills.sh catalog](https://skills.sh/pbakaus/impeccable/adapt) (sourced from [pbakaus/impeccable](https://github.com/pbakaus/impeccable), installable with `npx skills add https://github.com/pbakaus/impeccable --skill adapt`).

## Mandatory preparation

Before changing breakpoints, navigation patterns, or density:

1. **Load shared design law**: Read `skills/impeccable/SKILL.md` for register guidance (brand vs product), bans, and how responsive work should preserve capability—not hide it.
2. **Load craft context**: Read `skills/frontend-design/SKILL.md` for aesthetic direction; read `skills/web-design-guidelines/SKILL.md` for touch targets, motion, and accessibility expectations.
3. **Gather targets**: Confirm **source context** (what the UI was designed for) and **target contexts** (devices, input methods, connection assumptions, usage patterns).

If the repository has `PRODUCT.md` / `DESIGN.md` and you need full harness context, use `node skills/impeccable/scripts/load-context.mjs` when available.

If no design foundation exists yet, run the **teach** flow described in `skills/impeccable/SKILL.md` (or capture equivalent notes) before large layout restructures.

## Procedure

Follow **`reference/adapt.md`** end to end. It covers assessing source vs target context, planning mobile/tablet/desktop/print/email strategies, implementation techniques (grid, container queries, `clamp()`, touch), verification on real devices, and handoff to **polish**.

## Supporting references

- `reference/adapt.md` — main workflow (vendored from upstream `skill/reference/adapt.md`, with project-local polish handoff)
