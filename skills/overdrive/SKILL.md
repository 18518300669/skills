---
name: overdrive
description: Push interfaces past conventional limits with technically ambitious, context-aware implementations—cinematic transitions (View Transitions API, spring physics), scroll-driven animation, GPU rendering (WebGL/WebGPU/Canvas), and high-performance data UI. Use when a moment should feel extraordinary and budget allows; not for operator tools or dashboards where reliability beats spectacle. Requires design context first; propose 2–3 directions before building; verify with browser automation and prefers-reduced-motion fallbacks.
license: Apache-2.0. See LICENSE.txt; upstream attribution in NOTICE.md.
---

# Overdrive (technical ambition)

This skill is the **overdrive** workflow from the [skills.sh leaderboard #319](https://skills.sh/pbakaus/impeccable/overdrive) (sourced from [pbakaus/impeccable](https://github.com/pbakaus/impeccable), installable with `npx skills add https://github.com/pbakaus/impeccable --skill overdrive`). It pushes one interface moment past what users expect from the web—without spraying spectacle across every surface.

Start your response with:

```text
──────────── ⚡ OVERDRIVE ─────────────
》》》 Entering overdrive mode...
```

## Mandatory preparation

Before overdrive work:

1. Read **`skills/impeccable/SKILL.md`** for register guidance (brand vs product), the Context Gathering Protocol, and anti-patterns. If no design context exists yet, run the impeccable **teach** workflow or gather equivalent `PRODUCT.md` / `DESIGN.md` context before proposing directions.
2. Read **`skills/frontend-design/SKILL.md`** and **`skills/web-design-guidelines/SKILL.md`** for aesthetic direction, accessibility, and motion guardrails.
3. Confirm the target moment (hero, dialog, table, form, transition) and that **spectacle is appropriate** for this brand and surface. Do not use overdrive on operator tools, dense dashboards, or reliability-first workflows.

**Context determines what "extraordinary" means.** A particle hero on a portfolio is impressive; the same on a settings page is embarrassing. Instant optimistic saves with animated state transitions can be extraordinary on a settings page.

## Propose before building

This skill has the highest misfire risk. Do **not** jump straight into implementation.

1. Think through **2–3 directions** (technique, ambition level, aesthetic). Briefly describe what each would look and feel like.
2. Present trade-offs (browser support, performance cost, complexity, dependencies) and get the user's pick before writing code.
3. Proceed only with the confirmed direction.

## Procedure

Follow **`reference/overdrive.md`** end to end for surface assessment (visual vs functional vs performance vs data-heavy), the technique toolkit, progressive enhancement, 60fps performance rules, browser automation iteration, and verification (wow / removal / device / accessibility / context tests).

Pair with **`skills/animate/SKILL.md`** for motion that clarifies state; with **`skills/optimize/SKILL.md`** when performance is the extraordinary axis; with **`skills/agent-browser/SKILL.md`** or **`skills/webapp-testing/SKILL.md`** for visual iteration. Hand off to **`skills/polish/SKILL.md`** after the effect is stable.
