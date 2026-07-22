# Volume 09 - References

| Field | Value |
|---|---|
| Document ID | WORLD-VOL09-A7 |
| Title | References |
| Version | 1.0 |
| Status | Approved |
| Classification | Internal |
| Founder | Mahesh Choudhary |

## Purpose

This appendix collects the established, real-world data and database works and standards on which Volume 09 draws. Its purpose is intellectual honesty and traceability: WORLD's data tier is not invented in a vacuum but stands on a body of well-known books, papers, models, and specifications. Naming those sources lets a reader verify the reasoning, go deeper, and understand which ideas WORLD has adopted, adapted, or deliberately departed from.

## Scope

The document lists foundational references grouped by topic, covering the relational model, data modeling and normalization, data warehousing, distributed data and consistency, data management and governance, and data standards. Each entry names the work and its author or issuing body; formal citation details can be resolved from these names through their official publishers or standards bodies. To preserve accuracy, this appendix does not fabricate URLs or invent bibliographic identifiers. It is a curated starting point, not an exhaustive bibliography.

## Relational Model and Theory

| Reference | Author / Origin | Relevance to WORLD |
|---|---|---|
| A Relational Model of Data for Large Shared Data Banks | Edgar F. Codd | Foundation of the relational model underpinning the entire data tier. |
| The Relational Model for Database Management (Version 2) | Edgar F. Codd | Source of the relational principles and Codd's rules WORLD follows. |
| An Introduction to Database Systems | C. J. Date | Comprehensive treatment of relational theory referenced across Section A. |
| Database System Concepts | Silberschatz, Korth, Sudarshan | Reference for transactions, concurrency, and storage foundations. |

## Data Modeling and Normalization

| Reference | Author / Origin | Relevance to WORLD |
|---|---|---|
| The Entity-Relationship Model - Toward a Unified View of Data | Peter Chen | Foundation of the ER modeling used in Section C and Appendix A4. |
| Further Normalization of the Data Base Relational Model | Edgar F. Codd | Origin of the normal forms applied in Chapter 13. |
| The Data Model Resource Book | Len Silverston | Source of reusable universal patterns (party/role, document) in Appendix A4. |
| Data Modeling Essentials | Graeme Simsion and Graham Witt | Practical modeling guidance behind the modeling standards. |

## Data Warehousing and Analytics

| Reference | Author / Origin | Relevance to WORLD |
|---|---|---|
| The Data Warehouse Toolkit | Ralph Kimball and Margy Ross | Dimensional modeling and slowly changing dimensions in Chapter 08. |
| Building the Data Warehouse | William H. Inmon | The integrated, subject-oriented warehouse view balanced against Kimball. |
| The Data Warehouse Lifecycle Toolkit | Kimball Group | Reference for analytical-store delivery practices. |

## Distributed Data and Consistency

| Reference | Author / Origin | Relevance to WORLD |
|---|---|---|
| CAP Theorem (Brewer's conjecture) | Eric Brewer; proof by Gilbert and Lynch | Frames consistency/availability trade-offs in Chapters 17 and 19. |
| Designing Data-Intensive Applications | Martin Kleppmann | Reference for replication, partitioning, and consistency models. |
| BASE: An Acid Alternative | Dan Pritchett | Basis for the ACID/BASE contrast in Section A and Section D. |
| Principles of Transaction Processing | Bernstein and Newcomer | Reference for transactions, recovery, and isolation. |

## Data Management and Governance

| Reference | Author / Origin | Relevance to WORLD |
|---|---|---|
| DAMA-DMBOK: Data Management Body of Knowledge | DAMA International | Framework for governance, quality, and stewardship in Section G. |
| Data Quality: The Accuracy Dimension | Jack E. Olson | Reference for the data-quality dimensions in Chapter 28. |
| Master Data Management | David Loshin | Guidance on the Master Data category in Chapter 04. |
| Refactoring Databases: Evolutionary Database Design | Scott Ambler and Pramod Sadalage | Basis for versioned schema migration and evolution in Chapter 32. |

## Standards and Specifications

| Reference | Author / Origin | Relevance to WORLD |
|---|---|---|
| ISO/IEC 9075 (SQL) | ISO/IEC | The SQL language standard governing WORLD's relational stores. |
| ISO 8601 (Date and Time) | ISO | Standard for timestamp representation in Appendix A5. |
| ISO 4217 (Currency Codes) | ISO | Standard currency codes for monetary data. |
| ISO 3166 (Country Codes) | ISO | Standard country codes for Reference Data. |
| ISO/IEC 11179 (Metadata Registries) | ISO/IEC | Framework for the metadata management in Chapter 10. |

## Cross-References

- [Database Glossary](/docs/blueprint/volume-09-database/appendices/database-glossary.md)
- [ER Diagram Catalog](/docs/blueprint/volume-09-database/appendices/er-diagram-catalog.md)
- [Data Standards](/docs/blueprint/volume-09-database/appendices/data-standards.md)

## References

- [Volume 01 - Vision and Philosophy](/docs/blueprint/volume-01-vision-and-philosophy/README.md)
- [Document Standards](/docs/governance/document-standards.md)

## Change Log

| Version | Date | Author | Notes |
|---|---|---|---|
| 1.0 | 2026-07-12 | Lead Software Engineer | Initial approved version. |
