# Volume 09 - Naming & Coding Conventions

| Field | Value |
|---|---|
| Document ID | WORLD-VOL09-A6 |
| Title | Naming & Coding Conventions |
| Version | 1.0 |
| Status | Approved |
| Classification | Internal |
| Founder | Mahesh Choudhary |

## Purpose

This appendix defines the naming and coding conventions for every database object in Project WORLD: tables, columns, keys, indexes, constraints, and the business coding and numbering schemes that appear as data. Its purpose is to make the schema legible at a glance and safe to automate. Predictable names let an engineer infer an object's role from its name, let tooling generate and validate objects mechanically, and let the AI Business Partner navigate the model without a lookup.

## Scope

The document covers object naming conventions for relational database structures and the standard patterns for business codes and document numbering. It applies to all schemas across the seven data categories. It is expressed logically and is vendor-neutral. It does not cover logical data types or key strategy (governed by Appendix A5) nor terminology in prose (governed by Appendix A2). Conformance is mandatory for all migrations and models contributing to Volume 09.

## General Rules

| Rule | Standard |
|---|---|
| Case | `snake_case` for all identifiers; all lower case. |
| Language | English; use full words, not abbreviations, unless the abbreviation is standard. |
| Singular vs plural | Table names are singular (`customer`, not `customers`). |
| Reserved words | Never use SQL reserved words as identifiers. |
| Length | Keep identifiers within the shortest portable limit; avoid truncation. |
| Separators | Use underscores between words; never spaces, camelCase, or hyphens. |
| Booleans | Prefix boolean columns with `is_`, `has_`, or `can_`. |

## Table and Column Naming

| Object | Convention | Example |
|---|---|---|
| Table | Singular noun, snake_case. | `sales_order` |
| Associative (junction) table | Both entity names joined. | `user_role` |
| History table | Base name with `_history` suffix. | `sales_order_history` |
| Column | Singular, descriptive, snake_case. | `order_date` |
| Primary-key column | `<entity>_id`. | `sales_order_id` |
| Foreign-key column | `<referenced_entity>_id`. | `customer_id` |
| Code column | `<attribute>_code`. | `currency_code` |
| Amount column | `<attribute>_amount`. | `total_amount` |
| Timestamp column | `<event>_at`. | `created_at` |
| Boolean column | `is_/has_/can_<attribute>`. | `is_active` |

## Constraint and Index Naming

Constraint and index names encode their type through a standard prefix so their purpose is unambiguous.

| Object | Prefix | Pattern | Example |
|---|---|---|---|
| Primary key | `pk_` | `pk_<table>` | `pk_sales_order` |
| Foreign key | `fk_` | `fk_<table>_<ref_table>` | `fk_sales_order_customer` |
| Unique constraint | `ux_` | `ux_<table>_<columns>` | `ux_sales_order_number` |
| Check constraint | `ck_` | `ck_<table>_<rule>` | `ck_sales_order_amount_nonneg` |
| Non-unique index | `ix_` | `ix_<table>_<columns>` | `ix_sales_order_customer` |
| Partial index | `ix_` | `ix_<table>_<columns>` (with predicate) | `ix_sales_order_active` |
| Default constraint | `df_` | `df_<table>_<column>` | `df_sales_order_status` |
| Trigger | `tg_` | `tg_<table>_<event>` | `tg_sales_order_audit` |

## Schema and View Naming

| Object | Convention | Example |
|---|---|---|
| Schema | Domain or category name, snake_case. | `sales`, `reference`, `audit` |
| View | `v_<subject>`. | `v_open_sales_order` |
| Materialized view | `mv_<subject>`. | `mv_daily_sales_summary` |
| Sequence | `seq_<table>`. | `seq_sales_order` |
| Function | `fn_<action>`. | `fn_calculate_order_total` |

## Business Coding and Numbering Schemes

Business codes and document numbers are data, not schema, and follow their own standards to remain stable, sortable, and human-readable.

| Scheme | Convention | Example |
|---|---|---|
| Reference code | Short, uppercase, stable, meaningful. | `USD`, `IN`, `KG` |
| Status code | Lowercase, snake_case, from an approved set. | `confirmed`, `fulfilled` |
| Document number | `<PREFIX>-<YYYY>-<sequence>`, zero-padded sequence, unique per tenant and company. | `SO-2026-000123` |
| Document prefix | Two-to-four uppercase letters identifying the document type. | `SO`, `INV`, `PO`, `GRN` |
| Entity business key | Uppercase code, no embedded volatile data. | `CUST-000045` |
| Sequence reset | Document sequences reset per year and per company where required. | annual reset |
| Check character | Optional trailing check digit for externally shared codes. | `CUST-000045-7` |

## Cross-References

- [Database Standards](/docs/blueprint/volume-09-database/section-a-database-foundations/03-database-standards.md)
- [Data Standards](/docs/blueprint/volume-09-database/appendices/data-standards.md)
- [Database Terminology](/docs/blueprint/volume-09-database/appendices/database-terminology.md)

## References

- [Volume 01 - Vision and Philosophy](/docs/blueprint/volume-01-vision-and-philosophy/README.md)
- [Document Standards](/docs/governance/document-standards.md)

## Change Log

| Version | Date | Author | Notes |
|---|---|---|---|
| 1.0 | 2026-07-12 | Lead Software Engineer | Initial approved version. |
