# Agent365 Data Security and Purview

Atlanta, USA

[![GitHub](https://img.shields.io/badge/--181717?logo=github&logoColor=ffffff)](https://github.com/)
[Cloud2BR OSS - Learning Hub](https://github.com/Cloud2BR-MSFTLearningHub)

Last updated: 2026-08-04

----------

<details markdown>
<summary>References</summary>

- [Use Microsoft Purview for Agent365](https://learn.microsoft.com/en-us/purview/ai-agent-365)
- [Microsoft Purview for AI (artificial intelligence)](https://learn.microsoft.com/en-us/purview/ai-microsoft-purview)
- [Microsoft Agent 365 overview](https://learn.microsoft.com/en-us/microsoft-agent-365/overview)

</details>

## Data security objective

Protect sensitive information in prompt, grounding, tool, and response flows with
policy-driven controls that remain auditable at enterprise scale.

## Purview-aligned controls

| Control | Implementation focus |
| --- | --- |
| Classification | Label sensitive content and map to data zones |
| Data loss prevention (DLP (data loss prevention)) | Detect and block risky sharing and exfiltration |
| Insider and communication risk | Correlate risky user and interaction patterns |
| Records and retention | Preserve evidence for compliance and investigation |
| eDiscovery support | Enable traceable investigation workflows |

## Agent365 data control blueprint

1. Classify and label core enterprise data stores before broad onboarding.
2. Apply DLP (data loss prevention) controls to high-risk prompt and output channels.
3. Restrict unmanaged external transfer paths.
4. Create policy exception process with explicit expiry and owner.
5. Validate retention and eDiscovery alignment for critical workflows.

## Validation checklist

- [ ] Sensitive-data labels are applied and testable in target workloads.
- [ ] DLP (data loss prevention) rules cover prompt and response pathways for high-risk scenarios.
- [ ] Exception approvals are logged with expiry and review owner.
- [ ] Data-residency and retention requirements are documented by region.

## Business example

> A healthcare operations agent drafts internal summaries from sensitive records.
> Purview labels and DLP (data loss prevention) controls prevent external sharing, while retention and
> audit policies preserve interaction evidence for compliance review.