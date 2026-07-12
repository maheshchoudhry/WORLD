# Volume 03 - References

| Field | Value |
|---|---|
| Document ID | WORLD-VOL03-A7 |
| Title | References |
| Version | 1.0 |
| Status | Approved |
| Classification | Internal |
| Founder | Mahesh Choudhary |

## Purpose

This appendix curates the well-established concepts, frameworks, and standards referenced throughout Volume 03. It gives readers a map from the AI Business Partner's design choices to the recognised bodies of knowledge that inform them. References cite concept, author, or standard names rather than fabricated links, so readers can locate authoritative primary sources reliably.

## Scope

The references are grouped by topic and describe how each concept relates to the AI Business Partner. This appendix does not reproduce the source material; it points to it and explains its relevance. Where an external term maps to a WORLD preferred term, that mapping is noted (see WORLD-VOL03-A2).

## Reasoning and Language Models

- **Chain-of-Thought reasoning** - Wei et al., "Chain-of-Thought Prompting Elicits Reasoning in Large Language Models" (2022). Basis for the WORLD Reasoning Framework's step-wise deliberation before answering.
- **ReAct (Reasoning and Acting)** - Yao et al., "ReAct: Synergizing Reasoning and Acting in Language Models" (2022). Informs the Plan-Execute-Reflect pattern for agentic workflows.
- **Reflexion** - Shinn et al., "Reflexion: Language Agents with Verbal Reinforcement Learning" (2023). Informs the reflection stage of multi-step tasks.

## Grounding and Knowledge Retrieval

- **Retrieval-Augmented Generation (RAG)** - Lewis et al., "Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks" (2020). Foundational to the Ground-then-Answer pattern and the Business Context Engine.
- **DIKW hierarchy (Data, Information, Knowledge, Wisdom)** - commonly attributed to Russell Ackoff, "From Data to Wisdom" (1989). Frames how the intelligence layer transforms raw business data into actionable wisdom.
- **Grounding in dialogue** - Herbert H. Clark and Susan E. Brennan, "Grounding in Communication" (1991). Conceptual basis for shared understanding between the user and the AI Business Partner.

## Human-AI Collaboration

- **Human-in-the-Loop** - established practice in machine learning and control systems for incorporating human judgement at defined checkpoints. Basis for the Human-Approval-Gate pattern.
- **Levels of automation and human oversight** - Sheridan and Verplank, levels-of-automation taxonomy (1978); Parasuraman, Sheridan, and Wickens, "A Model for Types and Levels of Human Interaction with Automation" (2000). Informs Bounded-Autonomy and mandate design.
- **Calibrated trust in automation** - Lee and See, "Trust in Automation: Designing for Appropriate Reliance" (2004). Basis for honest confidence signalling and appropriate reliance.

## Explainability and Transparency

- **Explainable AI (XAI)** - DARPA Explainable AI program framing; Gunning and Aha, "DARPA's Explainable Artificial Intelligence Program" (2019). Basis for the Explain-on-Demand pattern.
- **Interpretable models guidance** - Doshi-Velez and Kim, "Towards A Rigorous Science of Interpretable Machine Learning" (2017). Informs standards for explanation quality.
- **Model documentation** - Mitchell et al., "Model Cards for Model Reporting" (2019); Gebru et al., "Datasheets for Datasets" (2018). Inform documentation and provenance practices.

## Decision Support and Management

- **RACI responsibility assignment** - established project and process management practice for clarifying Responsible, Accountable, Consulted, and Informed roles. Informs decision ownership in the Decision Brief.
- **Multi-criteria decision analysis** - established decision science practice underlying the Options Comparison Table.
- **Expected value and risk assessment** - foundational decision-theory concepts underlying the Risk-Weighted Recommendation.

## Governance, Security, and Risk

- **Principle of Least Privilege** - Saltzer and Schroeder, "The Protection of Information in Computer Systems" (1975). Basis for permission scoping in the AI Business Partner.
- **Separation of Duties** - long-established internal-control principle in information security and auditing. Basis for the approval and control model.
- **NIST AI Risk Management Framework (AI RMF 1.0)** - National Institute of Standards and Technology (2023). Reference framework for governing AI risk.
- **ISO/IEC 42001 (AI Management System)** and **ISO/IEC 23894 (AI Risk Management)** - International Organization for Standardization. Reference standards for AI governance and risk.
- **OECD AI Principles** - Organisation for Economic Co-operation and Development (2019). Reference for trustworthy, human-centred AI values.

## Cross-References

- [AI Design Patterns](/docs/blueprint/volume-03-ai-business-partner/appendices/ai-design-patterns.md)
- [Reasoning Framework](/docs/blueprint/volume-03-ai-business-partner/chapters/reasoning-framework.md)
- [Governance and Accountability](/docs/blueprint/volume-03-ai-business-partner/chapters/governance-and-accountability.md)

## References

- [Volume 01 - Vision and Philosophy](/docs/blueprint/volume-01-vision-and-philosophy/README.md)
- [Document Standards](/docs/governance/document-standards.md)

## Change Log

| Version | Date | Author | Notes |
|---|---|---|---|
| 1.0 | 2026-07-12 | Lead Software Engineer | Initial approved version. |
