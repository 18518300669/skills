# AGENTS.md

## Cursor Cloud specific instructions

This repository (`cursor-cloud-test`) is a minimal starter repository. It contains a `README.md` and project-local [Agent Skills](https://skills.sh/) under `skills/`.

**Agent skills in this repo**

- **`find-skills`** ([skills.sh leaderboard #1](https://skills.sh/)) — `skills/find-skills/SKILL.md`. Read and follow it when the user wants to discover or install skills from the open ecosystem (for example “find a skill for X”, “how do I do X” where a packaged skill may exist). Source aligned with [vercel-labs/skills find-skills](https://github.com/vercel-labs/skills/tree/main/skills/find-skills).

- **`frontend-design`** ([skills.sh leaderboard #2](https://skills.sh/)) — `skills/frontend-design/SKILL.md`. Read and follow it when building or styling web UI (components, pages, dashboards, landing pages, HTML/CSS layouts, or visual polish). Source aligned with [anthropics/skills frontend-design](https://github.com/anthropics/skills/tree/main/skills/frontend-design) (Apache-2.0; see `skills/frontend-design/LICENSE.txt`).

- **`vercel-react-best-practices`** ([skills.sh leaderboard #3](https://skills.sh/)) — `skills/vercel-react-best-practices/SKILL.md`. Read and follow it when writing, reviewing, or refactoring React or Next.js code for performance (data fetching, bundles, rendering, re-renders). Source aligned with [vercel-labs/agent-skills react-best-practices](https://github.com/vercel-labs/agent-skills/tree/main/skills/react-best-practices) (MIT; see frontmatter in `SKILL.md`).

- **`web-design-guidelines`** ([skills.sh leaderboard #4](https://skills.sh/)) — `skills/web-design-guidelines/SKILL.md`. Read and follow it when auditing UI code against Vercel Web Interface Guidelines (design, accessibility, UX). Source aligned with [vercel-labs/agent-skills web-design-guidelines](https://github.com/vercel-labs/agent-skills/tree/main/skills/web-design-guidelines) (MIT; see frontmatter in `SKILL.md`).

- **`microsoft-foundry`** ([skills.sh leaderboard #5](https://skills.sh/)) — `skills/microsoft-foundry/SKILL.md`. Read and follow it when working with Microsoft Foundry (agent deploy, invoke, evaluation, traces, projects, RBAC, quota, model deployment). Source aligned with [microsoft/azure-skills microsoft-foundry](https://github.com/microsoft/azure-skills/tree/main/skills/microsoft-foundry) (MIT; see `skills/microsoft-foundry/LICENSE.txt` and frontmatter in `SKILL.md`).

- **`remotion-best-practices`** ([skills.sh leaderboard #6](https://skills.sh/remotion-dev/skills/remotion-best-practices)) — `skills/remotion-best-practices/SKILL.md`. Read and follow it when writing, reviewing, or scaffolding [Remotion](https://www.remotion.dev/) code (compositions, timing, assets, captions, audio, FFmpeg, and related video-in-React workflows). Source aligned with [remotion-dev/skills](https://github.com/remotion-dev/skills/tree/main/skills/remotion) (skill package name `remotion-best-practices` on [skills.sh](https://skills.sh/remotion-dev/skills/remotion-best-practices)).

- **`azure-messaging`** ([skills.sh leaderboard #7](https://skills.sh/microsoft/azure-skills/azure-messaging)) — `skills/azure-messaging/SKILL.md`. Read and follow it when diagnosing Azure Event Hubs or Service Bus SDK issues (connections, AMQP, locks, processors, configuration). Source aligned with [microsoft/azure-skills azure-messaging](https://github.com/microsoft/azure-skills/tree/main/skills/azure-messaging) (MIT; see `skills/azure-messaging/LICENSE.txt` and frontmatter in `SKILL.md`).

- **`azure-hosted-copilot-sdk`** ([skills.sh leaderboard #8](https://skills.sh/microsoft/azure-skills/azure-hosted-copilot-sdk)) — `skills/azure-hosted-copilot-sdk/SKILL.md`. Read and follow it when building, deploying, or modifying GitHub Copilot SDK apps on Azure (scaffold, BYOM, `CopilotClient`, `azd` workflows). Source aligned with [microsoft/azure-skills azure-hosted-copilot-sdk](https://github.com/microsoft/azure-skills/tree/main/skills/azure-hosted-copilot-sdk) (MIT; see `skills/azure-hosted-copilot-sdk/LICENSE.txt` and frontmatter in `SKILL.md`).

**Current state:**
- No package manager, no dependency manifest, no build system.
- No services to start, no tests to run, no lint checks configured.
- No database or external service dependencies.

**For future agents:** Once application code is added to this repository, update this section with relevant setup, lint, test, build, and run instructions.
