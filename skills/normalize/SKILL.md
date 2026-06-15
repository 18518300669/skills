---
name: normalize
description: Align a feature with design system standards—typography, color, spacing, components, motion, responsive behavior, and accessibility—by discovering tokens and patterns first, then replacing one-offs with system equivalents. Use when UI drifts from the design system, mixes hard-coded values with tokens, or duplicates components that already exist in the library. Requires design context via impeccable teach when missing; not for net-new visual polish without structural alignment (use polish after normalize).
license: Apache-2.0. See LICENSE.txt; upstream attribution in NOTICE.md.
---

# Normalize (design system alignment)

This skill is the **normalize** workflow from the [skills.sh leaderboard #349](https://skills.sh/pbakaus/impeccable/normalize) (sourced from [pbakaus/impeccable](https://github.com/pbakaus/impeccable); catalog install: `npx skills add https://github.com/pbakaus/impeccable --skill normalize`). It analyzes and redesigns a feature so it matches design system standards, aesthetics, and established patterns—prioritizing UX consistency and token-driven implementation over decorative polish alone.

## Mandatory preparation

Before normalizing:

1. Read **`skills/impeccable/SKILL.md`** for design principles, anti-patterns, and the Context Gathering Protocol. If no design context exists yet (`PRODUCT.md` / `DESIGN.md` or equivalent), run the impeccable **teach** workflow or gather equivalent context before changing UI.
2. Read **`skills/frontend-design/SKILL.md`** and **`skills/web-design-guidelines/SKILL.md`** for aesthetic direction, accessibility, and interaction guardrails.
3. Search the repository for design system documentation, UI guidelines, component libraries, style guides, and token definitions (`design system`, `ui guide`, `style guide`, `tokens`, `components.json`, etc.).

**CRITICAL**: If design system principles are ambiguous, ask targeted questions. Do not guess at tokens, patterns, or hierarchy.

## Procedure

Follow **`reference/normalize.md`** end to end: plan (discover system, assess drift, define changes), execute across eight dimensions, then clean up shared components and orphaned code.

When alignment is solid, hand off to **`skills/polish/SKILL.md`** for the final ship pass. Use **`skills/audit/SKILL.md`** or **`skills/critique/SKILL.md`** first when you need a structured pre-normalization report.

## Distinction from polish

- **Normalize** — structural alignment: tokens, shared components, flows, and patterns match the design system; removes one-offs and drift.
- **Polish** — final craft pass after functionality and alignment are complete: spacing nits, micro-interactions, edge cases.

Normalize may touch the same surfaces as polish but must not skip discovery or substitute decoration for system conformance.
