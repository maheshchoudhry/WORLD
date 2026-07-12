# Volume 03 - AI Decision Templates

| Field | Value |
|---|---|
| Document ID | WORLD-VOL03-A5 |
| Title | AI Decision Templates |
| Version | 1.0 |
| Status | Approved |
| Classification | Internal |
| Founder | Mahesh Choudhary |

## Purpose

This appendix provides ready-to-use templates for decision support. They give the AI Business Partner a consistent structure for helping users make well-informed decisions while preserving user authority. Each template is designed to be grounded, explainable, and auditable, and to make risks and trade-offs explicit.

## Scope

These templates apply whenever the AI Business Partner supports a decision, from a quick go/no-go call to a structured evaluation of multiple options. They complement the interaction templates (WORLD-VOL03-A4): use those for general communication and these when the interaction centres on a decision. Placeholders in angle brackets are filled at runtime.

## Templates

### D1. Decision Brief

```
Decision: <the decision to be made, phrased as a question>
Owner: <who decides> | Date needed by: <date>

Context:
<2-4 sentences of grounded background and why this matters now.>

Options considered:
1. <Option A>
2. <Option B>
3. <Option C>

Evidence:
- <Fact / figure with source>
- <Fact / figure with source>

Key risks:
- <Risk and its impact>

Recommendation: <recommended option>
Rationale: <why, tied to evidence>
Confidence: <High | Medium | Low>
Approval required: <Yes / No - and from whom>
```

### D2. Options Comparison Table

```
Decision: <the decision>
Evaluation criteria and weights: <criterion (weight), ...>
```

| Criterion (weight) | Option A | Option B | Option C |
|---|---|---|---|
| <Cost> (<w>) | <score / note> | <score / note> | <score / note> |
| <Time to value> (<w>) | <score / note> | <score / note> | <score / note> |
| <Risk> (<w>) | <score / note> | <score / note> | <score / note> |
| <Strategic fit> (<w>) | <score / note> | <score / note> | <score / note> |
| **Weighted total** | **<total>** | **<total>** | **<total>** |

```
Leading option: <option> - <one-line justification>
```

### D3. Risk-Weighted Recommendation

```
Recommendation: <recommended action>

Expected benefit: <what success looks like, with figures if available>
```

| Risk | Likelihood (L/M/H) | Impact (L/M/H) | Mitigation |
|---|---|---|---|
| <Risk 1> | <L/M/H> | <L/M/H> | <mitigation> |
| <Risk 2> | <L/M/H> | <L/M/H> | <mitigation> |

```
Risk-adjusted view: <net assessment after weighing likelihood and impact>
Confidence: <High | Medium | Low>
Recommended safeguard: <condition, limit, or approval gate>
```

### D4. Go / No-Go

```
Decision point: <what is being gated>
Criteria for GO:
- [ ] <Criterion 1 met>
- [ ] <Criterion 2 met>
- [ ] <Criterion 3 met>

Assessment:
- <Criterion>: <met / not met - evidence>

Recommendation: <GO | NO-GO | GO with conditions>
Conditions (if any): <conditions>
Approval required: <who>
```

### D5. Trade-off Summary

```
We can optimise for <objective A> or <objective B>, but not both fully.

If we favour <A>: <consequence, who benefits, what we give up>
If we favour <B>: <consequence, who benefits, what we give up>

Balanced option: <middle path, if one exists>
Recommended balance: <choice> - <rationale>
```

### D6. Decision Record (Post-Decision)

```
Decision made: <what was decided>
Decided by: <person> on <date>
Options rejected: <options and brief reason>
Key rationale: <why>
Review date: <when this should be revisited>
Audit reference: <link or ID to the audit trail>
```

## Usage Notes

- Every recommendation must state its rationale and confidence.
- Make assumptions and risks explicit; do not bury uncertainty.
- Where a decision triggers an action, pair the relevant template with the Human-Approval-Gate pattern (WORLD-VOL03-A3).
- Preserve a Decision Record (D6) so decisions remain traceable.

## Cross-References

- [Decision Support](/docs/blueprint/volume-03-ai-business-partner/chapters/decision-support.md)
- [Reasoning Framework](/docs/blueprint/volume-03-ai-business-partner/chapters/reasoning-framework.md)
- [Governance and Accountability](/docs/blueprint/volume-03-ai-business-partner/chapters/governance-and-accountability.md)

## References

- [Volume 01 - Vision and Philosophy](/docs/blueprint/volume-01-vision-and-philosophy/README.md)
- [Document Standards](/docs/governance/document-standards.md)

## Change Log

| Version | Date | Author | Notes |
|---|---|---|---|
| 1.0 | 2026-07-12 | Lead Software Engineer | Initial approved version. |
