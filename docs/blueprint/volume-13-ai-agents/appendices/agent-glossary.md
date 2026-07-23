# Volume 13 - Agent Glossary

| Field | Value |
|---|---|
| Document ID | WORLD-VOL13-A1 |
| Title | Agent Glossary |
| Version | 1.0 |
| Status | Approved |
| Classification | Internal |
| Founder | Mahesh Choudhary |

## Purpose

This appendix provides a single, authoritative glossary of the agent and AI terms used throughout Volume 13. Its purpose is to remove ambiguity: when a chapter uses a term such as *tool calling*, *guardrail*, or *autonomy level*, this glossary fixes its meaning for Project WORLD. Agent systems combine concepts from language models, planning, and distributed systems, and reasoning about them coherently requires that every author mean the same thing by the same word. A shared vocabulary is a precondition for a governable agent tier.

## Scope

The glossary defines agent, cognition, collaboration, and governance terms that appear in Volume 13, Sections A through G, together with a small number of adjacent AI terms needed to make those definitions self-contained. Definitions are concise and vendor-neutral. It does not redefine security terms (governed by Volume 12), infrastructure terms (Volume 11), or knowledge-engine terms (Volume 14). Where a term has a broader meaning in general AI usage, the definition given here is the WORLD-canonical one for the agent context.

## Glossary

| Term | Definition |
|---|---|
| Agent | An autonomous software entity that perceives context, reasons, and acts toward a goal using tools and knowledge under governance. |
| Agent Identity | The canonical, verifiable representation of an agent used for authentication, authorization, and audit. |
| Agent Registry | The authoritative catalog of agents, their versions, capabilities, and status. |
| Agent Runtime | The managed execution environment in which an agent instance runs. |
| Autonomy Level | A graduated rung defining what an agent may do unattended versus what requires human authorization. |
| Audit Trail | An append-only, tamper-evident record of an agent's decisions and actions. |
| Capability | A discrete function an agent is designed and permitted to perform. |
| Chain of Thought | An intermediate reasoning trace a model produces to reach an answer. |
| Context Window | The bounded span of tokens a model can consider in a single inference. |
| Core Agent | An agent providing broad, cross-domain organizational function, such as a supervisor or executive agent. |
| Decision Authority | The set of actions an agent may decide and execute without human approval. |
| Delegation | The assignment of a task or sub-goal from one agent to another. |
| Embedding | A numeric vector representation of text or data used for similarity and retrieval. |
| Evaluation | The measurement of agent quality and performance against datasets or live samples. |
| Faithfulness | The degree to which an agent's output is grounded in its supporting evidence. |
| Fine-Tuning | Adapting a model's weights on task-specific data to improve behaviour. |
| Function Calling | A model's structured invocation of a defined tool with typed arguments. |
| Grounding | Anchoring an agent's output in retrieved, authoritative sources. |
| Guardrail | A hard runtime constraint that prevents an agent from exceeding permitted behaviour. |
| Hallucination | A fluent but unsupported or incorrect model output. |
| Human-in-the-Loop | A control pattern requiring human authorization before a consequential action executes. |
| Inference | A single execution of a model to produce output from input. |
| Kill-Switch | An out-of-band control that immediately suspends an agent, class, or the whole fleet. |
| Knowledge Source | An authoritative body of information an agent may retrieve from. |
| Large Language Model (LLM) | A model trained on large text corpora that generates and reasons over natural language. |
| Learning Model | The governed mechanism by which agents improve across versions from evidence. |
| Memory | The store of an agent's short-term and long-term state across a task or over time. |
| Multi-Agent System | A set of agents that coordinate to achieve goals beyond any single agent. |
| Orchestration | The coordination of agents and steps into a governed workflow. |
| Planning | The decomposition of a goal into an ordered set of executable steps. |
| Policy | An approved declaration of what an agent is permitted to do. |
| Prompt | The input instruction and context supplied to a model. |
| ReAct | A pattern interleaving reasoning and acting so a model plans, calls tools, and observes results iteratively. |
| Reasoning Engine | The component that draws conclusions and selects actions from context and evidence. |
| Reflection | An agent's review of its own output or process to detect and correct error. |
| Retrieval-Augmented Generation (RAG) | Generating output conditioned on evidence retrieved from a knowledge source. |
| Specialist Agent | An agent focused on a specific domain, such as finance, security, or coding. |
| Supervisor Agent | The core agent that routes work to and coordinates other agents. |
| System Prompt | The persistent instruction defining an agent's role, constraints, and behaviour. |
| Task Success | Whether an agent achieved the intended outcome of a task. |
| Temperature | A sampling parameter controlling the randomness of model output. |
| Token | The unit of text a model processes; the basis of context and cost accounting. |
| Tool | An external function or service an agent may invoke to act or retrieve information. |
| Tool Calling | The act of an agent invoking a tool with structured arguments and consuming its result. |
| Vector Store | A database that indexes embeddings for similarity search. |

## Cross-References

- [Agent Terminology](/docs/blueprint/volume-13-ai-agents/appendices/agent-terminology.md)
- [Tool Calling](/docs/blueprint/volume-13-ai-agents/section-c-agent-cognition/09-tool-calling.md)
- [Agent Governance](/docs/blueprint/volume-13-ai-agents/section-g-governance-and-evolution/31-agent-governance.md)

## References

- [Volume 01 - Vision and Philosophy](/docs/blueprint/volume-01-vision-and-philosophy/README.md)
- [Document Standards](/docs/governance/document-standards.md)

## Change Log

| Version | Date | Author | Notes |
|---|---|---|---|
| 1.0 | 2026-07-12 | Lead Software Engineer | Initial approved version. |
