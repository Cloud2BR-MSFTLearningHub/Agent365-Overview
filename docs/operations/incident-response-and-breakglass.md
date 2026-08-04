# Agent365 Incident Response and Break-Glass

Atlanta, USA

[![GitHub](https://img.shields.io/badge/--181717?logo=github&logoColor=ffffff)](https://github.com/)
[Cloud2BR OSS - Learning Hub](https://github.com/Cloud2BR-MSFTLearningHub)

Last updated: 2026-08-04

----------

<details markdown>
<summary>References</summary>

- [Secure AI agents at scale](https://learn.microsoft.com/en-us/security/security-for-ai/agent-365-security)
- [Detect, protect, and investigate agent threats](https://learn.microsoft.com/en-us/defender-xdr/security-for-ai/ai-agent-detection-protection)
- [Advanced hunting overview](https://learn.microsoft.com/en-us/defender-xdr/advanced-hunting-overview)

</details>

## Incident response objective

Contain agent risk quickly without breaking legitimate business operations.
Break-glass controls should be rare, explicit, and thoroughly audited.

## Incident severity model

| Severity | Example scenario | Response target |
| --- | --- | --- |
| Sev 1 | Confirmed data exfiltration or malicious autonomous action | Immediate containment |
| Sev 2 | High-confidence suspicious behavior with business impact risk | Rapid triage and constrained containment |
| Sev 3 | Policy drift or moderate anomalous behavior | Scheduled response with monitoring |
| Sev 4 | Low-confidence noise or known false-positive pattern | Tune and document |

## Containment playbook

1. Suspend affected agent or revoke high-risk tool access.
2. Lock or rotate agent credentials if compromise is suspected.
3. Preserve telemetry and policy evidence for investigation.
4. Notify owner, security, and compliance stakeholders.
5. Validate blast radius before partial or full service restoration.

## Break-glass governance

- Break-glass accounts must be isolated and strongly protected.
- Use only for predefined scenarios where normal controls are unavailable.
- Require dual authorization and post-use review.
- Expire emergency access immediately after incident stabilization.

## Post-incident requirements

- Root cause analysis with identity, policy, and runtime factors.
- Control updates mapped to prevent recurrence.
- Owner education and runbook updates.
- Executive summary for high-impact events.

## Business example

> A security alert indicates unusual privileged tool calls by an internal finance
> agent. The team suspends tool execution, rotates credentials, and scopes impact.
> Investigation finds an overbroad permission update during maintenance. The
> remediation introduces stricter change gates and automated permission checks.