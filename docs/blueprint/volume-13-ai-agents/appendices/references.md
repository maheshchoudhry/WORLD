# Volume 13 - References

| Field | Value |
|---|---|
| Document ID | WORLD-VOL13-A7 |
| Title | References |
| Version | 1.0 |
| Status | Approved |
| Classification | Internal |
| Founder | Mahesh Choudhary |

## Purpose

This appendix collects the established, real-world works and concepts on which Volume 13 draws. Its purpose is intellectual honesty and traceability: WORLD's agent tier is not invented in a vacuum but builds on a growing body of research and practice in language-model agents, tool use, multi-agent systems, and human oversight. Naming those sources lets a reader verify the reasoning, go deeper, and understand which ideas WORLD has adopted, adapted, or deliberately extended.

## Scope

The document lists foundational references grouped by topic, covering agent reasoning and acting, tool use and function calling, retrieval-augmented generation, multi-agent systems, human-in-the-loop oversight, and guardrails and evaluation. Each entry names the work and its author or origin; formal citation details can be resolved from these names through their publishers or the originating organizations. To preserve accuracy, this appendix does not fabricate URLs or invent bibliographic identifiers. It is a curated starting point, not an exhaustive bibliography.

## Agent Reasoning and Acting

| Reference | Author / Origin | Relevance to WORLD |
|---|---|---|
| ReAct: Synergizing Reasoning and Acting in Language Models | Yao et al. | Foundation for interleaving reasoning and tool use in the reasoning engine. |
| Chain-of-Thought Prompting | Wei et al. | Basis for eliciting intermediate reasoning in agents. |
| Reflexion: Language Agents with Verbal Reinforcement Learning | Shinn et al. | Conceptual reference for the reflection engine. |
| Toolformer: Language Models Can Teach Themselves to Use Tools | Schick et al. | Reference for models learning to invoke tools. |

## Tool Use and Function Calling

| Reference | Author / Origin | Relevance to WORLD |
|---|---|---|
| Function Calling / Tool Use interfaces | Anthropic and OpenAI | Reference pattern for structured tool invocation in tool calling. |
| Model Context Protocol (MCP) | Anthropic | Reference for standardized agent-to-tool and agent-to-data connectivity. |
| Gorilla: Large Language Model Connected with APIs | Patil et al. | Reference for model-driven API invocation. |

## Retrieval-Augmented Generation

| Reference | Author / Origin | Relevance to WORLD |
|---|---|---|
| Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks | Lewis et al. | Foundation for grounded knowledge access. |
| Dense Passage Retrieval | Karpukhin et al. | Reference for embedding-based retrieval behind RAG. |
| REALM: Retrieval-Augmented Language Model Pre-Training | Guu et al. | Reference for integrating retrieval with generation. |

## Multi-Agent Systems

| Reference | Author / Origin | Relevance to WORLD |
|---|---|---|
| An Introduction to MultiAgent Systems | Michael Wooldridge | Foundational reference for agent coordination and design. |
| Generative Agents: Interactive Simulacra of Human Behavior | Park et al. | Reference for memory and multi-agent interaction patterns. |
| Supervisor and worker agent patterns | Community and vendor practice | Reference for the supervisor-agent orchestration model. |

## Human-in-the-Loop Oversight

| Reference | Author / Origin | Relevance to WORLD |
|---|---|---|
| Human-in-the-Loop Machine Learning | Robert Munro | Reference for structured human oversight of automated systems. |
| Constitutional AI | Anthropic | Reference for principle-based behavioural constraints. |
| Concrete Problems in AI Safety | Amodei et al. | Reference for safe-interruptibility and oversight motivations behind the kill-switch. |

## Guardrails and Evaluation

| Reference | Author / Origin | Relevance to WORLD |
|---|---|---|
| NIST AI Risk Management Framework | US National Institute of Standards and Technology | Reference for governing and measuring AI risk. |
| OWASP Top 10 for Large Language Model Applications | Open Worldwide Application Security Project | Reference for agent-specific risks such as prompt injection. |
| HELM: Holistic Evaluation of Language Models | Stanford CRFM | Reference for multi-metric model evaluation behind agent performance. |

## Cross-References

- [Agent Glossary](/docs/blueprint/volume-13-ai-agents/appendices/agent-glossary.md)
- [Agent Governance](/docs/blueprint/volume-13-ai-agents/section-g-governance-and-evolution/31-agent-governance.md)
- [Agent Performance](/docs/blueprint/volume-13-ai-agents/section-g-governance-and-evolution/32-agent-performance.md)

## References

- [Volume 01 - Vision and Philosophy](/docs/blueprint/volume-01-vision-and-philosophy/README.md)
- [Document Standards](/docs/governance/document-standards.md)

## Change Log

| Version | Date | Author | Notes |
|---|---|---|---|
| 1.0 | 2026-07-12 | Lead Software Engineer | Initial approved version. |
