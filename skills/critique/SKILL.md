---
name: critique
description: Evaluate design effectiveness across visual hierarchy, information architecture, emotional resonance, and UX quality. Use when the user asks to review, critique, evaluate, or give feedback on a UI, screen, or component; when comparing two design directions; or when they want a structured design-health report before polish. Pairs with project-local `skills/impeccable` and `skills/polish`; optional `npx impeccable` CLI when installed.
license: Apache-2.0. See LICENSE.txt; upstream attribution in NOTICE.md.
---

# Critique (structured design review)

This skill is the **critique** workflow from the [skills.sh catalog](https://skills.sh/pbakaus/impeccable/critique) (sourced from [pbakaus/impeccable](https://github.com/pbakaus/impeccable), installable with `npx skills add https://github.com/pbakaus/impeccable --skill critique`).

## Mandatory preparation

Before critiquing:

1. **Load design law context**: Read `skills/impeccable/SKILL.md` (shared design laws, absolute bans, AI slop test). For aesthetic and composition guidance, also read `skills/frontend-design/SKILL.md` and `skills/web-design-guidelines/SKILL.md`.
2. **Resolve the artifact**: Turn the user's request into a concrete file path or URL (see `reference/critique.md`).
3. **Optional harness**: If the repo has `PRODUCT.md` / `DESIGN.md`, use `node skills/impeccable/scripts/load-context.mjs` when you need full impeccable context.

If no design foundation exists yet, run the **teach** flow described in `skills/impeccable/SKILL.md` (or gather equivalent product and audience notes) before a full critique.

## Procedure

Follow **`reference/critique.md`** end to end. It covers dual independent assessments (LLM design review + automated or manual detection), combined reporting, Nielsen heuristics scoring, persona red flags, snapshot persistence under `.impeccable/critique/`, and recommended follow-up skills.

**Scripts** (from repository root):

- `node skills/critique/scripts/critique-storage.mjs slug "<resolved-path-or-url>"`
- `node skills/critique/scripts/critique-storage.mjs write <slug> <body-file>` (with `IMPECCABLE_CRITIQUE_META` as in `reference/critique.md`)
- `node skills/critique/scripts/critique-storage.mjs trend <slug> 5`

**Automated detection**: When `npx impeccable detect` / `npx impeccable live` are available, use them as in upstream. Otherwise follow the manual fallback in `reference/critique.md` so Assessment B still produces honest, labeled evidence.

## Supporting references

- `reference/critique.md` — main workflow
- `reference/cognitive-load.md` — cognitive load checklist
- `reference/heuristics-scoring.md` — heuristic and severity definitions
- `reference/personas.md` — persona selection and walkthrough style
