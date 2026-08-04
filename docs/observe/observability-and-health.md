# Agent365 Observability and Agent Health

Atlanta, USA

[![GitHub](https://img.shields.io/badge/--181717?logo=github&logoColor=ffffff)](https://github.com/)
[Cloud2BR OSS - Learning Hub](https://github.com/Cloud2BR-MSFTLearningHub)

Last updated: 2026-08-04

----------

<details markdown>
<summary>References</summary>

- [Microsoft Agent 365 overview](https://learn.microsoft.com/en-us/microsoft-agent-365/overview)
- [Microsoft Agent 365 developer and observability docs](https://learn.microsoft.com/en-us/microsoft-agent-365/developer/)
- [Microsoft 365 Copilot architecture](https://learn.microsoft.com/en-us/microsoft-365/copilot/microsoft-365-copilot-architecture)

</details>

## Observability objectives

Observability must cover reliability, quality, security, and governance in a
single operating view, not separate dashboards with no correlation.

![Copilot query flow for prompt and response lifecycle visibility](https://learn.microsoft.com/en-us/microsoft-365/copilot/media/microsoft-365-copilot-architecture/copilot-query-flow.png)

*Source: [How Microsoft 365 Copilot works](https://learn.microsoft.com/en-us/microsoft-365/copilot/microsoft-365-copilot-architecture).* 

## Telemetry domains

| Domain | Example signals |
| --- | --- |
| Availability | Success rate, latency, timeout rate |
| Quality | Citation quality, fallback rate, retry rate |
| Safety | Policy blocks, restricted-content matches |
| Security | Risky session attempts, anomalous tool calls |
| Governance | Unapproved configuration drift, expired exceptions |

## Health model

1. Define service-level indicators (SLIs) by agent tier.
2. Set service-level objectives (SLOs) for user-critical journeys.
3. Attach alert thresholds to operational impact, not raw volume.
4. Route incidents by owner and risk tier.

## Health scorecard example

| Metric | Green | Amber | Red |
| --- | --- | --- | --- |
| End-to-end success rate | >= 99% | 97% to 98.9% | < 97% |
| P95 latency | <= 3s | 3s to 6s | > 6s |
| Policy violation rate | <= 0.1% | 0.1% to 0.5% | > 0.5% |
| Ownerless active agents | 0 | 1 to 2 | > 2 |

## Validation tests before production

- [ ] Prompt-response success under peak load.
- [ ] Tool invocation traceability by request identifier.
- [ ] Policy block and escalation workflow visibility.
- [ ] Evidence retention for regulated audit scenarios.

## Business example

> A high-volume support agent appears healthy by uptime but fails quality checks.
> Observability reveals high fallback and tool timeout rates during peak periods.
> The team scales dependencies, updates timeout strategy, and improves response
> quality while preserving security and governance controls.