# Volume 09 - Data Standards

| Field | Value |
|---|---|
| Document ID | WORLD-VOL09-A5 |
| Title | Data Standards |
| Version | 1.0 |
| Status | Approved |
| Classification | Internal |
| Founder | Mahesh Choudhary |

## Purpose

This appendix defines the data standards that every entity in Project WORLD must observe: the canonical data types, the key strategy, the standard system columns, the tenancy columns, and the representation of currency and units. Its purpose is to make the data tier uniform and predictable. When every table applies the same standards for identifiers, timestamps, soft deletion, and tenant scoping, the model becomes composable, auditable, and safe to evolve, and the AI Business Partner can reason about any table from its shape alone.

## Scope

The document covers logical data-type standards, key standards, system and audit columns, tenancy and isolation columns, and value-representation standards for currency, quantity, and units. It is expressed logically and is vendor-neutral; concrete physical type mappings are resolved per store within these constraints. It applies to all persistent entities across the seven data categories. It does not cover naming rules (governed by Appendix A6) nor physical performance structures (governed by Sections C and D).

## Data Type Standards

| Logical Type | Standard Representation | Rule |
|---|---|---|
| Identifier (surrogate) | `bigint` identity or `uuid` | One identifier strategy per store, applied consistently. |
| Short text | `varchar(n)` with explicit length | Always bound length; never unbounded text for codes or names. |
| Long text | `text` | Reserved for free-form, non-indexed narrative content. |
| Boolean | `boolean` | Use true/false; never 0/1 integers or Y/N characters. |
| Integer | `int` / `bigint` | Choose width by domain range; default `int`. |
| Decimal / money | `numeric(precision, scale)` | Never use floating point for monetary or exact values. |
| Date | `date` | Calendar date without time. |
| Timestamp | `timestamptz` | Always timezone-aware, stored in UTC. |
| Enumerated status | `varchar` with check constraint | Constrain to an approved value set; document the values. |
| JSON document | `jsonb` | For schemaless extension only; not a substitute for modeling. |

## Key Standards

| Standard | Rule | Rationale |
|---|---|---|
| Surrogate primary key | Every entity has a single-column, system-generated primary key. | Stable identity independent of business change. |
| Surrogate vs natural | Use a Surrogate Key as the primary key; enforce the Natural Key with a unique constraint. | Combines stability with business uniqueness. |
| Foreign keys explicit | Every relationship is enforced by a declared foreign key. | Guarantees referential integrity in the database. |
| No business meaning in PK | Primary keys carry no encoded business semantics. | Prevents coupling identity to changeable data. |
| Composite keys avoided as PK | Use composite keys only for associative uniqueness, not as primary key. | Simplifies joins and foreign-key references. |
| Immutable keys | Primary key values are never updated. | Referential stability across the model. |

## System and Audit Columns

Every persistent entity includes the following standard columns unless explicitly exempted.

| Column | Type | Rule |
|---|---|---|
| `created_at` | `timestamptz` | Set once on insert, in UTC; never modified. |
| `created_by` | `uuid` / `bigint` | Identity of the principal that created the row. |
| `updated_at` | `timestamptz` | Set on every modification, in UTC. |
| `updated_by` | `uuid` / `bigint` | Identity of the principal that last modified the row. |
| `deleted_at` | `timestamptz` (nullable) | Soft-delete marker; null means active. Physical deletes are exceptional. |
| `version` | `int` / `bigint` | Optimistic-concurrency token incremented on each update. |

## Tenancy and Isolation Columns

| Column | Type | Rule |
|---|---|---|
| `tenant_id` | `uuid` | Present on every tenant-scoped entity; enforces multi-tenant isolation. |
| `company_id` | `uuid` | Present where legal-entity isolation within a tenant is required. |
| Isolation enforcement | - | Every query is scoped by `tenant_id`; enforced by policy, not left to callers. |
| Uniqueness scope | - | Business-natural uniqueness is scoped within `tenant_id` (and `company_id` where relevant). |
| Cross-tenant reference | - | Foreign keys never cross a tenant boundary. |

## Currency, Quantity, and Unit Standards

| Standard | Rule |
|---|---|
| Currency code | Store an ISO 4217 alphabetic code (`char(3)`) alongside every monetary amount. |
| Monetary amount | Store as `numeric` with sufficient scale (minimum four decimal places); never floating point. |
| Amount + currency pairing | A monetary amount column is always paired with its currency column; amounts are never mixed across currencies without conversion. |
| Quantity | Store as `numeric` with a unit-of-measure code; do not assume a default unit. |
| Unit of measure | Reference a controlled unit code from Reference Data (for example, ISO/UN units). |
| Percentages and rates | Store as `numeric` fractions or explicit basis, with the convention documented. |
| Rounding | Apply a defined rounding policy at calculation boundaries, not at storage. |

## Cross-References

- [Database Standards](/docs/blueprint/volume-09-database/section-a-database-foundations/03-database-standards.md)
- [Naming & Coding Conventions](/docs/blueprint/volume-09-database/appendices/naming-and-coding-conventions.md)
- [Data Dictionary Template](/docs/blueprint/volume-09-database/appendices/data-dictionary-template.md)

## References

- [Volume 01 - Vision and Philosophy](/docs/blueprint/volume-01-vision-and-philosophy/README.md)
- [Document Standards](/docs/governance/document-standards.md)

## Change Log

| Version | Date | Author | Notes |
|---|---|---|---|
| 1.0 | 2026-07-12 | Lead Software Engineer | Initial approved version. |
