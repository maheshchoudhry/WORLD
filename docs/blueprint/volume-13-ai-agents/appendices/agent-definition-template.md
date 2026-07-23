# Volume 13 - Agent Definition Template

| Field | Value |
|---|---|
| Document ID | WORLD-VOL13-A4 |
| Title | Agent Definition Template |
| Version | 1.0 |
| Status | Approved |
| Classification | Internal |
| Founder | Mahesh Choudhary |

## Purpose

This appendix provides the reusable template every agent in Project WORLD is defined against. Its purpose is consistency and completeness: an agent is only safe to deploy when its responsibilities, capabilities, interfaces, authority, and boundaries are all explicitly stated and reviewable. The template forces every agent definition to answer the same questions in the same order, so governance can compare agents, spot gaps, and approve them against a uniform standard. Sections E and F of this volume are authored against this template.

## Scope

The document defines the ten mandatory fields of an agent definition and gives a fully worked sample. It specifies what each field must contain and why. It is the structural contract for agent chapters; it does not itself define any operational agent, and the authoritative instances live in Sections E and F. Field content must align with agent governance (Chapter 31), the human approval model (Chapter 18), and agent performance (Chapter 32).

## The Ten-Field Template

| # | Field | What It Must Contain |
|---|---|---|
| 1 | Responsibilities | The outcomes the agent is accountable for, stated as goals not tasks. |
| 2 | Capabilities | The discrete functions the agent can perform to meet its responsibilities. |
| 3 | Inputs | The data, events, and requests the agent consumes. |
| 4 | Outputs | The results, actions, and records the agent produces. |
| 5 | Tools | The governed tools the agent may invoke, by name and purpose. |
| 6 | Knowledge Sources | The authoritative sources the agent may retrieve from. |
| 7 | Decision Authority | The actions the agent may take unattended at its autonomy level. |
| 8 | Human Approval Requirements | The actions that require human authorization before executing. |
| 9 | KPIs | The metrics by which the agent's performance is judged. |
| 10 | Security Boundaries | The identity, permission, and data limits the agent cannot cross. |

## Filled Sample: Finance Agent

The following sample shows the template applied to a representative agent. It is illustrative; the authoritative Finance Agent definition is in Section F.

**1. Responsibilities.** Ensure supplier and expense payments are executed accurately, on time, and within budget and policy, and keep financial records reconciled.

**2. Capabilities.** Validate invoices against purchase orders; schedule and execute payments within ceilings; reconcile ledgers; flag anomalies; prepare payment approval requests.

**3. Inputs.** Approved invoices, purchase orders, budget lines, payment policies, and reconciliation data from the ERP.

**4. Outputs.** Executed payments below the ceiling, approval requests for payments above it, reconciliation entries, and anomaly reports - each written to the audit trail.

**5. Tools.** Payment execution API, invoice validation service, ledger query tool, and the approval request tool (see the Tool Catalog, Appendix A5).

**6. Knowledge Sources.** The finance module of the ERP, approved payment policy, supplier master data, and the current budget.

**7. Decision Authority.** May validate invoices and execute payments up to the governed per-payment ceiling and daily aggregate limit without human approval.

**8. Human Approval Requirements.** Any payment above the per-payment ceiling, any new supplier payee, and any action breaching the daily limit must be approved by the finance controller, escalating to the CFO above a higher threshold.

**9. KPIs.** Payment accuracy, on-time payment rate, reconciliation completeness, anomaly precision, and cost per processed payment.

**10. Security Boundaries.** Operates under its own agent identity; may access only finance-domain data; cannot approve its own payments; cannot alter the audit trail; all actions bounded by Volume 12 controls and Chapter 31 guardrails.

## Cross-References

- [Finance Agent](/docs/blueprint/volume-13-ai-agents/section-f-specialist-agents/25-finance-agent.md)
- [Agent Catalog](/docs/blueprint/volume-13-ai-agents/appendices/agent-catalog.md)
- [Human Approval Model](/docs/blueprint/volume-13-ai-agents/section-d-collaboration-and-control/18-human-approval-model.md)
- [Agent Governance](/docs/blueprint/volume-13-ai-agents/section-g-governance-and-evolution/31-agent-governance.md)

## References

- [Volume 01 - Vision and Philosophy](/docs/blueprint/volume-01-vision-and-philosophy/README.md)
- [Document Standards](/docs/governance/document-standards.md)

## Change Log

| Version | Date | Author | Notes |
|---|---|---|---|
| 1.0 | 2026-07-12 | Lead Software Engineer | Initial approved version. |
