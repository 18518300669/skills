---
name: azure-observability
description: "Query metrics, logs, and distributed traces across Azure Monitor, Application Insights, and Log Analytics using MCP tools or Azure CLI. WHEN: Azure Monitor metrics, KQL log query, Log Analytics workspace, Application Insights APM, distributed tracing, monitor alerts, workbook, resource usage, request performance, error rate, dependency failures, availability tests, trace correlation, App Insights query, metrics explorer."
license: MIT
metadata:
  author: Microsoft
  version: "1.0.0"
---

# Azure Observability (Monitor, Log Analytics, Application Insights)

Use this skill when the user needs **metrics**, **logs (KQL)**, **traces**, or **dashboards** across Azure observability services—not when they only need deployment (use **azure-deploy**) or deep live-site triage playbooks (use **azure-diagnostics** alongside this skill).

## Services

| Service | Use when | MCP tools (typical) | CLI |
| --- | --- | --- | --- |
| Azure Monitor | Platform metrics, metric alerts, activity logs | `mcp_azure_mcp_monitor` | `az monitor` |
| Application Insights | APM, requests, dependencies, exceptions, distributed traces | `mcp_azure_mcp_applicationinsights` | `az monitor app-insights` |
| Log Analytics | Tables in a workspace, custom KQL, cross-resource queries | `mcp_azure_mcp_monitor` (logs / KQL) | `az monitor log-analytics` |
| Alerts | Alert rules, action groups, fired alerts | — (prefer portal or ARM/Bicep) | `az monitor alert` |
| Workbooks | Saved interactive reports | varies by MCP surface | create via portal / ARM |

Tool names can differ by Azure MCP server build. If a call fails with “unknown tool”, use **`mcp_azure_mcp_documentation`** to confirm the exact tool and action names exposed in the client, then prefer the smallest matching operation.

## When to use this skill

- Metrics: CPU, memory, request count, latency percentiles, dependency duration
- Logs: exceptions, failed requests, container stdout, diagnostic settings to Log Analytics
- Traces: `operation_Id`, end-to-end transaction search, slow spans
- Comparisons before/after deploy, canary, or config change using time windows

## Preferred workflow (MCP first)

1. **Identify scope** — subscription, resource group, App Insights component or Log Analytics workspace, and time range (`ago(1h)`, `ago(24h)`, etc.).
2. **Metrics** — Use the Azure Monitor path on `mcp_azure_mcp_monitor` (for example metrics query actions as exposed by the client) for resource-level aggregates.
3. **Logs / KQL** — Use log query actions on `mcp_azure_mcp_monitor` or workspace-specific tools when available; scope queries to the workspace linked to the application.
4. **Application Insights** — Use `mcp_azure_mcp_applicationinsights` for component metadata, availability, and App Insights–centric operations when exposed.
5. **Explain results** — Summarize tables or charts; call out sampling, ingestion delay, and retention limits.

## KQL patterns (Log Analytics / App Insights tables)

Always bound time first (`where TimeGenerated > ago(...)` or `where Timestamp > ago(...)` depending on schema).

### Errors and failed dependencies

```kql
exceptions
| where timestamp > ago(24h)
| summarize count() by type, outerMessage
| order by count_ desc
```

```kql
dependencies
| where timestamp > ago(24h) and success == false
| summarize fail=count() by name, resultCode
| order by fail desc
```

### Request latency (p50 / p95)

```kql
requests
| where timestamp > ago(24h)
| summarize
    p50=percentile(duration, 50),
    p95=percentile(duration, 95),
    n=count()
  by bin(timestamp, 5m)
| render timechart
```

### Resource usage (VM / Container Apps — table names vary)

```kql
Perf
| where TimeGenerated > ago(1h) and CounterName == "% Processor Time"
| summarize avg(CounterValue) by Computer, bin(TimeGenerated, 5m)
| render timechart
```

### Trace correlation

```kql
union requests, dependencies, traces, exceptions
| where operation_Id == "<paste-operation-id>"
| project timestamp, itemType, name, message, resultCode, duration
| order by timestamp asc
```

## Azure CLI fallbacks

When MCP is unavailable or times out:

| Goal | Example |
| --- | --- |
| List App Insights components | `az monitor app-insights component list -g <rg>` |
| Query workspace (KQL) | `az monitor log-analytics query -w <workspace-id> --analytics-query "<kql>"` |
| List metrics definitions | `az monitor metrics list-definitions --resource <arm-id>` |
| Query metrics | `az monitor metrics list --resource <arm-id> --metric "<name>" --start-time ... --end-time ... --interval PT1M` |

Use `az monitor log-analytics workspace list -g <rg>` to resolve workspace IDs.

## Workbooks

Workbooks are JSON-based resources; prefer creating or editing in the Azure portal unless the user explicitly wants infrastructure-as-code. Link workbook results back to underlying queries where helpful.

## Boundaries

- **azure-diagnostics** — structured production triage (AppLens, resource health, service-specific debug flows). Use together: observability data here, playbooks there.
- **azure-kusto** — dedicated Azure Data Explorer (ADX) clusters and advanced Kusto-only scenarios; Log Analytics still uses KQL but different management plane.
- **azure-cost** / **azure-cost-optimization** — spend and reservations, not latency diagnostics.

## References

- Use **`mcp_azure_mcp_documentation`** for Microsoft Learn links on Monitor, KQL, and Application Insights.
- Catalog: [azure-observability on skills.sh](https://skills.sh/microsoft/azure-skills/azure-observability).
