# Agent365 Onboarding and Approvals

Atlanta, USA

[![GitHub](https://img.shields.io/badge/--181717?logo=github&logoColor=ffffff)](https://github.com/)
[Cloud2BR OSS - Learning Hub](https://github.com/Cloud2BR-MSFTLearningHub)

Last updated: 2026-08-04

----------

<details markdown>
<summary>References</summary>

- [Connect existing agents](https://learn.microsoft.com/en-us/microsoft-agent-365/connect-existing-agents)
- [Discover partner agents](https://learn.microsoft.com/en-us/microsoft-agent-365/third-party-agents)
- [Agent requests in Microsoft 365 admin center](https://learn.microsoft.com/en-us/microsoft-365/admin/manage/agent-requests)

</details>

## Onboarding objective

Onboarding should be fast for low-risk use cases and deliberate for high-risk
agent capabilities. Approval depth must be proportional to risk.

## Approval lanes

| Lane | Criteria | Typical SLA (service-level agreement) |
| --- | --- | --- |
| Standard | Low-risk internal data, no privileged tools | 3 to 5 business days |
| Elevated | Sensitive data or business-critical workflow | 5 to 10 business days |
| Restricted | Regulated data or high-impact automation | Case-by-case with governance board |

## Evidence required for onboarding

- Business objective and success metric.
- Named owner and support model.
- Data sources and destinations.
- Identity model and permission scope.
- Tooling and external dependency list.
- Risk classification and rollback plan.

## Approval decision matrix

| Decision point | Required approvers |
| --- | --- |
| Initial production enablement | Business owner and AI admin |
| Sensitive data access | Compliance owner and security owner |
| Privileged tool execution | Security owner and platform owner |
| Exception to baseline policy | Governance board delegate |

## Onboarding guardrails

- [ ] No production access without owner accountability.
- [ ] No unmanaged external tool invocation.
- [ ] No unbounded data-source permissions.
- [ ] Every approval includes explicit expiry for exceptions.

## Business example

> A customer support agent is approved in the standard lane. A follow-up request
> adds finance data access, which automatically routes to elevated review. The
> team receives fast initial delivery while preserving stronger control for the
> higher-risk expansion.