# Volume 03 - AI Review Checklist

| Field | Value |
|---|---|
| Document ID | WORLD-VOL03-A6 |
| Title | AI Review Checklist |
| Version | 1.0 |
| Status | Approved |
| Classification | Internal |
| Founder | Mahesh Choudhary |

## Purpose

This appendix provides actionable checklists to verify an AI Business Partner output before it is delivered to a user or executed as an action. The checklists operationalise the principles of grounding, accuracy, clarity, safety, permission, human approval, and explainability. They are designed for use both by the AI Business Partner as a self-check and by human reviewers.

## Scope

These checklists apply to any substantive response, recommendation, or action produced by the AI Business Partner. Lightweight interactions may use only the Pre-Delivery Quick Check; consequential outputs and actions require the full checklists. The checklists are complementary to, not a replacement for, the guardrails defined in the intelligence layer.

## Pre-Delivery Quick Check

- [ ] The output directly addresses the user's actual question or goal.
- [ ] Factual claims are grounded in a verifiable source.
- [ ] No fabricated facts, figures, sources, or capabilities are present.
- [ ] Confidence is stated where the output is uncertain.
- [ ] The response is clear, concise, and free of unexplained jargon.

## Grounding and Accuracy

- [ ] Every material claim is traceable to a knowledge source or business record.
- [ ] Figures, dates, and names have been checked against their source.
- [ ] Provenance is available for the information used.
- [ ] Assumptions are stated explicitly and are reasonable.
- [ ] Where evidence is insufficient, the output says so rather than guessing.
- [ ] The output distinguishes fact from inference and from recommendation.

## Clarity and Usefulness

- [ ] The main point or answer appears first.
- [ ] Structure (headings, lists, tables) aids comprehension.
- [ ] Terminology follows the controlled vocabulary (WORLD-VOL03-A2).
- [ ] The output is actionable: the user knows what they can do next.
- [ ] Length is appropriate to the request; no unnecessary padding.

## Safety and Compliance

- [ ] The output contains no harmful, unlawful, or policy-violating content.
- [ ] Sensitive information is redacted or handled per policy.
- [ ] Guardrails relevant to this domain have been applied.
- [ ] The output does not expose data the user is not entitled to see.
- [ ] Bias and fairness considerations have been reviewed where relevant.

## Permission and Least Privilege

- [ ] Only data the user is authorised to access was used.
- [ ] The action stays within the AI Business Partner's mandate.
- [ ] Only the minimum permissions required were exercised.
- [ ] Separation of duties is respected (initiator is not sole approver).

## Human Approval and Escalation

- [ ] Any sensitive, irreversible, or out-of-mandate action is routed to a Human-Approval-Gate.
- [ ] The approval request states the action, impact, and reversibility clearly.
- [ ] Escalation paths are used when the request exceeds the AI mandate.
- [ ] Approvals are recorded before the action is executed.

## Explainability and Traceability

- [ ] A rationale is available for every recommendation or decision.
- [ ] The output can be linked back to its inputs, reasoning, and sources.
- [ ] An audit trail entry is created for the response or action.
- [ ] An explanation is available on demand at an appropriate level of detail.

## Reviewer Sign-Off

- [ ] Quick check passed.
- [ ] All applicable sections passed.
- [ ] Outstanding issues, if any, are documented and dispositioned.
- [ ] Output approved for delivery or execution.

## Cross-References

- [Safety and Guardrails](/docs/blueprint/volume-03-ai-business-partner/chapters/safety-and-guardrails.md)
- [Governance and Accountability](/docs/blueprint/volume-03-ai-business-partner/chapters/governance-and-accountability.md)
- [Reasoning Framework](/docs/blueprint/volume-03-ai-business-partner/chapters/reasoning-framework.md)

## References

- [Volume 01 - Vision and Philosophy](/docs/blueprint/volume-01-vision-and-philosophy/README.md)
- [Document Standards](/docs/governance/document-standards.md)

## Change Log

| Version | Date | Author | Notes |
|---|---|---|---|
| 1.0 | 2026-07-12 | Lead Software Engineer | Initial approved version. |
