---
name: onboard
description: Design onboarding flows, first-run experiences, and empty states that guide new users to value. Covers welcome screens, account setup, progressive disclosure, contextual tooltips, feature announcements, and activation moments. Use when the user mentions onboarding, first-time users, empty states, activation, getting started, new user flows, or the aha moment.
license: Apache-2.0. See LICENSE.txt; upstream attribution in NOTICE.md.
user-invocable: true
argument-hint: "[target]"
---

# Onboard (first-run and activation)

This skill is the **onboard** workflow from the [skills.sh leaderboard #357](https://skills.sh/pbakaus/impeccable/onboard) (sourced from [pbakaus/impeccable](https://github.com/pbakaus/impeccable); catalog install: `npx skills add https://github.com/pbakaus/impeccable --skill onboard`). It designs first-run flows, empty states, guided tours, and activation moments that get users to their aha moment quickly—not exhaustive product tutorials.

## Mandatory preparation

Before designing onboarding:

1. Clarify the **aha moment** (what proves the product is worth their time) and the target user's experience level.
2. Read project-local design guidance:
   - `skills/frontend-design/SKILL.md` — composition, hierarchy, and visual craft.
   - `skills/web-design-guidelines/SKILL.md` — interaction, accessibility, and UX guardrails.
3. Optional: read `skills/impeccable/SKILL.md` for shared design laws and context-gathering when the repo uses the full impeccable harness.

Distinguish this skill from **`skills/onboarding-cro/SKILL.md`**, which optimizes post-signup activation metrics and lifecycle programs; **onboard** focuses on in-product UX for first-run, empty states, and progressive disclosure.

## Procedure

Follow **`reference/onboard.md`** end to end: assess needs, apply onboarding principles, design experiences (welcome, empty states, tours, tooltips), implement tracking patterns, and verify quality.

When flows are structurally complete, hand off to **`skills/polish/SKILL.md`** for the final alignment-and-detail pass.

## Supporting references

- **`reference/onboard.md`** — full assess → principles → design → empty states → implementation → verify workflow (upstream impeccable reference).
