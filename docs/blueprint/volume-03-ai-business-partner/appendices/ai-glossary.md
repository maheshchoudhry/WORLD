# Volume 03 - AI Glossary

| Field | Value |
|---|---|
| Document ID | WORLD-VOL03-A1 |
| Title | AI Glossary |
| Version | 1.0 |
| Status | Approved |
| Classification | Internal |
| Founder | Mahesh Choudhary |

## Purpose

This appendix provides a single, authoritative glossary of terms specific to the WORLD AI Business Partner. It ensures that every reader of Volume 03 shares a common understanding of the vocabulary used to describe the intelligence layer, its behaviours, and its supporting concepts. Definitions are written to be concise, unambiguous, and directly usable in day-to-day engineering, product, and operational work.

## Scope

The glossary covers terms that are meaningful within the context of the AI Business Partner and the intelligence layer of WORLD. It does not attempt to redefine general software engineering terminology. Where a term also carries a governance or naming implication, the reader should consult the AI Terminology appendix (WORLD-VOL03-A2) for approved usage. Terms are listed alphabetically for ease of reference.

## Glossary

| Term | Definition |
|---|---|
| Action | A discrete operation the AI Business Partner performs on behalf of a user, such as retrieving data, drafting a document, or invoking a business capability. |
| Advisor | A specialised persona of the AI Business Partner focused on providing recommendations and guidance in a specific business domain (for example, finance or operations). |
| Agentic Workflow | A multi-step sequence in which the AI Business Partner plans, executes, and reflects on actions to accomplish a goal, rather than responding to a single prompt. |
| Audit Trail | The immutable, timestamped record of AI reasoning, actions, data accessed, and approvals, retained for accountability and compliance. |
| Business Context Engine | The subsystem that assembles the relevant business state, entities, and history needed to ground the AI Business Partner's responses in the user's actual situation. |
| Business Question | A natural-language query from a user seeking insight, analysis, or a recommendation about their business. |
| Capability | A defined, reusable business function that the AI Business Partner can invoke, typically exposed through the intelligence layer with clear inputs, outputs, and permissions. |
| Clarification | A structured request the AI Business Partner issues when a user's intent, scope, or required inputs are ambiguous or incomplete. |
| Confidence | A qualified expression of how certain the AI Business Partner is about a statement or recommendation, communicated to help the user calibrate trust. |
| Decision Brief | A structured artifact summarising a decision, its context, options, evidence, risks, and a recommended course of action. |
| Decision Support | The class of AI behaviours that help a user reach a well-informed decision without removing the user's authority to decide. |
| Escalation | The act of routing a request, risk, or approval to a human or a higher-authority process when it exceeds the AI Business Partner's mandate. |
| Explainability | The property of an AI output being accompanied by an understandable account of how and why it was produced. |
| Grounding | The practice of anchoring AI responses in verifiable business data and authoritative sources rather than unsupported generation. |
| Guardrail | A constraint that limits the AI Business Partner's behaviour to keep outputs safe, permitted, and within policy. |
| Hallucination | A confident but unsupported or fabricated statement produced by an AI system; explicitly to be prevented through grounding and review. |
| Human-in-the-Loop | A design in which a human reviews, approves, or corrects AI output at defined points before it takes effect. |
| Human-Approval-Gate | A mandatory checkpoint where a qualified human must explicitly approve a proposed AI action before it is executed. |
| Intent | The interpreted goal behind a user's request, used to select the appropriate reasoning path and capabilities. |
| Intelligence Layer | The functional layer of WORLD that houses the AI Business Partner's reasoning, context, and decision-support capabilities. |
| Knowledge Source | An authoritative repository of information the AI Business Partner may draw upon, such as business records, documents, or defined reference data. |
| Least Privilege | The principle that the AI Business Partner is granted only the minimum permissions required to complete a task. |
| Mandate | The defined scope of authority within which the AI Business Partner may act autonomously. |
| Observability | The ability to monitor, trace, and inspect the AI Business Partner's behaviour, inputs, and outputs in production. |
| Options Comparison | A structured evaluation of alternative courses of action against consistent criteria to support a decision. |
| Permission | An explicit grant that authorises the AI Business Partner to access data or perform an action. |
| Persona | A configured role and tone the AI Business Partner adopts to serve a particular audience or function. |
| Prompt | The instruction and context supplied to the reasoning model to produce a response. |
| Provenance | The traceable origin of a piece of information used or produced by the AI Business Partner. |
| Reasoning Framework | The structured method the AI Business Partner uses to move from question and context to a grounded, explainable answer or recommendation. |
| Recommendation | A proposed course of action offered by the AI Business Partner, accompanied by rationale and supporting evidence. |
| Redaction | The removal or masking of sensitive information from AI inputs or outputs to protect privacy and security. |
| Retrieval | The act of fetching relevant grounding data from knowledge sources for use in a response. |
| Risk-Weighted Recommendation | A recommendation that explicitly incorporates the likelihood and impact of associated risks. |
| Safety | The property of AI outputs being free from harmful, non-compliant, or out-of-policy content and actions. |
| Separation of Duties | The control that prevents a single actor from both initiating and approving a sensitive action. |
| Traceability | The ability to link an AI output back to the specific data, reasoning, and approvals that produced it. |
| Trust Boundary | The demarcation between what the AI Business Partner may do autonomously and what requires human authority. |
| User Authority | The principle that the human user retains ultimate decision-making power over business outcomes. |

## Cross-References

- [Reasoning Framework](/docs/blueprint/volume-03-ai-business-partner/chapters/reasoning-framework.md)
- [Business Context Engine](/docs/blueprint/volume-03-ai-business-partner/chapters/business-context-engine.md)
- [Decision Support](/docs/blueprint/volume-03-ai-business-partner/chapters/decision-support.md)

## References

- [Volume 01 - Vision and Philosophy](/docs/blueprint/volume-01-vision-and-philosophy/README.md)
- [Document Standards](/docs/governance/document-standards.md)

## Change Log

| Version | Date | Author | Notes |
|---|---|---|---|
| 1.0 | 2026-07-12 | Lead Software Engineer | Initial approved version. |
