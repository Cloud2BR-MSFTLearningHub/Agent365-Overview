# Agent365 Tools and MCP Governance

Atlanta, USA

[![GitHub](https://img.shields.io/badge/--181717?logo=github&logoColor=ffffff)](https://github.com/)
[Cloud2BR OSS - Learning Hub](https://github.com/Cloud2BR-MSFTLearningHub)

Last updated: 2026-08-04

----------

<details markdown>
<summary>References</summary>

- [Manage tools for agents](https://learn.microsoft.com/en-us/microsoft-365/admin/manage/manage-tools-for-agent)
- [Work IQ MCP overview](https://learn.microsoft.com/en-us/microsoft-agent-365/tooling-servers-overview)
- [Copilot Studio MCP certification](https://learn.microsoft.com/en-us/microsoft-copilot-studio/mcp-certification)

</details>

## Governance objective

Agent tools and model context protocol (MCP) integrations can create high-value
automation and high-impact risk. Governance must enforce bounded capability and
traceable authorization.

## Tool risk tiers

| Tier | Tool characteristics | Required controls |
| --- | --- | --- |
| Tier 1 | Read-only internal lookup | Owner approval and basic monitoring |
| Tier 2 | Writes to business systems | Change control and stronger alerting |
| Tier 3 | Privileged, financial, or regulated actions | Segregated approvals, runtime controls, audit evidence |

## MCP governance requirements

1. Tool registration with owner, purpose, and risk tier.
2. Contracted input and output validation requirements.
3. Explicit allowed operations and denied operations list.
4. Credential and token management standards.
5. Runtime logging and abnormal-use detection.

## Approval checklist for new tool integrations

- [ ] Business need and measurable outcome documented.
- [ ] Least-privilege permissions validated.
- [ ] Data handling impact assessed.
- [ ] Failure and rollback behavior tested.
- [ ] Runtime observability and alerts configured.

## Runtime safeguards

- Rate limits by tenant, app, and agent.
- Timeouts and retry ceilings for external operations.
- Human approval gates for high-impact actions.
- Automatic suspension triggers for anomalous behaviors.

## Business example

> A procurement automation agent uses an MCP server to create purchase requests.
> Because the action changes financial systems, governance classifies it as Tier 3,
> requires dual approval for production enablement, and introduces runtime approval
> prompts for high-value transactions.