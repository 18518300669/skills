---
name: colorize
description: Strategically introduce color to monochromatic or gray-heavy UI while preserving hierarchy, accessibility, and restraint. Use when dashboards, forms, or marketing surfaces read as flat grayscale, lack semantic state color, or need brand warmth without rainbow overload. Pair with frontend-design for craft and web-design-guidelines for contrast and interaction checks; hand off to polish when the palette is in place.
license: Apache-2.0. See LICENSE.txt; upstream attribution in NOTICE.md.
---

# Colorize (strategic palette)

This skill is the **colorize** workflow from the [skills.sh leaderboard](https://skills.sh/pbakaus/impeccable/colorize) (sourced from [pbakaus/impeccable](https://github.com/pbakaus/impeccable)). It replaces timid grayscale with a purposeful palette: semantic states, tinted neutrals, restrained accents, and OKLCH-friendly scales—without defaulting to generic purple–cyan gradients.

## Mandatory preparation

Before colorizing:

1. Read **`skills/frontend-design/SKILL.md`** for aesthetic direction, OKLCH usage, and anti-patterns.
2. Read **`skills/web-design-guidelines/SKILL.md`** for contrast, focus, and non–color-only state signaling.
3. If the repository uses the full **impeccable** harness (`PRODUCT.md` / `DESIGN.md`), load context per `skills/impeccable/SKILL.md` and capture **existing brand colors** before choosing new hues.

If brand colors or semantic roles are unclear from the codebase, ask the user once rather than inventing a palette from model defaults.

## Procedure

Follow **`reference/colorize.md`** end to end for register-specific rules (brand vs product), application dimensions, balance checks, and verification.

When the palette is stable, continue with **`skills/polish/SKILL.md`** for the final ship pass.
