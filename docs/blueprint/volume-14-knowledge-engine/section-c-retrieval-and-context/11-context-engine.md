# Volume 14 - Context Engine

| Field | Value |
|---|---|
| Document ID | WORLD-VOL14-011 |
| Title | Context Engine |
| Version | 1.0 |
| Status | Approved |
| Classification | Internal |
| Founder | Mahesh Choudhary |

## Purpose

The Context Engine assembles the right knowledge, at the right scope, for the right actor, at the moment of need. A language model reasons only over the tokens placed in front of it; the quality of any AI decision is therefore bounded by the quality of the context supplied. This chapter defines how WORLD constructs a grounded, permission-scoped, token-budgeted context package for every request, so that the AI Business Partner (Volume 03) and AI Agents (Volume 13) reason over authoritative organizational truth rather than parametric guesswork.

## Scope

The chapter covers context assembly: intent interpretation, source selection across the Knowledge Engine, relevance ranking, deduplication, token budgeting, and packaging with provenance. It defines the boundary between the Context Engine (what to include and how to present it) and the Retrieval Engine (Chapter 12, how candidates are fetched). It does not define ingestion, ontology, or storage, which belong to other sections of this volume.

## Architecture

The Context Engine is an orchestration layer. It receives an intent, resolves the actor's scope, invokes retrieval, composes candidates into a bounded package, and returns that package with citations for grounding.

```mermaid
flowchart LR
    REQ[Request + Intent] --> INT[Intent Interpretation]
    INT --> SCOPE[Scope Resolution\nTenant + Permission]
    SCOPE --> SEL[Source Selection]
    SEL --> RET[Retrieval Engine Ch 12]
    RET --> RANK[Relevance Ranking]
    RANK --> DEDUP[Dedup + Freshness]
    DEDUP --> BUDGET[Token Budgeting]
    BUDGET --> PKG[Context Package + Citations]
    PKG --> AI[AI / Agent Reasoning]
```

Intent interpretation converts a raw request into a retrieval plan. Scope resolution binds the request to a tenant and permission set before any knowledge is touched. Source selection chooses which stores to query (documents, policies, business rules, vector index, knowledge graph). Ranking, deduplication, and freshness filtering reduce noise, and token budgeting fits the highest-value evidence within the model's window.

## Data Flow

A request enters with an intent and an authenticated principal. The engine resolves scope, selects sources, and delegates candidate fetching to the Retrieval Engine. Candidates are ranked, de-duplicated, and freshness-checked, then packed against a token budget that reserves space for the system prompt, the retrieved evidence, and the response. The engine emits a context package: ordered evidence blocks, each carrying a source identifier, version, and confidence, ready to be grounded by the consuming model. Every assembly is logged for audit and analytics.

## Relationship with AI

The Context Engine is the supply line for AI cognition. It operationalizes the Knowledge Model of the AI Business Partner (Volume 03, Chapter 17) by deciding what the AI is allowed to see and what it must verify. Agents (Volume 13, Chapter 10) invoke context assembly as a read-only, governed step before reasoning. By enforcing grounding and provenance at assembly time, the engine converts a probabilistic model into a source-backed decision-maker: claims trace to evidence, and unretrievable claims surface as gaps rather than confident inventions.

## Relationship with ERP

Operational truth lives in the ERP (Volumes 05-06). The Context Engine treats ERP records - the current price, the account tier, the open order, the approval state - as first-class, high-freshness context. When intent references a transactional entity, the engine pulls the live record and pairs it with the governing policy or SOP from the Knowledge Engine, so the AI reasons over both the rule and the current fact. ERP data is scoped by the same tenant and permission boundary as all other context.

## Relationship with Analytics

Every context assembly emits telemetry: which sources were selected, hit rates, ranking scores, token utilization, and grounding coverage. Business Intelligence (Volume 04) consumes this to measure knowledge effectiveness - which sources answer questions, which intents go unserved, and where context is thin. These signals close the loop: gaps detected in analytics drive knowledge acquisition, and low-value sources are demoted, continuously improving the context supplied to the AI.

## Implementation Strategy

Implementation is staged. First, establish scope resolution and a single-source assembly path so that every context package is permission-safe and cited from day one. Second, add multi-source selection and relevance ranking across the vector index and structured stores. Third, introduce token budgeting with reserved regions and eviction by marginal value. Fourth, wire telemetry into Analytics and use it to tune source weights. The engine is stateless per request and horizontally scalable; assembly latency is held within an interactive budget by parallel retrieval and caching of stable sources within a task.

**Enterprise example:** A finance agent is asked, "Can we approve this vendor invoice for early-payment discount?" The Context Engine interprets the intent, resolves the finance team's scope, and assembles a package containing the live invoice record from the ERP, the current early-payment policy from the policy store, and the vendor's contract terms retrieved from the vector index. It de-duplicates two near-identical policy drafts, keeps only the approved version, and budgets the package to fit the model window. The agent answers "yes, a two percent discount applies" and cites the exact policy clause, contract term, and invoice line - a grounded decision, assembled in one governed step.

## Key Components

| Component | Responsibility | Guarantee |
|---|---|---|
| Intent Interpreter | Converts request into a retrieval plan | Correct source targeting |
| Scope Resolver | Binds request to tenant and permissions | No cross-tenant leakage |
| Source Selector | Chooses stores to query | Right knowledge, least noise |
| Ranking + Dedup | Orders and de-duplicates candidates | Signal over redundancy |
| Token Budgeter | Fits evidence to the model window | Highest value within limit |
| Package Composer | Emits ordered, cited evidence blocks | Grounded, auditable output |

## Cross-References

- [Retrieval Engine](/docs/blueprint/volume-14-knowledge-engine/section-c-retrieval-and-context/12-retrieval-engine.md)
- [Semantic Search](/docs/blueprint/volume-14-knowledge-engine/section-c-retrieval-and-context/13-semantic-search.md)
- [Volume 03 - Context Understanding](/docs/blueprint/volume-03-ai-business-partner/README.md)
- [Volume 13 - Knowledge Access](/docs/blueprint/volume-13-ai-agents/section-c-agent-cognition/10-knowledge-access.md)

## References

- [Volume 01 - Vision and Philosophy](/docs/blueprint/volume-01-vision-and-philosophy/README.md)
- [Document Standards](/docs/governance/document-standards.md)

## Change Log

| Version | Date | Author | Notes |
|---|---|---|---|
| 1.0 | 2026-07-12 | Lead Software Engineer | Initial approved version. |
