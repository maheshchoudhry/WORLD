# Volume 09 - Database Terminology

| Field | Value |
|---|---|
| Document ID | WORLD-VOL09-A2 |
| Title | Database Terminology |
| Version | 1.0 |
| Status | Approved |
| Classification | Internal |
| Founder | Mahesh Choudhary |

## Purpose

This appendix defines the controlled vocabulary of Project WORLD's data tier: the canonical terms that must be used, the way they must be used, and the near-synonyms that must be avoided. Where the Glossary (Appendix A1) explains *what a term means*, this document governs *which term to use and how*. Its purpose is consistency of expression across chapters, data models, migrations, and code, so that reviewers and the AI Business Partner encounter one name for one concept everywhere in WORLD's database.

## Scope

The document covers the canonical database terms of Volume 09 and their approved usage, capitalization, and abbreviation. It lists discouraged synonyms and states the preferred term. It does not define business terminology (Volume 05) nor writing style beyond terminology (governed by the Document Standards). Compliance is expected of all authors contributing to Volume 09 and to data artifacts elsewhere in the blueprint.

## Canonical Terminology

The following table fixes the canonical term for each concept, its approved usage, and the abbreviation, if any, permitted after first full use.

| Canonical Term | Approved Usage | Abbreviation |
|---|---|---|
| Master Data | The shared, slowly changing core business entities; two words, capitalized when naming the category. | - |
| Reference Data | Controlled code lists and classifications; distinct from Master Data. | - |
| Transactional Data | Event-level records of business operations; do not shorten to "transactions" when the category is meant. | - |
| Surrogate Key | The system-generated primary key; use in preference to "auto ID" or "technical key". | - |
| Natural Key | A business-meaningful identifier; pair with Surrogate Key when contrasting. | - |
| Primary Key | The unique row identifier; always spell out on first use per document. | PK |
| Foreign Key | A referential link to another table's primary key. | FK |
| Tenant Key | The column enforcing multi-tenant scoping; two words, capitalized as a named concept. | - |
| Soft Delete | Logical deletion via a marker column; two words, not "logical delete" in prose. | - |
| Normalization | The reduction of redundancy through normal forms; reserve for the formal process. | - |
| Denormalization | The deliberate, documented introduction of redundancy for reads. | - |
| Referential Integrity | The guarantee of valid foreign-key references; do not shorten to "RI" in prose. | - |
| Data Dictionary | The authoritative catalog of entities and attributes. | - |
| Sharding | Horizontal partitioning across instances; distinct from Partitioning within one instance. | - |
| Eventual Consistency | The convergence consistency model; always state the model, never imply it. | - |

## Approved Usage Notes

- **Capitalization of named concepts.** Capitalize a term when it names a WORLD data concept ("the Tenant Key scopes every Master Data row"); use lower case for the general English word ("a reference to the source document").
- **Abbreviations.** Spell out an abbreviation on first use in each document, then use the short form (for example, "Primary Key (PK)").
- **Data categories.** Master Data, Reference Data, Transactional Data, Operational Data, Analytical Data, Knowledge Data, and Metadata are the seven named categories and are capitalized as such.
- **Keys.** Use *Surrogate Key* for the system identifier and *Natural Key* for the business identifier; never use "key" alone where the kind matters.
- **Partitioning versus sharding.** Use *Partitioning* for division within a single database instance and *Sharding* for distribution across independent instances. Do not use them interchangeably.

## Terms to Avoid

| Avoid | Use Instead | Reason |
|---|---|---|
| "Lookup table" | Reference Data | Understates governance; reference codes are controlled, versioned assets. |
| "Auto ID" / "technical key" | Surrogate Key | Imprecise; Surrogate Key is the canonical WORLD term. |
| "Delete flag" | Soft Delete | Names a mechanism loosely; Soft Delete is the standard concept and pattern. |
| "Denorm" (as a verb) | Denormalization | Abbreviated slang; use the full, deliberate term to signal it is a decision. |
| "Partition" (for cross-instance split) | Sharding | Conflates two distinct distribution strategies. |
| "Consistent eventually" (hand-wave) | Eventual Consistency (with model stated) | Consistency guarantees must be explicit, not implied. |
| "Archive" (to mean delete) | Archival vs Purge | Archival preserves data; purging destroys it. The two must be named separately. |
| "Company column" | Tenant Key / Company Key (as defined) | Ambiguous; state whether tenant-level or company-level isolation is meant. |
| "Backup table" (for history) | Audit Trail / History Table | Loose; historical and audit data have defined structures and retention. |
| "Index everything" | Index Strategy | Indexing is a designed trade-off, not a blanket practice. |

## Cross-References

- [Database Glossary](/docs/blueprint/volume-09-database/appendices/database-glossary.md)
- [Database Standards](/docs/blueprint/volume-09-database/section-a-database-foundations/03-database-standards.md)
- [Naming & Coding Conventions](/docs/blueprint/volume-09-database/appendices/naming-and-coding-conventions.md)

## References

- [Volume 01 - Vision and Philosophy](/docs/blueprint/volume-01-vision-and-philosophy/README.md)
- [Document Standards](/docs/governance/document-standards.md)

## Change Log

| Version | Date | Author | Notes |
|---|---|---|---|
| 1.0 | 2026-07-12 | Lead Software Engineer | Initial approved version. |
