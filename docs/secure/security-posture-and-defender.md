# Agent365 Security Posture and Defender

Atlanta, USA

[![GitHub](https://img.shields.io/badge/--181717?logo=github&logoColor=ffffff)](https://github.com/)
[Cloud2BR OSS - Learning Hub](https://github.com/Cloud2BR-MSFTLearningHub)

Last updated: 2026-08-04

----------

<details markdown>
<summary>References</summary>

- [Secure AI (artificial intelligence) agents at scale](https://learn.microsoft.com/en-us/security/security-for-ai/agent-365-security)
- [Defender Security for AI (artificial intelligence)](https://learn.microsoft.com/en-us/defender-xdr/security-for-ai/defender-security-for-ai)
- [Detect, protect, and investigate agent threats](https://learn.microsoft.com/en-us/defender-xdr/security-for-ai/ai-agent-detection-protection)

</details>

## Security objective

Continuously reduce identity abuse, unsafe behavior, and malicious activity across
agent execution paths while preserving productivity.

![Secure capability icon from Microsoft Agent 365 documentation](https://learn.microsoft.com/en-us/microsoft-agent-365/media/hub/secure.png)

*Source: [Microsoft Agent 365 documentation](https://learn.microsoft.com/en-us/microsoft-agent-365/).* 

## Threat model dimensions

| Dimension | Questions to answer |
| --- | --- |
| Identity abuse | Can agent identities be misused for unauthorized actions? |
| Data misuse | Can prompts or outputs leak sensitive content? |
| Tool exploitation | Can tool calls execute harmful or out-of-policy actions? |
| Supply-chain risk | Are dependencies and connectors trusted and monitored? |
| Runtime manipulation | Can prompt injection or chaining bypass safeguards? |

## Defender-aligned controls

1. Baseline discovery of all active agents and associated risk signals.
2. Continuous monitoring for suspicious behavior and anomalous tool activity.
3. Alert triage playbooks that map to accountable owners.
4. Automated containment paths for high-confidence detections.
5. Post-incident hardening feedback into governance policy.

## Security scorecard

| Control area | Example indicator |
| --- | --- |
| Identity hardening | Privileged identity exposure trend |
| Runtime safety | Policy-block success rate |
| Threat detection | Mean time to detect and triage |
| Containment | Mean time to contain high-severity event |
| Hardening | Recurrence rate after remediation |

## Business example

> A runtime detection identifies an unusual sequence of tool requests by a normally
> low-impact agent. Security operations isolate the agent, revoke tool tokens,
> review prompts and telemetry, and update policy templates to block the pattern
> before restoring service.