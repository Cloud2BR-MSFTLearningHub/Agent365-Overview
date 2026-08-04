# Agent365 Data Boundary and Compliance

Atlanta, USA

[![GitHub](https://img.shields.io/badge/--181717?logo=github&logoColor=ffffff)](https://github.com/)
[Cloud2BR OSS - Learning Hub](https://github.com/Cloud2BR-MSFTLearningHub)

Last updated: 2026-08-04

----------

<details markdown>
<summary>References</summary>

- [Microsoft Agent 365 overview](https://learn.microsoft.com/en-us/microsoft-agent-365/overview)
- [Microsoft Purview for AI (artificial intelligence) apps](https://learn.microsoft.com/en-us/purview/ai-microsoft-purview)
- [Use Microsoft Purview for Agent365](https://learn.microsoft.com/en-us/purview/ai-agent-365)
- [Data privacy for Microsoft 365 Copilot](https://learn.microsoft.com/en-us/microsoft-365/copilot/microsoft-365-copilot-privacy)

</details>

## Data boundary objective

Define which data classes and systems agents can access, transform, store, or
transmit, and enforce policy guardrails before scaling adoption.

![Microsoft 365 services that help prepare data for Copilot](https://learn.microsoft.com/en-us/microsoft-365/copilot/media/copilot-services-help.png)

*Source: [Microsoft 365 Copilot overview](https://learn.microsoft.com/en-us/microsoft-365/copilot/microsoft-365-copilot-overview).* 

## Data handling zones

| Zone | Typical data | Agent policy baseline |
| --- | --- | --- |
| Public | Marketing content and public knowledge | Open use with standard monitoring |
| Internal | Operational documents and routine business data | Approved agent access, standard controls |
| Sensitive | Personal, financial, and contractual information | Restricted access, stronger DLP (data loss prevention) and logging |
| Highly regulated | Legal hold, critical records, high-risk data | Dedicated controls, explicit approvals, strict retention |

## Compliance control model

1. Classify data before agent access is granted.
2. Map each agent capability to allowed data zones.
3. Apply DLP (data loss prevention) and exfiltration protections to prompt and response pathways.
4. Record exceptions with expiry and accountable owner.
5. Retain evidence for policy, user, and runtime decisions.

## Required evidence records

- Agent identifier, owner, and lifecycle state.
- Authorized data sources and prohibited destinations.
- Policy decisions, overrides, and justification.
- Prompt and response handling metadata where permitted by policy.
- Incident and remediation linkage for any control violation.

## Common compliance risks

- Copying enterprise prompts to unmanaged external tools.
- Silent expansion of agent access to new data sources.
- Missing retention and legal process integration.
- Policy exceptions that never expire.

## Business example

> A compliance team allows an internal knowledge assistant to use internal and
> sensitive zones but blocks highly regulated data. It enables DLP (data loss prevention) controls for
> prompt and response channels and requires compliance-owner sign-off before any
> zone expansion. The policy model allows productivity gains without violating data
> residency and audit requirements.