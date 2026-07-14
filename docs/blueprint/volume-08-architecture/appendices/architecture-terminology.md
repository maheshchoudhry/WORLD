# Volume 08 - Architecture Terminology

| Field | Value |
|---|---|
| Document ID | WORLD-VOL08-A2 |
| Title | Architecture Terminology |
| Version | 1.0 |
| Status | Approved |
| Classification | Internal |
| Founder | Mahesh Choudhary |

## Purpose

This appendix defines the controlled vocabulary of Project WORLD's architecture: the canonical terms that must be used, the way they must be used, and the near-synonyms that must be avoided. Where the Glossary (Appendix A1) explains *what a term means*, this document governs *which term to use and how*. Its purpose is consistency of expression across chapters, diagrams, code, and Architecture Decision Records, so that reviewers and the AI Business Partner encounter one name for one concept everywhere in WORLD.

## Scope

The document covers the canonical architecture terms of Volume 08 and their approved usage, capitalization, and abbreviation. It lists discouraged synonyms and states the preferred term. It does not define business terminology (Volume 05) nor writing style beyond terminology (governed by the Document Standards). Compliance is expected of all authors contributing to Volume 08 and to architecture artifacts elsewhere in the blueprint.

## Canonical Terminology

The following table fixes the canonical term for each concept, its approved usage, and the abbreviation, if any, permitted after first full use.

| Canonical Term | Approved Usage | Abbreviation |
|---|---|---|
| Project WORLD | The product and platform as a whole; always capitalized as WORLD. | WORLD |
| AI Business Partner | The autonomous, governed AI actor; a proper noun, always capitalized. | the Partner (after first use) |
| Bounded Context | A model-consistency boundary; two words, each capitalized when naming the concept. | - |
| Domain Event | An immutable published fact; use in preference to "message" for domain state changes. | - |
| Command | An intent to change state; distinct from Query. | - |
| Query | A read that does not change state; distinct from Command. | - |
| Aggregate | A consistency cluster with a single root; use "aggregate root" for the entry entity. | - |
| Modular Monolith | The default deployment style for WORLD; two words. | - |
| Microservice | A single independently deployable service; plural "microservices" names the style. | - |
| Architecture Decision Record | A recorded architectural decision; use the full term on first use. | ADR |
| Security Context | The uniform authenticated-principal object; two words, capitalized as a named concept. | - |
| Ubiquitous Language | The shared domain vocabulary within a Bounded Context. | - |
| Observability | The umbrella term for logs, metrics, and traces; do not equate with "monitoring". | - |
| Recovery Point Objective | The tolerated data-loss window. | RPO |
| Recovery Time Objective | The tolerated restoration time. | RTO |

## Approved Usage Notes

- **Capitalization of named concepts.** Capitalize a term when it names a WORLD architectural concept ("the Repository pattern isolates the Aggregate"); use lower case for the general English word ("a repository of documents").
- **Abbreviations.** Spell out an abbreviation on first use in each document, then use the short form (for example, "Architecture Decision Record (ADR)").
- **Actors.** The AI Business Partner, the Identity Provider, and the Workflow Engine are named actors and are capitalized as such.
- **Events versus messages.** Use *Domain Event* for business facts; reserve *message* for transport-level payloads on a broker.
- **Style versus pattern versus principle.** A *style* shapes a whole system (Clean, Hexagonal, Microservices); a *pattern* is a reusable solution to a recurring problem (Repository, CQRS, Saga); a *principle* is a durable rule (Section A). Do not use these words interchangeably.

## Terms to Avoid

| Avoid | Use Instead | Reason |
|---|---|---|
| "CRUD service" | Command / Query, Repository | Obscures the intent-carrying distinction between writes and reads. |
| "Layered n-tier" (as a synonym for Clean) | Clean Architecture | "n-tier" implies technical layering; Clean mandates inward dependency direction. |
| "Chatbot" | AI Business Partner | WORLD's AI is an autonomous, governed actor, not a conversational widget. |
| "Monolith" (unqualified, pejorative) | Modular Monolith | The unqualified term implies a big ball of mud; WORLD's default is modular and bounded. |
| "Micro-frontend/micro-everything" | the specific pattern name | Vague marketing terms; name the actual pattern or style. |
| "Logging" (to mean all telemetry) | Observability | Logging is one signal; Observability is the umbrella concern. |
| "Sync it up" / "eventual" (as a hand-wave) | Eventual Consistency (with model stated) | Consistency guarantees must be explicit, not implied. |
| "Permissions check" (for identity) | Authentication vs Authorization | These are distinct concerns and must be named separately. |
| "Backup site" (for resilience) | Disaster Recovery, RPO, RTO | Resilience objectives must be quantified, not described loosely. |
| "Bus" (unqualified) | Message Broker / Event Bus (as defined) | Ambiguous; state whether transport or in-process dispatch is meant. |

## Cross-References

- [Architecture Glossary](/docs/blueprint/volume-08-architecture/appendices/architecture-glossary.md)
- [Architecture Principles](/docs/blueprint/volume-08-architecture/section-a-architecture-foundations/01-architecture-principles.md)
- [Patterns Catalog](/docs/blueprint/volume-08-architecture/appendices/patterns-catalog.md)

## References

- [Volume 01 - Vision and Philosophy](/docs/blueprint/volume-01-vision-and-philosophy/README.md)
- [Document Standards](/docs/governance/document-standards.md)

## Change Log

| Version | Date | Author | Notes |
|---|---|---|---|
| 1.0 | 2026-07-12 | Lead Software Engineer | Initial approved version. |
