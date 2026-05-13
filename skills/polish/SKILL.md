---
name: polish
description: Final quality pass catching alignment, spacing, consistency, and interaction details before shipping. Use when the user wants a last-mile UI polish, pre-release review of a screen or component, or to systematically tighten visual craft after feature work is functionally complete. Requires prior design context (see preparation); not for backend-only tasks.
license: Apache-2.0. See LICENSE.txt; upstream attribution in NOTICE.md.
---

# Polish (final UI pass)

This skill is the **polish** workflow from the [skills.sh leaderboard](https://skills.sh/pbakaus/impeccable/polish) (sourced from [pbakaus/impeccable](https://github.com/pbakaus/impeccable)). It catches alignment, spacing, consistency, micro-interactions, and edge-case gaps before ship.

## Mandatory preparation

Before polishing:

1. Confirm the surface is **functionally complete** (polish is last, not first).
2. Gather **quality bar** (MVP vs flagship) and ship timeline from the user or task context.
3. Read project-local design guidance in this repository:
   - `skills/frontend-design/SKILL.md` — aesthetic direction and craft expectations.
   - `skills/web-design-guidelines/SKILL.md` — spacing, typography, interaction, and accessibility checks.

If the repository later adds full **impeccable** harness files (`PRODUCT.md` / `DESIGN.md` and scripts), prefer that upstream workflow; this vendored copy stays self-contained for agents that only have project-local skills.

## Procedure

Follow **`reference/polish.md`** end to end. It expands pre-assessment, systematic dimensions, checklist, verification, and cleanup.

When `reference/polish.md` mentions loading prior critique snapshots via Node scripts (impeccable-specific), substitute: incorporate any **existing** written critique, audit notes, or design review for the same target from the repo or chat; if none exist, continue with your own pass.
