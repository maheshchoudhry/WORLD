# Volume 13 - Human Approval Model

| Field | Value |
|---|---|
| Document ID | WORLD-VOL13-018 |
| Title | Human Approval Model |
| Version | 1.0 |
| Status | Approved |
| Classification | Internal |
| Founder | Mahesh Choudhary |

## Purpose

This chapter defines how humans stay in control of consequential agent actions in Project WORLD. Agents are capable and autonomous, but autonomy without human oversight is unacceptable for actions that move money, change records of consequence, or affect people and reputation. The human approval model is the mandatory control that requires a human to authorize such actions before they take effect. This chapter establishes approval thresholds, the request-and-decision flow, escalation, and the audit trail that make human-in-the-loop enforceable and provable rather than aspirational.

## Scope

The chapter covers the classification of actions by consequence, approval thresholds and who may approve at each level, the approval request and decision flow, escalation and timeout handling, and the audit record of every decision. It aligns directly with the human-in-the-loop governance of Volume 03 (Section G) and is invoked by orchestration (Chapter 16) and collaboration (Chapters 17 and 19) whenever an agent proposes a consequential action. It does not define the business policies themselves, which are owned by governance.

## Concept

From first principles, an autonomous agent should be trusted in proportion to the reversibility and impact of its actions. Reading data or drafting a document is low-consequence and safely automated; issuing a payment, signing a contract, or deleting production data is high-consequence and must not proceed on an agent's authority alone. WORLD therefore classifies every action by consequence and attaches an approval threshold: below the threshold the agent acts autonomously, at or above it the agent must pause and obtain explicit human authorization. Approval is not a courtesy notification after the fact; it is a hard gate that blocks the action until a human with the right authority decides. This makes human control a structural property of the platform rather than a matter of trust in the agent.

## Architecture

When an agent reaches a gated action, it does not execute. It raises an approval request to the appropriate human authority and blocks until a decision is returned. Every step is recorded to the immutable audit store.

```mermaid
sequenceDiagram
    participant AG as Agent
    participant GATE as Approval Gate
    participant AUD as Audit Store
    participant H as Human Approver
    AG->>GATE: Propose consequential action
    GATE->>AUD: Record request
    GATE->>GATE: Classify consequence and threshold
    GATE->>H: Request approval with context and rationale
    alt Approved
        H->>GATE: Approve
        GATE->>AUD: Record decision
        GATE->>AG: Authorize execution
    else Rejected or Timeout
        H->>GATE: Reject (or no response)
        GATE->>AUD: Record decision
        GATE->>AG: Deny; escalate if required
    end
```

Because the gate sits on the execution path, the action is physically unable to proceed without a recorded human decision. The approver receives full context - what the agent proposes, why, and the expected impact - so the decision is informed rather than a rubber stamp.

**Enterprise example:** The Finance Agent prepares a supplier payment of a size that exceeds the auto-approval threshold. It halts and raises an approval request to the finance controller, attaching the invoice, the payment amount, the budget line, and its rationale. The controller reviews and approves; the gate records the decision with identity and timestamp, and only then does the agent execute the payment. Had the amount exceeded a higher threshold, the request would have escalated to the CFO. Had no one responded within the deadline, the action would have expired unexecuted and been escalated for attention.

## Key Components

| Component | Responsibility |
|---|---|
| Consequence Classifier | Scores each proposed action by impact and reversibility |
| Approval Threshold Policy | Maps consequence levels to required approver authority |
| Approval Gate | Blocks the action until an authorized decision is recorded |
| Escalation Handler | Routes to higher authority on high impact, rejection, or timeout |
| Approval Audit Record | Immutable log of request, context, approver identity, decision, and time |
| Human Approver Interface | Presents context and rationale so the decision is informed |

## Relationship to Other Layers

This model is the agent-layer enforcement of the human-in-the-loop governance defined in Volume 03 (Section G); that volume sets the principle, and this chapter makes it a hard runtime gate. Approval requests and decisions travel over the communication substrate of Chapter 15 and the Volume 10 messaging and event bus. Approver identity, authority, and the immutability of the audit record are guaranteed by the security architecture of Volume 12, so no agent can approve its own action and no decision can be altered after the fact. Orchestration (Chapter 16) and multi-agent collaboration (Chapter 19) invoke the gate whenever a workflow proposes a consequential action.

## Trade-offs and Considerations

Approval gates trade speed for control; every gate adds human latency, so thresholds are tuned to gate only genuinely consequential actions and to keep low-risk work fully automated. Setting thresholds too low causes approval fatigue and rubber-stamping, which erodes the control it is meant to provide; setting them too high concedes safety, so thresholds are governed, reviewed, and adjusted with evidence. Timeouts must fail safe - an unanswered request must never default to execution - which can stall work but is the correct bias for consequential actions. Rich decision context improves judgment but must avoid overwhelming approvers, so requests present impact and rationale concisely. The audit and escalation machinery adds overhead, accepted deliberately because provable human control is foundational to trusting an autonomous platform.

## Cross-References

- [Agent Orchestration](/docs/blueprint/volume-13-ai-agents/section-d-collaboration-and-control/16-agent-orchestration.md)
- [Multi-Agent Collaboration](/docs/blueprint/volume-13-ai-agents/section-d-collaboration-and-control/19-multi-agent-collaboration.md)
- [Volume 03 - AI Business Partner](/docs/blueprint/volume-03-ai-business-partner/README.md)
- [Volume 12 - Security](/docs/blueprint/volume-12-security/README.md)

## References

- [Volume 01 - Vision and Philosophy](/docs/blueprint/volume-01-vision-and-philosophy/README.md)
- [Document Standards](/docs/governance/document-standards.md)

## Change Log

| Version | Date | Author | Notes |
|---|---|---|---|
| 1.0 | 2026-07-12 | Lead Software Engineer | Initial approved version. |
