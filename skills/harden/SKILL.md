---
name: harden
description: Strengthen interfaces against edge cases, errors, internationalization, and real-world data—long text, RTL, API failures, empty states, overflow, and boundary conditions. Use when preparing UI for production, launch, new locales, or bug reports about messy user data. Not for first-run onboarding flows (use onboard) or design-system alignment (use normalize).
license: Apache-2.0. See LICENSE.txt; upstream attribution in NOTICE.md.
user-invocable: true
argument-hint: "[target]"
---

# Harden (production resilience)

This skill is the **harden** workflow from the [skills.sh leaderboard #268](https://skills.sh/pbakaus/impeccable/harden) (sourced from [pbakaus/impeccable](https://github.com/pbakaus/impeccable); catalog install: `npx skills add https://github.com/pbakaus/impeccable --skill harden`). It makes interfaces production-ready against messy data, network failures, i18n expansion, and edge cases that break idealized designs.

## Mandatory preparation

Before hardening:

1. Identify the surfaces to harden (page, component, or flow) and the failure modes users already hit or are likely to hit at launch.
2. Read project-local design guidance:
   - `skills/frontend-design/SKILL.md` — layout, hierarchy, and visual craft.
   - `skills/web-design-guidelines/SKILL.md` — interaction, accessibility, and UX guardrails.
3. Optional: read `skills/impeccable/SKILL.md` when the repo uses the full impeccable harness.

Distinguish this skill from:

- **`skills/onboard/SKILL.md`** — first-run flows, empty states, and activation UX.
- **`skills/normalize/SKILL.md`** — design-system alignment and token conformance.
- **`skills/audit/SKILL.md`** — scored technical audit without applying fixes.

## Procedure

Follow **`reference/harden.md`** end to end: assess hardening needs, work through text overflow, i18n, error handling, edge cases, validation, accessibility resilience, and performance resilience, then verify with extreme inputs.

When structural hardening is complete, hand off to **`skills/polish/SKILL.md`** for the final alignment-and-detail pass.

## Supporting references

- **`reference/harden.md`** — full assess → dimensions → testing → verify workflow (upstream impeccable reference).
