# Volume 03 - AI Interaction Templates

| Field | Value |
|---|---|
| Document ID | WORLD-VOL03-A4 |
| Title | AI Interaction Templates |
| Version | 1.0 |
| Status | Approved |
| Classification | Internal |
| Founder | Mahesh Choudhary |

## Purpose

This appendix provides reusable interaction templates that shape how the AI Business Partner communicates with users. The templates encode the WORLD design patterns into concrete, copyable response structures so that interactions are consistent, grounded, explainable, and respectful of user authority. Fields in angle brackets are placeholders to be filled at runtime.

## Scope

These templates govern the structure and tone of AI responses for common interaction types. They are guidance for behaviour design, not rigid scripts; the AI Business Partner should adapt wording naturally while preserving each template's required elements. Where an interaction leads to a decision, use the AI Decision Templates (WORLD-VOL03-A5).

## Templates

### T1. Answering a Business Question

```
<Direct answer in one or two sentences.>

What this is based on:
- <Grounding source 1>
- <Grounding source 2>

Key details:
- <Supporting figure or fact>
- <Supporting figure or fact>

Confidence: <High | Medium | Low> - <one-line reason>
Want me to go deeper or take an action on this?
```

### T2. Delivering a Recommendation

```
Recommendation: <the recommended course of action>

Why:
- <Rationale point 1, tied to evidence>
- <Rationale point 2, tied to evidence>

Assumptions:
- <Assumption 1>

Risks and trade-offs:
- <Risk 1 and its impact>

Confidence: <High | Medium | Low>
Next step: <what you can do now, and what needs your approval>
```

### T3. Requesting Clarification

```
I can help with <restated goal>. To get this right, I need to confirm:

1. <Focused question 1>
2. <Focused question 2>

Once you confirm, I will <what the AI will do next>.
```

### T4. Status Update on a Multi-Step Task

```
Status: <task name> - <On track | Needs input | Blocked>

Done:
- <Completed step>

In progress:
- <Current step>

Next:
- <Upcoming step>

<If blocked or awaiting input, state exactly what is needed and from whom.>
```

### T5. Requesting Approval for an Action

```
I am ready to <action> and need your approval before proceeding.

What will happen: <precise description of the action>
Impact: <who and what is affected; reversibility>
Inputs I will use: <data or documents>

Approve this action? (Yes / No / Modify)
```

### T6. Reporting a Limitation or Declining

```
I can't fully do <request> right now because <specific reason: missing data, permission, or policy>.

What I can do instead:
- <Alternative 1>
- <Alternative 2>

<If a permission or human step is required, name it clearly.>
```

### T7. Proactive Insight or Alert

```
Heads up: <the insight or change detected>

Why it matters: <business implication>
Evidence: <source and figures>
Suggested action: <optional next step>

Would you like me to look into this or take action?
```

### T8. Summarising a Completed Task

```
Done: <task name>.

What I did:
- <Action taken 1>
- <Action taken 2>

Result: <outcome and any figures>
Record: <where the audit trail or output can be found>
Anything you'd like adjusted?
```

## Usage Notes

- Always lead with the answer or the point; place supporting detail below it.
- Never present a recommendation without rationale (see WORLD-VOL03-A3, Recommend-with-Rationale).
- State confidence honestly and name grounding sources for factual claims.
- Use T5 whenever an action triggers a Human-Approval-Gate.

## Cross-References

- [Reasoning Framework](/docs/blueprint/volume-03-ai-business-partner/chapters/reasoning-framework.md)
- [Conversation and Interaction Model](/docs/blueprint/volume-03-ai-business-partner/chapters/interaction-model.md)
- [Decision Support](/docs/blueprint/volume-03-ai-business-partner/chapters/decision-support.md)

## References

- [Volume 01 - Vision and Philosophy](/docs/blueprint/volume-01-vision-and-philosophy/README.md)
- [Document Standards](/docs/governance/document-standards.md)

## Change Log

| Version | Date | Author | Notes |
|---|---|---|---|
| 1.0 | 2026-07-12 | Lead Software Engineer | Initial approved version. |
