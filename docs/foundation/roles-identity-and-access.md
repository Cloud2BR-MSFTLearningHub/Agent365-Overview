# Agent365 Roles, Identity, and Access

Atlanta, USA

[![GitHub](https://img.shields.io/badge/--181717?logo=github&logoColor=ffffff)](https://github.com/)
[Cloud2BR OSS - Learning Hub](https://github.com/Cloud2BR-MSFTLearningHub)

Last updated: 2026-08-04

----------

<details markdown>
<summary>References</summary>

- [Microsoft Agent 365 overview](https://learn.microsoft.com/en-us/microsoft-agent-365/overview)
- [Copilot architecture: conditional access and multifactor authentication](https://learn.microsoft.com/en-us/microsoft-365/copilot/microsoft-365-copilot-architecture)
- [Protect AI with Conditional Access policy](https://learn.microsoft.com/en-us/entra/identity/conditional-access/policy-all-users-copilot-ai-security)

</details>

## Why this matters

Most agent incidents are identity incidents first. Over-privileged access,
inconsistent service principals, and weak approval separation can quickly become
enterprise-scale data or control failures.

![Conditional Access and multifactor authentication for Copilot](https://learn.microsoft.com/en-us/microsoft-365/copilot/media/microsoft-365-copilot-architecture/copilot-conditional-access-mfa.png)

*Source: [How Microsoft 365 Copilot works](https://learn.microsoft.com/en-us/microsoft-365/copilot/microsoft-365-copilot-architecture).* 

## Role model

| Role | Responsibility | Must not also own |
| --- | --- | --- |
| Agent business owner | Outcome definition, risk acceptance, prioritization | Security exception approval |
| Agent technical owner | Implementation, release, support | Independent audit sign-off |
| AI admin | Registry, lifecycle operations, policy execution | Unreviewed production bypass |
| Security operations | Monitoring, triage, response | Sole authority for business risk acceptance |
| Compliance owner | Data handling controls and evidence quality | Unilateral deployment approvals |

## Identity patterns

1. User-delegated execution for user-context tasks with strict access inheritance.
2. Agent-owned identity for autonomous workflows with explicit resource permissions.
3. Hybrid identity with constrained elevation for high-trust operations.

## Access principles

- Least privilege by default, with role-based access control (RBAC) at the narrowest practical scope.
- Just-in-time elevation for sensitive lifecycle operations.
- Policy-based restrictions for non-compliant devices and risky sessions.
- Explicit approval for cross-domain data access and external tooling.

## Minimum controls

- [ ] Every agent identity has named owner and renewal cadence.
- [ ] Privileged assignments require time-bound activation and logging.
- [ ] Conditional access protects admin and high-risk workflows.
- [ ] Access reviews run on a fixed schedule with documented remediation.
- [ ] Break-glass usage is auditable and independently reviewed.

## Validation scenarios

| Scenario | Expected result |
| --- | --- |
| Suspended user prompts an agent | Access denied and event captured |
| Agent requests out-of-scope resource | Request blocked and owner alerted |
| Privileged action without approval context | Action denied or queued for approval |
| Policy exception expired | Access automatically reverts to baseline |

## Business example

> A team introduces agent-owned identities for unattended workflows. During pilot,
> it detects broad graph permissions and replaces them with scoped permissions plus
> just-in-time elevation for sensitive actions. This reduces standing privilege and
> improves audit traceability without blocking delivery.