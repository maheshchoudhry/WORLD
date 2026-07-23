# Volume 13 - Agent Terminology

| Field | Value |
|---|---|
| Document ID | WORLD-VOL13-A2 |
| Title | Agent Terminology |
| Version | 1.0 |
| Status | Approved |
| Classification | Internal |
| Founder | Mahesh Choudhary |

## Purpose

This appendix defines the controlled vocabulary for the agent tier of Project WORLD: the preferred terms every chapter, diagram, and agent definition must use, and the terms to avoid because they are ambiguous, anthropomorphizing, or misleading. Where the glossary (Appendix A1) fixes meanings, this appendix fixes usage. Consistent terminology matters because agents make consequential decisions, and imprecise or over-stated language about their capability erodes the clarity that governance depends on.

## Scope

The document establishes the canonical term for each concept, lists common alternatives that must not be used in Volume 13, and states the reason. It also gives usage conventions for describing agent behaviour precisely and without overstatement. It governs terminology within Volume 13 only; adjacent vocabularies for security, infrastructure, and the knowledge engine are owned by Volumes 12, 11, and 14 respectively. It does not redefine the concepts themselves, which the glossary covers.

## Controlled Vocabulary

| Preferred Term | Use For | Do Not Use |
|---|---|---|
| Agent | An autonomous, governed software actor | bot, assistant, worker, digital employee |
| Tool Calling | An agent invoking a defined tool | plugin use, skill, action (bare) |
| Guardrail | A hard runtime constraint | filter, limiter, safety net |
| Human Approval | Required human authorization of an action | sign-off, rubber stamp, checkpoint |
| Autonomy Level | A graduated rung of unattended authority | trust level, maturity, tier |
| Supervisor Agent | The routing and coordinating core agent | orchestrator agent, master agent, boss agent |
| Specialist Agent | A domain-focused agent | expert bot, micro-agent |
| Decision Authority | The scope an agent may act on unattended | permission set (for this sense), power |
| Task Success | Achievement of the intended outcome | accuracy (for this sense), win rate |
| Kill-Switch | The out-of-band halt control | off button, circuit breaker (for this sense) |
| Reasoning | The model-driven derivation of conclusions | thinking, understanding, knowing |
| Retrieval-Augmented Generation | Grounded generation from retrieved evidence | search-and-answer, lookup mode |

## Terms to Avoid

| Term to Avoid | Reason | Use Instead |
|---|---|---|
| Sentient / conscious | Attributes awareness agents do not have; misleads governance | autonomous, capable |
| Understands / knows | Overstates model cognition as human comprehension | processes, infers, retrieves |
| Self-aware | Implies introspective consciousness | reflective (of the reflection process only) |
| Digital employee / colleague | Anthropomorphizes and blurs accountability | agent |
| Fully trusted | Implies unbounded autonomy; no agent is ungoverned | operating at autonomy level N |
| Fool-proof / cannot fail | False assurance; all agents can err | governed, guardrailed |
| Learns on its own | Implies ungoverned self-modification | improves under the governed learning model |
| Decides freely | Contradicts bounded autonomy | decides within its decision authority |

## Usage Conventions

Describe agent behaviour in terms of observable action and evidence, not inner states: prefer "the agent inferred X from the retrieved records" over "the agent understood X." Always pair a statement of autonomy with its bound - name the autonomy level or the guardrail that constrains it. Attribute outcomes to agents by identity, never anonymously, to preserve accountability. Reserve human-oriented verbs such as *believe* or *want* for people; use *infer*, *propose*, *execute*, and *escalate* for agents.

## Cross-References

- [Agent Glossary](/docs/blueprint/volume-13-ai-agents/appendices/agent-glossary.md)
- [Agent Definition Template](/docs/blueprint/volume-13-ai-agents/appendices/agent-definition-template.md)
- [Agent Governance](/docs/blueprint/volume-13-ai-agents/section-g-governance-and-evolution/31-agent-governance.md)

## References

- [Volume 01 - Vision and Philosophy](/docs/blueprint/volume-01-vision-and-philosophy/README.md)
- [Document Standards](/docs/governance/document-standards.md)

## Change Log

| Version | Date | Author | Notes |
|---|---|---|---|
| 1.0 | 2026-07-12 | Lead Software Engineer | Initial approved version. |
