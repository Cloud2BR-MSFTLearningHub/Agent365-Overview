# Agent365 Agent Registry and Agent Map

Atlanta, USA

[![GitHub](https://img.shields.io/badge/--181717?logo=github&logoColor=ffffff)](https://github.com/)
[Cloud2BR OSS - Learning Hub](https://github.com/Cloud2BR-MSFTLearningHub)

Last updated: 2026-08-04

----------

<details markdown>
<summary>References</summary>

- [Microsoft Agent 365 overview](https://learn.microsoft.com/en-us/microsoft-agent-365/overview)
- [Agent registry (Microsoft 365 admin center)](https://learn.microsoft.com/en-us/microsoft-365/admin/manage/agent-registry)
- [Agent Map](https://learn.microsoft.com/en-us/microsoft-365/admin/manage/agent-map)

</details>

## Purpose

The registry is your source of truth for agent inventory. Agent Map adds
relationship context across identities, apps, tools, data, and activity.

![Observe capability icon from Microsoft Agent 365 documentation](https://learn.microsoft.com/en-us/microsoft-agent-365/media/hub/manage.png)

*Source: [Microsoft Agent 365 documentation](https://learn.microsoft.com/en-us/microsoft-agent-365/).* 

## Minimum registry schema

| Field | Why it is required |
| --- | --- |
| Agent name and unique ID | Prevent ambiguity and duplicate ownership |
| Business owner and technical owner | Ensure accountable triage and decisions |
| Runtime and origin platform | Distinguish control capabilities by platform |
| Identity model | Determine access and audit strategy |
| Approved data sources | Enforce scope and compliance controls |
| Lifecycle state | Govern release, suspension, and retirement |
| Risk tier | Route approvals and monitoring depth |

## Agent Map use cases

1. Trace where an agent is active across channels and apps.
2. Identify high-risk agents with privileged data or broad tool access.
3. Detect orphaned agents without active owners.
4. Prioritize review based on usage volume and risk tier.

## Inventory quality metrics

- Registration completeness rate.
- Owner attribution completeness.
- Unapproved tool or connector count.
- Drift between declared and observed behavior.
- Mean time to register new production agents.

## Operating cadence

| Cadence | Action |
| --- | --- |
| Daily | Review new and changed agent registrations |
| Weekly | Investigate ownership gaps and risk exceptions |
| Monthly | Certify high-risk agent inventory and access |
| Quarterly | Revalidate mandatory metadata standards |

## Business example

> An enterprise discovers multiple duplicated support agents with inconsistent
> ownership and permissions. Using Agent Map relationships, it consolidates them,
> assigns clear ownership, and enforces a mandatory registration policy before
> publication to production channels.