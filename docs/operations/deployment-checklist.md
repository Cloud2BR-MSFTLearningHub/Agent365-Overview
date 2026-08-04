# Agent365 Deployment Checklist

Atlanta, USA

[![GitHub](https://img.shields.io/badge/--181717?logo=github&logoColor=ffffff)](https://github.com/)
[Cloud2BR OSS - Learning Hub](https://github.com/Cloud2BR-MSFTLearningHub)

Last updated: 2026-08-04

----------

## Foundation readiness

- [ ] Business objective, owner, and support model are documented.
- [ ] Agent registration metadata is complete.
- [ ] Identity model and least-privilege permissions are approved.
- [ ] Data sources, destinations, and zone restrictions are approved.

## Governance readiness

- [ ] Risk tier is assigned and approval lane is complete.
- [ ] Lifecycle state and decommission path are documented.
- [ ] Exceptions are approved with expiry date and accountable owner.
- [ ] Tooling and MCP integrations are reviewed and logged.

## Security and compliance readiness

- [ ] Monitoring and alerting are configured for runtime behavior.
- [ ] Data loss prevention (DLP) and sensitive-data controls are validated.
- [ ] Incident response workflow and escalation matrix are confirmed.
- [ ] Retention and audit evidence requirements are implemented.

## Operational readiness

- [ ] Service-level objectives and error budgets are defined.
- [ ] Runbook and on-call ownership are published.
- [ ] Rollback plan is tested and time-bounded.
- [ ] KPI baseline is captured for post-go-live comparison.

## Go-live gates

1. Pilot results meet reliability and policy thresholds.
2. No unresolved high-risk security findings remain.
3. Business owner and security owner approve production release.
4. First-week hypercare staffing and review cadence are confirmed.

## First 14 days after release

- Day 1 to 3: monitor latency, failure modes, and policy blocks.
- Day 4 to 7: review user feedback and correctness drift.
- Day 8 to 14: tune policies, finalize known-issue playbook, and confirm stable KPI trend.