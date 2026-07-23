# Volume 13 - Tool Catalog

| Field | Value |
|---|---|
| Document ID | WORLD-VOL13-A5 |
| Title | Tool Catalog |
| Version | 1.0 |
| Status | Approved |
| Classification | Internal |
| Founder | Mahesh Choudhary |

## Purpose

This appendix catalogs the representative tools that agents in Project WORLD may invoke through tool calling. Its purpose is to make the agents' means of acting explicit and governable: every tool an agent can use is a channel through which it affects the world, so each must have a stated purpose, a defined interface, an assessed risk level, and a clear rule on whether its use requires human approval. A central tool catalog lets governance reason about the fleet's total capability and the blast radius of each tool.

## Scope

The catalog lists representative tools across data access, communication, execution, and financial domains, with purpose, inputs and outputs, risk level, and approval requirement. It is representative rather than exhaustive; the authoritative binding of tools to a specific agent lives in that agent's definition (Appendix A4 template, Sections E and F). Risk levels and approval rules align with agent governance (Chapter 31) and the human approval model (Chapter 18). Tool implementation and the API contracts themselves are governed by Volume 10.

## Tool Catalog

| Tool | Purpose | Inputs / Outputs | Risk Level | Approval Required |
|---|---|---|---|---|
| Knowledge Retrieval | Retrieve grounded evidence from a knowledge source | Query / ranked passages | Low | No |
| Ledger Query | Read financial records for analysis and reconciliation | Account or filter / records | Low | No |
| Record Read | Read business records from the ERP | Entity and filter / record set | Low | No |
| Report Generation | Produce a report or summary artifact | Data and template / document | Low | No |
| Notification Send | Send an informational message to a user or channel | Recipient and message / delivery receipt | Medium | No |
| Record Update | Modify a non-consequential business record | Entity and changes / updated record | Medium | Conditional - above scope |
| Ticket / Task Create | Open a work item for a human or agent | Task detail / created item | Medium | No |
| Code Change Proposal | Propose a code change for review | Diff and rationale / pull request | Medium | Yes - merge requires approval |
| Payment Execution | Execute a supplier or expense payment | Payee, amount, reference / confirmation | High | Yes - above ceiling |
| Data Deletion | Delete a business record | Entity reference / deletion result | High | Yes |
| Access Grant | Grant or change a permission | Subject, resource, scope / grant record | High | Yes |
| Security Containment | Isolate a compromised resource | Target and scope / containment result | High | Conditional - beyond containment |

## Notes on Risk and Approval

Risk level reflects the reversibility and impact of a tool's effect: low-risk tools read or draft and are safely autonomous; medium-risk tools make bounded, recoverable changes; high-risk tools move money, remove data, change access, or contain systems and therefore gate for human approval by default. "Conditional" means approval depends on scope - the guardrail enforcer (Chapter 31) evaluates the specific arguments against the agent's ceilings and escalates when they are exceeded. Every tool invocation, approved or autonomous, is recorded to the audit trail.

## Cross-References

- [Tool Calling](/docs/blueprint/volume-13-ai-agents/section-c-agent-cognition/09-tool-calling.md)
- [Agent Governance](/docs/blueprint/volume-13-ai-agents/section-g-governance-and-evolution/31-agent-governance.md)
- [Human Approval Model](/docs/blueprint/volume-13-ai-agents/section-d-collaboration-and-control/18-human-approval-model.md)
- [Agent Definition Template](/docs/blueprint/volume-13-ai-agents/appendices/agent-definition-template.md)

## References

- [Volume 01 - Vision and Philosophy](/docs/blueprint/volume-01-vision-and-philosophy/README.md)
- [Document Standards](/docs/governance/document-standards.md)

## Change Log

| Version | Date | Author | Notes |
|---|---|---|---|
| 1.0 | 2026-07-12 | Lead Software Engineer | Initial approved version. |
