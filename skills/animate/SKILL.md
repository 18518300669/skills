---
name: animate
description: Plan and implement purposeful UI motion (feedback, transitions, entrances, reduced-motion) for web or app surfaces. Use when the user wants animations, micro-interactions, page-load choreography, scroll-driven motion, or to fix jarring state changes without decorating for decoration's sake.
license: Apache-2.0. See LICENSE.txt; upstream attribution in NOTICE.md.
---

# Animate (purposeful motion)

This skill is the **animate** workflow from the [skills.sh catalog](https://skills.sh/pbakaus/impeccable/animate) (sourced from [pbakaus/impeccable](https://github.com/pbakaus/impeccable), installable with `npx skills add https://github.com/pbakaus/impeccable --skill animate`).

## Mandatory preparation

Before animating:

1. **Load shared design law**: Read `skills/impeccable/SKILL.md` for register guidance (brand vs product), bans, and how motion should clarify state.
2. **Load craft context**: Read `skills/frontend-design/SKILL.md` for aesthetic direction; read `skills/web-design-guidelines/SKILL.md` for interaction, motion sensitivity, and accessibility expectations.
3. **Resolve the target**: Concrete components, routes, or URLs where motion will ship.

If the repository has `PRODUCT.md` / `DESIGN.md` and you need full harness context, use `node skills/impeccable/scripts/load-context.mjs` when available.

## Procedure

Follow **`reference/animate.md`** end to end. It covers register-specific tone, opportunity assessment, animation strategy, implementation categories (CSS, JS libraries, performance), verification, and handoff to polish when motion is in service of clarity.

## Supporting references

- `reference/animate.md` — main workflow (vendored from upstream `skill/reference/animate.md`)
