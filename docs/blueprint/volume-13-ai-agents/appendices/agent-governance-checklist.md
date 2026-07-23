# Volume 13 - Agent Governance Checklist

| Field | Value |
|---|---|
| Document ID | WORLD-VOL13-A6 |
| Title | Agent Governance Checklist |
| Version | 1.0 |
| Status | Approved |
| Classification | Internal |
| Founder | Mahesh Choudhary |

## Purpose

This appendix provides the operational checklists that govern the introduction and operation of an agent in Project WORLD. Its purpose is to make governance repeatable and auditable: rather than relying on judgement alone, every agent passes through the same explicit gates for onboarding, safety review, and go-live. A checklist turns the principles of agent governance (Chapter 31) into concrete, verifiable steps that a reviewer signs off, leaving a record that the checks were performed.

## Scope

The document contains three checklists - agent onboarding, safety review, and go-live - each a set of verifiable items. They apply to every new agent and to any material change to an existing agent. The checklists operationalize agent governance (Chapter 31), the human approval model (Chapter 18), and agent performance (Chapter 32); they do not replace those chapters' definitions. Completion is recorded and retained as governance evidence.

## Onboarding Checklist

- [ ] Agent defined against the ten-field template (Appendix A4).
- [ ] Responsibilities and capabilities approved by the domain owner.
- [ ] Agent identity provisioned under Volume 12 controls.
- [ ] Permissions scoped to least privilege (Chapter 07).
- [ ] Tools bound and each tool's risk level confirmed (Appendix A5).
- [ ] Knowledge sources registered and access authorized.
- [ ] Decision authority and default autonomy level set (Chapter 33).
- [ ] Human approval requirements defined for consequential actions.
- [ ] Agent registered in the Agent Registry (Chapter 05).

## Safety Review Checklist

- [ ] Guardrails configured with ceilings, scopes, and rate caps (Chapter 31).
- [ ] Human approval gates verified on every high-risk action.
- [ ] Kill-switch tested for the agent and its class.
- [ ] Audit trail confirmed to capture all decisions and actions immutably.
- [ ] Prompt-injection and misuse scenarios reviewed against guardrails.
- [ ] Data boundaries verified - agent cannot access out-of-domain data.
- [ ] Separation enforced - agent cannot approve its own actions.
- [ ] Offline evaluation passed against curated datasets (Chapter 32).
- [ ] Failure and timeout behaviour confirmed to fail safe.

## Go-Live Checklist

- [ ] Governance review board approval recorded.
- [ ] Online evaluation and monitoring dashboards active (Chapter 32).
- [ ] Cost accounting attributing usage to the agent.
- [ ] Rollback and demotion path verified (Chapter 33).
- [ ] On-call ownership and escalation contacts assigned.
- [ ] Initial autonomy level set conservatively pending evidence.
- [ ] Change logged and communicated to affected owners.
- [ ] Post-launch review scheduled against KPI thresholds.

## Cross-References

- [Agent Governance](/docs/blueprint/volume-13-ai-agents/section-g-governance-and-evolution/31-agent-governance.md)
- [Agent Performance](/docs/blueprint/volume-13-ai-agents/section-g-governance-and-evolution/32-agent-performance.md)
- [Future Agent Evolution](/docs/blueprint/volume-13-ai-agents/section-g-governance-and-evolution/33-future-agent-evolution.md)
- [Agent Definition Template](/docs/blueprint/volume-13-ai-agents/appendices/agent-definition-template.md)

## References

- [Volume 01 - Vision and Philosophy](/docs/blueprint/volume-01-vision-and-philosophy/README.md)
- [Document Standards](/docs/governance/document-standards.md)

## Change Log

| Version | Date | Author | Notes |
|---|---|---|---|
| 1.0 | 2026-07-12 | Lead Software Engineer | Initial approved version. |
