---
name: audit
description: Run systematic technical quality checks across accessibility, performance, theming, responsive design, and anti-patterns; score each dimension and produce a severity-ranked report without fixing code. Use before shipping, during a quality sprint, or when the user asks for an a11y/perf/responsive audit, a tech health report, or P0–P3 findings to route into polish or harden workflows.
license: Apache-2.0. See LICENSE.txt; upstream attribution in NOTICE.md.
---

# Audit (technical quality report)

This skill is the **audit** workflow from the [skills.sh catalog](https://skills.sh/pbakaus/impeccable/audit) (sourced from [pbakaus/impeccable](https://github.com/pbakaus/impeccable), installable with `npx skills add https://github.com/pbakaus/impeccable --skill audit`).

## Mandatory preparation

Before auditing:

1. **Load design and implementation law context**: Read `skills/impeccable/SKILL.md` (shared design laws, absolute bans, AI slop test). For measurable web checks, also load `skills/web-design-guidelines/SKILL.md` when the surface is a web UI.
2. **Resolve the target**: Turn the user's request into concrete paths, routes, or a URL (components, pages, or a feature area).
3. **Optional harness**: If the repo has `PRODUCT.md` / `DESIGN.md`, use `node skills/impeccable/scripts/load-context.mjs` when you need full impeccable context.

If no design foundation exists yet, run the **teach** flow described in `skills/impeccable/SKILL.md` before a full audit when the work depends on product or audience constraints.

**Scope boundary:** This is a **technical** audit (measurable implementation quality). For subjective design effectiveness, pair with `skills/critique/SKILL.md`.

## Procedure

Follow **`reference/audit.md`** end to end. It defines the five-dimension diagnostic scan (0–4 scores), P0–P3 severity tagging, report structure, pattern mining, and how to route follow-ups to other impeccable workflows.

**Do not apply fixes during the audit** — document findings for downstream commands and skills.

## Supporting references

- `reference/audit.md` — main workflow and report template
