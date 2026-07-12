# Volume 03 - AI Terminology

| Field | Value |
|---|---|
| Document ID | WORLD-VOL03-A2 |
| Title | AI Terminology |
| Version | 1.0 |
| Status | Approved |
| Classification | Internal |
| Founder | Mahesh Choudhary |

## Purpose

This appendix establishes a controlled vocabulary for Volume 03. Whereas the AI Glossary (WORLD-VOL03-A1) defines what terms mean, this appendix governs how terms are used: which term is canonical, what it denotes, and which alternative terms must be avoided to preserve consistency. Consistent naming reduces ambiguity, improves searchability, and protects the integrity of the specification.

## Scope

This controlled vocabulary is binding for all Volume 03 documentation, product copy, and engineering artifacts that describe the AI Business Partner. It applies to author-facing naming decisions. When a term appears in this appendix, the preferred term must be used and the listed deprecated terms must not. Where a concept is not covered here, authors should follow the AI Glossary and the general document standards.

## Controlled Vocabulary

| Preferred Term | Meaning (Approved Usage) | Terms to Avoid |
|---|---|---|
| AI Business Partner | The product: WORLD's AI persona that partners with the user to run their business. Use the full term on first mention. | AI assistant, bot, chatbot, copilot, agent (as a product name) |
| Intelligence Layer | The functional layer housing reasoning, context, and decision support. | AI engine, brain, AI module |
| Business Context Engine | The subsystem that assembles grounding context about the user's business. | context service, memory system, RAG engine |
| Grounding | Anchoring responses in verifiable business data and authoritative sources. | fact-checking, sourcing, referencing |
| Reasoning Framework | The structured method used to move from question and context to answer. | thought process, logic engine, chain of thought (as a product term) |
| Recommendation | A proposed course of action with rationale and evidence. | suggestion, advice, tip |
| Decision Brief | The canonical structured artifact summarising a decision. | decision doc, summary sheet, brief note |
| Human-in-the-Loop | The design pattern of human review or approval at defined points. | manual check, human oversight, HITL (spell out on first use) |
| Human-Approval-Gate | A mandatory human approval checkpoint before an action executes. | sign-off, manual gate, approval step |
| User | The human the AI Business Partner serves. | end user, customer (unless referring to the user's own customers), operator |
| Action | A discrete operation performed by the AI Business Partner. | task (when meaning an operation), command, function call |
| Capability | A reusable business function the AI Business Partner can invoke. | feature (when meaning an invocable function), skill, plugin |
| Advisor | A domain-focused persona providing guidance. | expert, consultant, specialist bot |
| Explainability | The property of outputs being accompanied by an understandable rationale. | transparency (when meaning explanation), interpretability (unless technical) |
| Confidence | A qualified expression of certainty in an output. | probability (unless a numeric value is truly meant), sureness |
| Guardrail | A constraint keeping behaviour safe and in policy. | rule, filter, restriction |
| Permission | An explicit grant authorising access or action. | access, right, privilege (privilege is reserved for Least Privilege) |
| Least Privilege | The principle of granting only the minimum required permissions. | minimal access, restricted mode |
| Escalation | Routing to a human or higher authority beyond the AI mandate. | hand-off (when meaning escalation), referral |
| Clarification | A structured request to resolve ambiguity before acting. | follow-up question, prompt-back |
| Audit Trail | The immutable record of reasoning, actions, and approvals. | log, history, activity feed |
| Hallucination | A confident but unsupported or fabricated statement (to be prevented). | mistake, error, made-up answer |

## Usage Rules

- Introduce a preferred term in full on first use within a document; an approved abbreviation may follow in parentheses and be used thereafter.
- Never substitute a deprecated term for a preferred term, even for stylistic variety.
- When quoting external frameworks (see WORLD-VOL03-A7), retain the external term but map it to the WORLD preferred term on first mention.
- Capitalise canonical product and subsystem names (AI Business Partner, Business Context Engine, Intelligence Layer) consistently.

## Cross-References

- [AI Glossary](/docs/blueprint/volume-03-ai-business-partner/appendices/ai-glossary.md)
- [Reasoning Framework](/docs/blueprint/volume-03-ai-business-partner/chapters/reasoning-framework.md)
- [Personas and Advisors](/docs/blueprint/volume-03-ai-business-partner/chapters/personas-and-advisors.md)

## References

- [Volume 01 - Vision and Philosophy](/docs/blueprint/volume-01-vision-and-philosophy/README.md)
- [Document Standards](/docs/governance/document-standards.md)

## Change Log

| Version | Date | Author | Notes |
|---|---|---|---|
| 1.0 | 2026-07-12 | Lead Software Engineer | Initial approved version. |
