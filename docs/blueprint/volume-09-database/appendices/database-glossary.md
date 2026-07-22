# Volume 09 - Database Glossary

| Field | Value |
|---|---|
| Document ID | WORLD-VOL09-A1 |
| Title | Database Glossary |
| Version | 1.0 |
| Status | Approved |
| Classification | Internal |
| Founder | Mahesh Choudhary |

## Purpose

This appendix provides a single, authoritative glossary of the database terms used throughout Volume 09. Its purpose is to remove ambiguity: when a chapter, a data model, or a design review uses a term such as *surrogate key*, *sharding*, or *eventual consistency*, this glossary fixes its meaning for Project WORLD. A shared vocabulary is a precondition for a coherent data tier, because master, reference, transactional, operational, analytical, knowledge, and metadata stores can only stay aligned if their authors mean the same thing by the same word.

## Scope

The glossary defines database and data-management terms that appear in Volume 09, Sections A through H, together with a small number of adjacent terms needed to make those definitions self-contained. Definitions are concise and platform-neutral. It does not redefine business-domain terms (governed by Volume 05), nor does it fix concrete technology choices (governed by Appendix A5, Data Standards). Where a term has a broader meaning in general usage, the definition given here is the WORLD-canonical one.

## Glossary

| Term | Definition |
|---|---|
| ACID | The transactional guarantees of Atomicity, Consistency, Isolation, and Durability that a data store provides for a unit of work. |
| Aggregate Function | A function (such as SUM, COUNT, or AVG) that computes a single value across a set of rows. |
| Archival | The controlled movement of data that is no longer operationally active to lower-cost, longer-retention storage. |
| Attribute | A named property of an entity, realized as a column in a relational table. |
| Audit Trail | An immutable, time-ordered record of who changed what data, when, and from where. |
| BASE | An availability-oriented model (Basically Available, Soft state, Eventual consistency) contrasted with ACID. |
| Cardinality | The numeric relationship between two entities (one-to-one, one-to-many, many-to-many), and separately, the number of distinct values in a column. |
| CAP Theorem | The principle that a distributed data store can guarantee at most two of Consistency, Availability, and Partition tolerance simultaneously. |
| Change Data Capture (CDC) | A technique that observes and streams row-level changes from a source store to downstream consumers. |
| Check Constraint | A rule that restricts the permitted values of a column or row to those satisfying a boolean expression. |
| Column | The vertical structure in a table that holds values of one attribute for every row. |
| Composite Key | A key composed of two or more columns that together identify a row uniquely. |
| Constraint | A declared rule the database enforces to protect integrity (primary key, foreign key, unique, check, not null). |
| Data Dictionary | The authoritative catalog that describes each entity, attribute, type, constraint, and relationship in the model. |
| Data Governance | The exercise of authority and control over data assets through policy, ownership, standards, and stewardship. |
| Data Lineage | The documented origin and transformation path of a data element from source to consumption. |
| Data Mart | A subject-focused subset of an analytical store serving one business area. |
| Data Warehouse | An integrated, subject-oriented, non-volatile analytical store built for query and reporting. |
| Denormalization | The deliberate introduction of redundancy into a schema to improve read performance, accepting update cost. |
| Dimension | A descriptive entity in a dimensional model providing context for facts (for example, customer, product, time). |
| Entity | A distinct thing of business interest about which data is stored; realized as a table. |
| Entity-Relationship (ER) Model | A representation of entities, their attributes, and the relationships among them. |
| Eventual Consistency | A consistency model in which replicas converge to the same state over time, given no new updates. |
| Fact Table | The central table of a star schema holding measures and foreign keys to dimensions. |
| Foreign Key (FK) | A column or set of columns whose values reference the primary key of another table, enforcing referential integrity. |
| Idempotency | The property that applying an operation more than once has the same effect as applying it once. |
| Index | An auxiliary structure that accelerates row lookup and ordering at the cost of storage and write overhead. |
| Isolation Level | The degree to which concurrent transactions are shielded from one another's intermediate state. |
| Knowledge Graph | A graph-structured representation of entities and relationships used as a semantic backbone for reasoning and retrieval. |
| Master Data | The core, slowly changing business entities shared across modules (customers, products, accounts, employees). |
| Materialized View | A stored, physically persisted result of a query, refreshed on a schedule or on demand. |
| Metadata | Data that describes other data: structure, meaning, ownership, lineage, and quality. |
| Migration | A versioned, repeatable change to a database schema or its data. |
| Natural Key | A key formed from attributes with real-world business meaning that already identify an entity. |
| Normalization | The process of organizing columns and tables to reduce redundancy and dependency, expressed as normal forms. |
| Optimistic Concurrency | A concurrency approach that detects conflicts at commit time using a version token rather than locking. |
| Partitioning | The division of a large table into smaller physical segments by a partition key to improve manageability and performance. |
| Primary Key (PK) | The column or columns that uniquely identify every row in a table and cannot be null. |
| Query Plan | The execution strategy the database chooses to satisfy a query, produced by the query optimizer. |
| Read Replica | A copy of a database that serves read traffic to offload the primary and improve availability. |
| Referential Integrity | The guarantee that every foreign key value matches an existing primary key value or is null. |
| Reference Data | Standardized, controlled code lists and classifications (currencies, countries, units, status codes). |
| Relational Model | The data model, founded by Codd, that represents data as relations (tables) governed by set theory and predicate logic. |
| Replication | The maintenance of copies of data across nodes for availability, durability, and read scaling. |
| Retention | The policy-defined period for which a class of data must be kept before it may be archived or purged. |
| Rollback | The undoing of a transaction's changes so the database returns to its prior consistent state. |
| Row | A single record in a table, holding one value per column. |
| Schema | The formal definition of tables, columns, types, keys, and constraints in a database. |
| Sharding | Horizontal partitioning of data across independent database instances by a shard key. |
| Slowly Changing Dimension (SCD) | A dimension whose attribute changes are tracked over time using a defined strategy (Type 1, 2, or 3). |
| Soft Delete | The marking of a row as deleted (for example, via a deleted-at timestamp) instead of physically removing it. |
| Surrogate Key | A system-generated, meaningless identifier used as a primary key in place of a natural key. |
| Tenant Key | The column that scopes a row to a tenant, enforcing multi-tenant isolation. |
| Transaction | A unit of work executed atomically against the database, committed or rolled back as a whole. |
| Transactional Data | The event-level records of business operations (orders, invoices, payments, movements). |
| Trigger | Procedural logic the database executes automatically in response to a data-modifying event. |
| Unique Constraint | A rule that guarantees no two rows share the same value in the constrained column or columns. |
| View | A named, stored query presented as a virtual table without persisting its result. |

## Cross-References

- [Database Standards](/docs/blueprint/volume-09-database/section-a-database-foundations/03-database-standards.md)
- [Database Terminology](/docs/blueprint/volume-09-database/appendices/database-terminology.md)
- [ER Diagram Catalog](/docs/blueprint/volume-09-database/appendices/er-diagram-catalog.md)

## References

- [Volume 01 - Vision and Philosophy](/docs/blueprint/volume-01-vision-and-philosophy/README.md)
- [Document Standards](/docs/governance/document-standards.md)

## Change Log

| Version | Date | Author | Notes |
|---|---|---|---|
| 1.0 | 2026-07-12 | Lead Software Engineer | Initial approved version. |
