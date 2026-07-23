# Volume 13 - Agent Catalog

| Field | Value |
|---|---|
| Document ID | WORLD-VOL13-A3 |
| Title | Agent Catalog |
| Version | 1.0 |
| Status | Approved |
| Classification | Internal |
| Founder | Mahesh Choudhary |

## Purpose

This appendix is the consolidated catalog of every agent defined in Volume 13. Its purpose is to give a single, at-a-glance view of the agent fleet: what each agent is, which type it belongs to, the domain it serves, the authority it holds, and the level of human approval its consequential actions require. A central catalog lets governance reason about the fleet as a whole - coverage, overlap, and the distribution of authority - rather than agent by agent.

## Scope

The catalog lists the core agents of Section E and the specialist agents of Section F, with their type, primary domain, decision authority, and human-approval level. The decision-authority and approval columns summarize each agent's own chapter and the human approval model (Chapter 18); the authoritative definition remains in the agent's chapter. The catalog does not define the agents' internals, which their chapters cover, nor the tools they use, which the Tool Catalog (Appendix A5) covers.

## Agent Catalog

| Agent | Type | Primary Domain | Decision Authority | Human-Approval Level |
|---|---|---|---|---|
| Supervisor Agent | Core | Fleet routing and coordination | Routes and delegates work; no direct business mutations | Low - approval only for cross-domain escalations |
| Executive Agents | Core | Strategy and cross-functional oversight | Synthesizes and recommends; proposes consequential decisions | High - executive-level actions require human authorization |
| Department Agents | Core | Departmental operations (e.g. HR, sales) | Executes routine departmental actions within ceilings | Medium - above-ceiling actions require approval |
| Industry Agents | Core | Industry-specific workflows | Applies industry logic within a bounded scope | Medium - regulated actions require approval |
| Security Agent | Specialist | Security monitoring and response | Detects, contains, and recommends; limited autonomous containment | High - remediation beyond containment requires approval |
| Finance Agent | Specialist | Finance and payments | Executes financial actions within value ceilings | High - payments above ceiling require approval |
| Operations Agent | Specialist | Supply, inventory, logistics | Places routine operational actions within limits | Medium - above-limit actions require approval |
| Research Agent | Specialist | Information gathering and analysis | Retrieves, synthesizes, and reports; no business mutations | Low - read and report only |
| Coding Agent | Specialist | Software development | Writes and proposes code changes | Medium - merge and deploy require approval |
| QA Agent | Specialist | Quality assurance and testing | Runs and evaluates tests; flags defects | Low - reports; release gating requires approval |
| Monitoring Agent | Specialist | Observability and alerting | Observes, alerts, and recommends | Low - alerts; corrective action requires approval |

## Notes on the Catalog

Type distinguishes core agents, which provide broad organizational function, from specialist agents, which serve a focused domain. Decision authority states what an agent may do unattended at its default autonomy level (Chapter 33); the level can be adjusted by governance. Human-approval level summarizes how often consequential actions require authorization under the human approval model: low agents chiefly read and report, medium agents act within ceilings, and high agents touch money, security remediation, or executive decisions and therefore gate frequently.

## Cross-References

- [Supervisor Agent](/docs/blueprint/volume-13-ai-agents/section-e-core-agents/20-supervisor-agent.md)
- [Human Approval Model](/docs/blueprint/volume-13-ai-agents/section-d-collaboration-and-control/18-human-approval-model.md)
- [Agent Definition Template](/docs/blueprint/volume-13-ai-agents/appendices/agent-definition-template.md)
- [Tool Catalog](/docs/blueprint/volume-13-ai-agents/appendices/tool-catalog.md)

## References

- [Volume 01 - Vision and Philosophy](/docs/blueprint/volume-01-vision-and-philosophy/README.md)
- [Document Standards](/docs/governance/document-standards.md)

## Change Log

| Version | Date | Author | Notes |
|---|---|---|---|
| 1.0 | 2026-07-12 | Lead Software Engineer | Initial approved version. |
