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

- **`agent-browser`** ([skills.sh leaderboard #9](https://skills.sh/vercel-labs/agent-browser/agent-browser)) — `skills/agent-browser/SKILL.md`. Read and follow it when automating browsers or web apps (navigation, forms, clicks, screenshots, scraping, QA, Electron, Slack, Vercel Sandbox, or AWS AgentCore). Source aligned with [vercel-labs/agent-browser](https://github.com/vercel-labs/agent-browser/tree/main/skills/agent-browser) (Apache-2.0; see `skills/agent-browser/LICENSE.txt` and frontmatter in `SKILL.md`).

- **`azure-compute`** ([skills.sh leaderboard #10](https://skills.sh/microsoft/azure-skills/azure-compute)) — `skills/azure-compute/SKILL.md`. Read and follow it when working with Azure VMs and VM Scale Sets (sizing and pricing, VMSS orchestration, connectivity troubleshooting, capacity reservations, or Essential Machine Management). Source aligned with [microsoft/azure-skills azure-compute](https://github.com/microsoft/azure-skills/tree/main/skills/azure-compute) (MIT; see frontmatter in `SKILL.md`).

- **`azure-cloud-migrate`** ([skills.sh leaderboard #11](https://skills.sh/microsoft/azure-skills/azure-cloud-migrate)) — `skills/azure-cloud-migrate/SKILL.md`. Read and follow it when assessing or migrating workloads from AWS, GCP, or other clouds to Azure (Lambda→Functions, Beanstalk/Heroku/App Engine→App Service, Fargate/K8s/Cloud Run/Spring→Container Apps). Source aligned with [microsoft/azure-skills azure-cloud-migrate](https://github.com/microsoft/azure-skills/tree/main/skills/azure-cloud-migrate) (MIT; see frontmatter in `SKILL.md`).

- **`azure-cost-optimization`** ([skills.sh leaderboard #12](https://skills.sh/microsoft/azure-skills/azure-cost-optimization)) — `skills/azure-cost-optimization/SKILL.md`. Read and follow it when reducing Azure spend (optimization reports, orphaned resources, rightsizing, Redis/AKS-focused cost work). Workflows and references are vendored under `skills/azure-cost/` (unified Azure Cost Management skill: query, forecast, optimization). Source aligned with [microsoft/azure-skills `skills/azure-cost`](https://github.com/microsoft/azure-skills/tree/main/skills/azure-cost) (MIT; see `skills/azure-cost/LICENSE.txt` and frontmatter in `SKILL.md`).

- **`skill-creator`** ([skills.sh leaderboard #13](https://skills.sh/anthropics/skills/skill-creator)) — `skills/skill-creator/SKILL.md`. Read and follow it when creating new agent skills, editing or improving existing skills, running evaluations, benchmarking skill performance, or optimizing a skill description for triggering. Bundled scripts, eval viewer, and agent prompts live under `skills/skill-creator/`. Source aligned with [anthropics/skills skill-creator](https://github.com/anthropics/skills/tree/main/skills/skill-creator) (Apache-2.0; see `skills/skill-creator/LICENSE.txt`).

- **`azure-quotas`** ([skills.sh leaderboard #14](https://skills.sh/microsoft/azure-skills/azure-quotas)) — `skills/azure-quotas/SKILL.md`. Read and follow it when checking or managing Azure subscription quotas and regional capacity (CLI `az quota`, usage vs limits, quota increases, multi-region comparison). Source aligned with [microsoft/azure-skills azure-quotas](https://github.com/microsoft/azure-skills/tree/main/skills/azure-quotas) (MIT; see frontmatter in `SKILL.md`).

- **`azure-upgrade`** ([skills.sh leaderboard #15](https://skills.sh/microsoft/azure-skills/azure-upgrade)) — `skills/azure-upgrade/SKILL.md`. Read and follow it when assessing or automating upgrades of Azure workloads (plan or tier changes, Functions Consumption to Flex Consumption, Redis to Azure Managed Redis, legacy Java `com.microsoft.azure` to `com.azure`). Source aligned with [microsoft/azure-skills azure-upgrade](https://github.com/microsoft/azure-skills/tree/main/skills/azure-upgrade) (MIT; see frontmatter in `SKILL.md`).

- **`vercel-composition-patterns`** ([skills.sh leaderboard #16](https://skills.sh/vercel-labs/agent-skills/vercel-composition-patterns)) — `skills/vercel-composition-patterns/SKILL.md`. Read and follow it when refactoring React components with boolean prop proliferation, building flexible component libraries, or reviewing component architecture (compound components, context providers, explicit variants, React 19 composition APIs). Source aligned with [vercel-labs/agent-skills composition-patterns](https://github.com/vercel-labs/agent-skills/tree/main/skills/composition-patterns) (MIT; see frontmatter in `SKILL.md`).

**Current state:**
- No package manager, no dependency manifest, no build system.
- No services to start, no tests to run, no lint checks configured.
- No database or external service dependencies.

**For future agents:** Once application code is added to this repository, update this section with relevant setup, lint, test, build, and run instructions.
