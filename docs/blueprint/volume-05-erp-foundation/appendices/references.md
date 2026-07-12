# Volume 05 - References

| Field | Value |
|---|---|
| Document ID | WORLD-VOL05-A8 |
| Title | References |
| Version | 1.0 |
| Status | Approved |
| Classification | Internal |
| Founder | Mahesh Choudhary |

## Purpose

This appendix curates the established concepts, methods, and standards that underpin Volume 05 - ERP Foundation. It provides an authoritative, grouped list of the intellectual sources WORLD's ERP framework draws upon, so that design decisions can be traced to recognized bodies of knowledge. References cite concept, author, or standard names; no URLs are asserted, and no citations are fabricated.

## Scope

This appendix lists conceptual and standards references relevant to ERP architecture, domain modeling, integration, data management, and controls. It is a reference index, not a bibliography of specific editions. Where a work is widely attributed to an author or an organization, that attribution is named. Entries are grouped by topic for ease of navigation.

## 1. Domain Modeling And Architecture

| Reference | Attribution | Relevance to Volume 05 |
|---|---|---|
| Domain-Driven Design | Eric Evans | Ubiquitous language, aggregates, bounded contexts underpinning module design. |
| Implementing Domain-Driven Design | Vaughn Vernon | Practical aggregate and context mapping guidance. |
| Patterns of Enterprise Application Architecture | Martin Fowler | Layering, domain model, and data mapping patterns. |
| Clean Architecture | Robert C. Martin | Dependency direction and separation of concerns. |

## 2. Microservices And Distributed Systems

| Reference | Attribution | Relevance to Volume 05 |
|---|---|---|
| Building Microservices | Sam Newman | Service autonomy, boundaries, and independent deployability. |
| Microservices architectural style | Martin Fowler and James Lewis | Definition and trade-offs of the microservices approach. |
| Designing Data-Intensive Applications | Martin Kleppmann | Consistency, replication, and reliability foundations. |
| The Twelve-Factor App | Adam Wiggins et al. | Configuration, statelessness, and deployment discipline. |

## 3. Event-Driven Architecture And Messaging

| Reference | Attribution | Relevance to Volume 05 |
|---|---|---|
| Enterprise Integration Patterns | Gregor Hohpe and Bobby Woolf | Messaging, routing, and idempotent consumer patterns. |
| Event Sourcing and CQRS | Greg Young (attributed) | Event-first modeling and command-query separation. |
| Saga pattern | Hector Garcia-Molina and Kenneth Salem (original concept) | Long-running distributed transaction coordination. |

## 4. Master Data And Data Management

| Reference | Attribution | Relevance to Volume 05 |
|---|---|---|
| DAMA-DMBOK (Data Management Body of Knowledge) | DAMA International | Data governance, stewardship, and quality dimensions. |
| Master Data Management | David Loshin | System-of-record, matching, and MDM discipline. |
| Data quality dimensions | DAMA / industry consensus | Accuracy, completeness, consistency, timeliness, validity, uniqueness, integrity. |

## 5. Security, Access Control, And Segregation Of Duties

| Reference | Attribution | Relevance to Volume 05 |
|---|---|---|
| Role-Based Access Control (RBAC) | Ferraiolo and Kuhn; NIST RBAC model | Role-based authorization on services and operations. |
| Segregation of Duties | Internal control practice (COSO-aligned) | Distributing critical steps to prevent fraud and error. |
| ISO/IEC 27001 | International Organization for Standardization | Information security management system requirements. |
| ISO/IEC 27002 | International Organization for Standardization | Information security controls guidance. |
| NIST Cybersecurity Framework | NIST | Identify, protect, detect, respond, recover functions. |

## 6. Financial Controls And Governance

| Reference | Attribution | Relevance to Volume 05 |
|---|---|---|
| Sarbanes-Oxley Act (SOX) controls | U.S. legislation (2002) | Internal control over financial reporting; audit trails and approvals. |
| COSO Internal Control - Integrated Framework | Committee of Sponsoring Organizations | Control environment and control activities. |
| Three-way match | Established accounts-payable control practice | PO, goods receipt, and invoice verification before payment. |
| Double-entry bookkeeping | Luca Pacioli (historical codification) | Balanced debit-and-credit posting foundation of the General Ledger. |

## 7. APIs And Integration Standards

| Reference | Attribution | Relevance to Volume 05 |
|---|---|---|
| REST architectural style | Roy Fielding | Resource-oriented API contract design. |
| OpenAPI Specification | OpenAPI Initiative | API contract description conventions. |
| Semantic Versioning | Tom Preston-Werner | Compatibility signaling for contracts and events. |
| Idempotency in HTTP APIs | Industry practice (IETF drafts on idempotency keys) | Safe retries via idempotency keys. |

## 8. Reliability And Operations

| Reference | Attribution | Relevance to Volume 05 |
|---|---|---|
| Site Reliability Engineering | Google (Beyer, Jones, Petoff, Murphy) | Error budgets, observability, and operational discipline. |
| Release It! | Michael Nygard | Stability patterns: retries, timeouts, circuit breakers, bulkheads. |

## Citation Discipline

| Rule | Description |
|---|---|
| CIT-01 | References name concepts, authors, or standards bodies; no URLs are asserted. |
| CIT-02 | Attributions reflect widely recognized authorship; where a concept is community-attributed, this is stated. |
| CIT-03 | New references are added only when the concept is genuinely relied upon in Volume 05. |

## Cross-References

- [ERP Design Standards](/docs/blueprint/volume-05-erp-foundation/appendices/erp-design-standards.md)
- [Enterprise Data Standards](/docs/blueprint/volume-05-erp-foundation/appendices/enterprise-data-standards.md)
- [Integration Templates](/docs/blueprint/volume-05-erp-foundation/appendices/integration-templates.md)

## References

- [Volume 01 - Vision and Philosophy](/docs/blueprint/volume-01-vision-and-philosophy/README.md)
- [Document Standards](/docs/governance/document-standards.md)

## Change Log

| Version | Date | Author | Summary |
|---|---|---|---|
| 1.0 | 2026-07-12 | Lead Software Engineer | Initial approved version. |
