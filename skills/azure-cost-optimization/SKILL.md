---
name: azure-cost-optimization
description: "Identify cost savings across Azure subscriptions through resource analysis, utilization metrics, and optimization recommendations. WHEN: optimize Azure costs, reduce spending, cost optimization report, orphaned resources, rightsizing, Redis cost optimization, AKS cost analysis add-on, namespace cost, cost spike, budget alert. Uses Cost Management and Monitor data; requires Cost Management Reader, Monitoring Reader, and Reader on scope."
license: MIT
metadata:
  author: Microsoft
  version: "1.2.1"
---

# Azure Cost Optimization

> This entry matches [**skills.sh** leaderboard #12 — `azure-cost-optimization`](https://skills.sh/microsoft/azure-skills/azure-cost-optimization). The procedural content lives in the upstream-aligned [**Azure Cost Management**](../azure-cost/SKILL.md) skill (`microsoft/azure-skills`, package path `skills/azure-cost`).

## When to Use

Read and follow this skill when the user wants to **reduce spend** (not only view historical costs): optimization reports, orphaned/unused resources, rightsizing, Redis-specific or AKS-specific cost work, and prioritized savings with audit-friendly outputs.

## Canonical workflow

Execute the full pipeline in:

**[../azure-cost/cost-optimization/workflow.md](../azure-cost/cost-optimization/workflow.md)**

That workflow references:

- [Azure Quick Review (azqr)](../azure-cost/cost-optimization/azure-quick-review.md)
- [Azure Resource Graph patterns](../azure-cost/cost-optimization/azure-resource-graph.md)
- [Report template](../azure-cost/cost-optimization/report-template.md)
- [Redis focus](../azure-cost/cost-optimization/services/redis/azure-cache-for-redis.md)
- [AKS cost analysis add-on](../azure-cost/cost-optimization/azure-aks-cost-addon.md)
- [AKS cost anomalies & budgets](../azure-cost/cost-optimization/azure-aks-anomalies.md)

## Cost breakdown alongside optimization

The optimization workflow assumes you also pull **actual costs and breakdowns** via:

**[../azure-cost/cost-query/workflow.md](../azure-cost/cost-query/workflow.md)**

Always present the bill and top drivers together with savings recommendations (see the note at the top of the optimization workflow).

## Source

Aligned with [microsoft/azure-skills](https://github.com/microsoft/azure-skills) (`skills/azure-cost`, cost-optimization workflows). Published install string on skills.sh: `npx skills add https://github.com/microsoft/azure-skills --skill azure-cost-optimization`.
