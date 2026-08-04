# Agent365 Lifecycle and Policy Controls

Atlanta, USA

[![GitHub](https://img.shields.io/badge/--181717?logo=github&logoColor=ffffff)](https://github.com/)
[Cloud2BR OSS - Learning Hub](https://github.com/Cloud2BR-MSFTLearningHub)

Last updated: 2026-08-04

----------

<details markdown>
<summary>References</summary>

- [Agent management overview](https://learn.microsoft.com/en-us/microsoft-365/admin/manage/agent-365-overview)
- [Agent settings and lifecycle actions](https://learn.microsoft.com/en-us/microsoft-365/admin/manage/agent-actions)
- [Microsoft Agent 365 overview](https://learn.microsoft.com/en-us/microsoft-agent-365/overview)

</details>

## Lifecycle objective

Apply repeatable controls from registration through retirement so every agent is
observable, owned, policy-compliant, and reversible.

![Govern capability icon from Microsoft Agent 365 documentation](https://learn.microsoft.com/en-us/microsoft-agent-365/media/hub/govern.png)

*Source: [Microsoft Agent 365 documentation](https://learn.microsoft.com/en-us/microsoft-agent-365/).* 

## Lifecycle states

| State | Entry criteria | Exit criteria |
| --- | --- | --- |
| Proposed | Business case and owner identified | Risk classification complete |
| Pilot | Controls configured in limited scope | Pilot evidence and sign-off complete |
| Production | Monitoring and policy baselines active | Decommission trigger reached |
| Suspended | High-risk issue or policy breach | Remediation verified and approved |
| Retired | Usage ended and records preserved | Archival and revocation complete |

## Policy domains

1. Identity and access policy.
2. Data source and destination policy.
3. Tool and connector policy.
4. Runtime behavior and safety policy.
5. Logging, retention, and audit policy.

## Required policy artifacts

- Standard onboarding checklist.
- Risk-tier matrix and required approvals.
- Exception process with expiry and owner.
- Incident linkage and rollback procedure.
- Decommission process for identity and access cleanup.

## Governance review cadence

| Cadence | Scope |
| --- | --- |
| Weekly | New production requests and exceptions |
| Monthly | High-risk agent lifecycle review |
| Quarterly | Policy template baseline update |

## Business example

> A procurement agent enters production with approved policies. Later, a new tool
> integration raises its risk profile. The lifecycle framework automatically moves
> the change through risk review and controlled reapproval before reactivation.