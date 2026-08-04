# Microsoft Agent 365 Setup and Overview Hub

Atlanta, USA

[![GitHub](https://img.shields.io/badge/--181717?logo=github&logoColor=ffffff)](https://github.com/)
[Cloud2BR OSS - Learning Hub](https://github.com/Cloud2BR-MSFTLearningHub)

Last updated: 2026-08-04

----------

![Microsoft Agent 365 documentation banner from Microsoft Learn](https://learn.microsoft.com/en-us/microsoft-agent-365/media/hub/banner.png)

Agent 365 is the enterprise control plane for agent ecosystems. This hub provides
a practical, implementation-first blueprint for IT, security, and platform teams
to observe, govern, secure, and operationalize agents at scale.

!!! warning
    These guides are learning material. Validate current service behavior,
    licensing, and support boundaries in official Microsoft documentation before
    production rollout.

<div class="guide-grid">
  <a class="guide-card" href="overview/"><strong>Start Here</strong><br>Understand Agent 365 capabilities, scope, and decision points.</a>
  <a class="guide-card" href="foundation/architecture-and-control-plane/"><strong>Foundation</strong><br>Design tenant, identity, ownership, and data boundaries.</a>
  <a class="guide-card" href="observe/agent-registry-and-map/"><strong>Observe</strong><br>Build complete agent inventory, telemetry, health, and KPI tracking.</a>
  <a class="guide-card" href="govern/lifecycle-and-policy/"><strong>Govern</strong><br>Apply lifecycle controls, approvals, policies, and MCP/tool standards.</a>
  <a class="guide-card" href="secure/security-posture-and-defender/"><strong>Secure</strong><br>Reduce risk with identity controls, Defender, and runtime protection.</a>
  <a class="guide-card" href="operations/deployment-checklist/"><strong>Operate</strong><br>Deploy with evidence, run production safely, and handle incidents.</a>
</div>

## Use this hub

| If your goal is | Start with |
| --- | --- |
| Understand what Agent 365 changes operationally | [Overview](overview.md) |
| Define architecture and operating boundaries | [Architecture and control plane](foundation/architecture-and-control-plane.md) |
| Establish least-privilege access | [Roles, identity, and access](foundation/roles-identity-and-access.md) |
| Discover and monitor all agents | [Agent registry and Agent Map](observe/agent-registry-and-map.md) |
| Create governance and approvals | [Lifecycle and policy controls](govern/lifecycle-and-policy.md) |
| Protect data and reduce leakage risk | [Data security and Purview](secure/data-security-and-purview.md) |
| Prepare production rollout | [Deployment checklist](operations/deployment-checklist.md) |

## Recommended implementation sequence

1. Build your foundation: architecture, ownership, identity, and policy boundaries.
2. Onboard a pilot set of agents and validate discovery, observability, and controls.
3. Operationalize governance and security controls with approval and rollback paths.
4. Move to scaled operations only after KPI and incident workflows are proven.
