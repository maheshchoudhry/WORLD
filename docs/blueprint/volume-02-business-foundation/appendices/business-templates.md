# Volume 02 - Business Templates

| Field | Value |
|---|---|
| Document ID | WORLD-VOL02-A3 |
| Title | Business Templates |
| Version | 1.0 |
| Status | Approved |
| Classification | Internal |
| Founder | Mahesh Choudhary |

## Purpose

This appendix provides ready-to-use Markdown templates for the recurring business artifacts referenced across Volume 02. Each template is complete and directly reusable: copy it, fill in the bracketed fields, and produce a consistent, professional document without starting from scratch.

## Scope

The templates cover general-purpose business artifacts - planning, procedure, decision, responsibility, review, and risk. They are format-neutral and apply to any function. Fill placeholders enclosed in angle brackets (`< >`) with real content before use.

## Template 1 - Business Plan Outline

```markdown
# Business Plan - <Business or Initiative Name>

## 1. Executive Summary
<One paragraph: what the business does, for whom, and why it will succeed.>

## 2. Problem and Opportunity
<The customer problem and the size and nature of the opportunity.>

## 3. Value Proposition
<The specific benefits delivered and why they matter to the target customer.>

## 4. Target Market and Customer Segments
<Who the customers are, their needs, and segment sizes.>

## 5. Business Model
<How value is created, delivered, and captured; primary revenue streams.>

## 6. Go-To-Market Strategy
<Channels, positioning, pricing, and acquisition approach.>

## 7. Operations Plan
<Key processes, resources, suppliers, and capabilities required.>

## 8. Financial Plan
<Revenue projections, cost structure, and funding requirements.>

## 9. Risks and Mitigations
<Top risks with likelihood, impact, and planned response.>

## 10. Milestones and Roadmap
<Key milestones with target dates and success criteria.>
```

## Template 2 - Standard Operating Procedure (SOP)

```markdown
# SOP - <Procedure Name>

| Field | Value |
|---|---|
| SOP ID | <ID> |
| Owner | <Role> |
| Version | <n.n> |
| Effective Date | <YYYY-MM-DD> |
| Review Cycle | <e.g. Annual> |

## Purpose
<Why this procedure exists and the outcome it ensures.>

## Scope
<Where, when, and to whom this procedure applies.>

## Roles and Responsibilities
<Who performs and who approves each part.>

## Prerequisites
<Inputs, access, tools, or conditions required before starting.>

## Procedure
1. <Step one - action and expected result.>
2. <Step two.>
3. <Step three.>

## Exceptions and Escalation
<How to handle deviations and whom to escalate to.>

## Records
<What evidence is produced and where it is stored.>
```

## Template 3 - Decision Record

```markdown
# Decision Record - <Short Decision Title>

| Field | Value |
|---|---|
| Decision ID | <ID> |
| Date | <YYYY-MM-DD> |
| Decision Owner | <Name / Role> |
| Status | <Proposed / Accepted / Superseded> |

## Context
<The situation and forces that make a decision necessary.>

## Options Considered
1. <Option A - summary, pros, cons.>
2. <Option B - summary, pros, cons.>
3. <Option C - summary, pros, cons.>

## Decision
<The option chosen and the primary rationale.>

## Consequences
<Expected outcomes, trade-offs accepted, and follow-up actions.>
```

## Template 4 - RACI Responsibility Matrix

```markdown
| Activity / Deliverable | <Role 1> | <Role 2> | <Role 3> | <Role 4> |
|---|---|---|---|---|
| <Activity 1> | R | A | C | I |
| <Activity 2> | A | R | I | C |
| <Activity 3> | C | A | R | I |
```

_Legend: R = Responsible, A = Accountable, C = Consulted, I = Informed. Each activity has exactly one A._

## Template 5 - Meeting / Review Template

```markdown
# <Meeting Name> - <YYYY-MM-DD>

| Field | Value |
|---|---|
| Facilitator | <Name> |
| Attendees | <Names> |
| Objective | <The single outcome this meeting must achieve.> |

## Agenda
1. <Topic - owner - time box>
2. <Topic - owner - time box>

## Discussion Notes
<Key points, data reviewed, and context.>

## Decisions
- <Decision made and rationale.>

## Action Items
| Action | Owner | Due Date | Status |
|---|---|---|---|
| <Action> | <Name> | <YYYY-MM-DD> | Open |
```

## Template 6 - Risk Register Row

```markdown
| Risk ID | Risk Description | Category | Likelihood (1-5) | Impact (1-5) | Score | Owner | Mitigation | Status |
|---|---|---|---|---|---|---|---|---|
| <R-001> | <What could go wrong and its cause.> | <Operational> | <3> | <4> | <12> | <Name> | <Planned response.> | <Open> |
```

_Score = Likelihood x Impact. Prioritize risks with the highest scores for active management._

## Related Documents

- [Volume 02 - Business Foundation Overview](/docs/blueprint/volume-02-business-foundation/README.md)
- [Appendix A4 - Business Checklists](/docs/blueprint/volume-02-business-foundation/appendices/business-checklists.md)
- [Appendix A5 - Business Assessment Framework](/docs/blueprint/volume-02-business-foundation/appendices/business-assessment-framework.md)

## References

- [Volume 01 - Vision and Philosophy](/docs/blueprint/volume-01-vision-and-philosophy/README.md)
- [Document Standards](/docs/governance/document-standards.md)

## Change Log

| Version | Date | Author | Notes |
|---|---|---|---|
| 1.0 | 2026-07-12 | Lead Software Engineer | Initial approved version. |
