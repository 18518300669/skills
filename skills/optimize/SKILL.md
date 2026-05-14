---
name: optimize
description: Systematically identify and fix frontend performance bottlenecks across loading, rendering, animations, and bundle size using measurement-first workflows and Core Web Vitals targets. Use when the user wants faster pages, better LCP/INP/CLS, smaller bundles, smoother animations, or a performance pass after feature work; pair with audit for diagnosis-only reports and polish after numbers improve.
license: Apache-2.0. See LICENSE.txt; upstream attribution in NOTICE.md.
---

# Optimize (performance)

This skill is the **optimize** workflow from the [skills.sh catalog](https://skills.sh/pbakaus/impeccable/optimize) (sourced from [pbakaus/impeccable](https://github.com/pbakaus/impeccable), installable with `npx skills add https://github.com/pbakaus/impeccable --skill optimize`).

## Mandatory preparation

Before changing code for performance:

1. **Load context**: Read `skills/impeccable/SKILL.md` for shared design laws and bans (do not trade away accessibility or correctness). For web stacks, also read `skills/web-design-guidelines/SKILL.md` and, when the surface is React or Next.js, `skills/vercel-react-best-practices/SKILL.md` and/or `skills/next-best-practices/SKILL.md` as applicable.
2. **Establish a baseline**: Decide how you will measure (Lighthouse, DevTools Performance, RUM, bundle analyzer) and capture **before** numbers for the slow path the user cares about.
3. **Optional harness**: If the repo has `PRODUCT.md` / `DESIGN.md`, run `node skills/impeccable/scripts/load-context.mjs` when performance work must align with documented product constraints.

**Scope boundary:** This skill **implements** optimizations. For a scored, fix-free technical survey first, use `skills/audit/SKILL.md` (performance is one of its dimensions).

## Procedure

Follow **`reference/optimize.md`** end to end. It covers assessing bottlenecks, loading vs rendering vs animation vs network tactics, Core Web Vitals thresholds, verification, and handoff to **polish** after improvements land.

## Supporting references

- `reference/optimize.md` — main workflow (vendored from upstream `skill/reference/optimize.md`, with project-local polish paths)
