# Volume 08 - References

| Field | Value |
|---|---|
| Document ID | WORLD-VOL08-A7 |
| Title | References |
| Version | 1.0 |
| Status | Approved |
| Classification | Internal |
| Founder | Mahesh Choudhary |

## Purpose

This appendix collects the established, real-world architecture works and standards on which Volume 08 draws. Its purpose is intellectual honesty and traceability: WORLD's architecture is not invented in a vacuum but stands on a body of well-known books, papers, models, and specifications. Naming those sources lets a reader verify the reasoning, go deeper, and understand which ideas WORLD has adopted, adapted, or deliberately departed from.

## Scope

The document lists foundational references grouped by topic, covering architectural styles, domain modeling, distributed systems, APIs and events, identity, and operations. Each entry names the work and its author or issuing body; formal citation details can be resolved from these names through their official publishers or standards bodies. To preserve accuracy, this appendix does not fabricate URLs or invent bibliographic identifiers. It is a curated starting point, not an exhaustive bibliography.

## Architectural Styles and Design

| Reference | Author / Origin | Relevance to WORLD |
|---|---|---|
| Clean Architecture: A Craftsman's Guide to Software Structure and Design | Robert C. Martin | Basis for the inward-dependency layering in Chapter 05. |
| The Clean Architecture (article) | Robert C. Martin | Concise statement of the dependency rule adopted by WORLD. |
| Hexagonal Architecture (Ports and Adapters) | Alistair Cockburn | Foundation of the isolation model in Chapter 06. |
| Patterns of Enterprise Application Architecture | Martin Fowler | Source of the Repository and related application patterns. |
| Design Patterns: Elements of Reusable Object-Oriented Software | Gamma, Helm, Johnson, Vlissides (Gang of Four) | Vocabulary of reusable object patterns underpinning the catalog. |

## Domain-Driven Design

| Reference | Author / Origin | Relevance to WORLD |
|---|---|---|
| Domain-Driven Design: Tackling Complexity in the Heart of Software | Eric Evans | Source of bounded contexts and ubiquitous language in Chapter 07. |
| Implementing Domain-Driven Design | Vaughn Vernon | Practical aggregate and context-mapping guidance applied in WORLD. |
| Domain-Driven Design Distilled | Vaughn Vernon | Concise reference for the DDD terminology used across Volume 08. |

## Distributed Systems and Data

| Reference | Author / Origin | Relevance to WORLD |
|---|---|---|
| CAP Theorem (Brewer's conjecture) | Eric Brewer; proof by Gilbert and Lynch | Frames the consistency/availability trade-offs in Chapters 11, 12, and 24. |
| Designing Data-Intensive Applications | Martin Kleppmann | Reference for consistency models, replication, and event streams. |
| Building Microservices | Sam Newman | Guidance on service boundaries and distribution in Chapter 08. |
| Enterprise Integration Patterns | Gregor Hohpe and Bobby Woolf | Messaging and event patterns behind Chapter 11. |
| Sagas (paper) | Hector Garcia-Molina and Kenneth Salem | Origin of the Saga pattern for cross-boundary consistency. |

## Modeling and Diagrams

| Reference | Author / Origin | Relevance to WORLD |
|---|---|---|
| The C4 Model for Visualising Software Architecture | Simon Brown | Basis of the System Context, Container, and Component diagrams in Appendix A4. |
| UML (Unified Modeling Language) | Object Management Group (OMG) | Source of sequence, state, and structural diagram conventions. |
| Entity-Relationship Model (paper) | Peter Chen | Foundation of the ER diagrams used for data modeling. |

## APIs, Events, and Contracts

| Reference | Author / Origin | Relevance to WORLD |
|---|---|---|
| OpenAPI Specification | OpenAPI Initiative (Linux Foundation) | Contract-first API definition referenced in Chapter 10 and Appendix A5. |
| Representational State Transfer (REST), doctoral dissertation | Roy Fielding | Architectural constraints informing WORLD's API style. |
| CQRS (article) | Greg Young; Martin Fowler | Conceptual basis for the read/write separation in Chapter 12. |
| Event Sourcing (article) | Martin Fowler | Reference for event-based persistence discussed in Chapter 11. |

## Identity, Security, and Access

| Reference | Author / Origin | Relevance to WORLD |
|---|---|---|
| OAuth 2.0 Authorization Framework (RFC 6749) | IETF | Authorization-grant model underlying WORLD authentication in Chapter 19. |
| OpenID Connect Core | OpenID Foundation | Identity layer used by the WORLD Identity Provider. |
| JSON Web Token (RFC 7519) | IETF | Format of the signed identity tokens validated at the API edge. |
| Role-Based Access Control (NIST model) | NIST | Basis of the role-based authorization in Chapter 20. |

## Operations, Cloud, and Resilience

| Reference | Author / Origin | Relevance to WORLD |
|---|---|---|
| The Twelve-Factor App | Adam Wiggins (Heroku) | Principles for cloud-native, portable services in Chapter 25. |
| Release It! Design and Deploy Production-Ready Software | Michael T. Nygard | Source of the Circuit Breaker and stability patterns in Chapter 24. |
| Site Reliability Engineering | Google (Beyer, Jones, Petoff, Murphy, eds.) | Reference for observability, SLOs, and operations in Chapters 22 and 24. |
| Accelerate: The Science of Lean Software and DevOps | Forsgren, Humble, Kim | Evidence base for the delivery and deployment practices in Chapter 26. |

## Cross-References

- [Architecture Glossary](/docs/blueprint/volume-08-architecture/appendices/architecture-glossary.md)
- [Patterns Catalog](/docs/blueprint/volume-08-architecture/appendices/patterns-catalog.md)
- [Technology Standards](/docs/blueprint/volume-08-architecture/appendices/technology-standards.md)

## References

- [Volume 01 - Vision and Philosophy](/docs/blueprint/volume-01-vision-and-philosophy/README.md)
- [Document Standards](/docs/governance/document-standards.md)

## Change Log

| Version | Date | Author | Notes |
|---|---|---|---|
| 1.0 | 2026-07-12 | Lead Software Engineer | Initial approved version. |
