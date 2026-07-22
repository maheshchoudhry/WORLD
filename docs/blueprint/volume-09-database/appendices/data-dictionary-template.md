# Volume 09 - Data Dictionary Template

| Field | Value |
|---|---|
| Document ID | WORLD-VOL09-A3 |
| Title | Data Dictionary Template |
| Version | 1.0 |
| Status | Approved |
| Classification | Internal |
| Founder | Mahesh Choudhary |

## Purpose

This appendix provides the reusable template by which every entity in Project WORLD's data model is documented. Its purpose is to make the data model self-describing: each table is accompanied by a precise, uniform specification of its purpose, its columns, their types and constraints, and its keys and relationships. A consistent data dictionary lets engineers, data stewards, and the AI Business Partner understand a table without reading its migration history, and it is the primary input to review, governance, and quality control.

## Scope

The template covers the entity-level and attribute-level specification of a relational table: identity, ownership, data category, keys, columns, constraints, indexes, and relationships. It applies to all persistent entities across the seven data categories. It does not replace the physical migration scripts, which remain the source of truth for deployment, nor the ER Diagram Catalog (Appendix A4), which governs relationship visualization. A filled sample entity follows the blank template to demonstrate the expected level of detail.

## Entity Specification Template

| Field | Description |
|---|---|
| Entity Name | The canonical table name in snake_case. |
| Logical Name | The human-readable name of the entity. |
| Data Category | Master, Reference, Transactional, Operational, Analytical, Knowledge, or Metadata. |
| Owning Domain | The bounded context or module that owns the entity. |
| Data Steward | The role accountable for the entity's definition and quality. |
| Description | One or two sentences stating what one row represents. |
| Primary Key | The column(s) that uniquely identify a row. |
| Tenant Scoping | The tenant/company key columns, if the entity is tenant-scoped. |
| Retention Class | The retention policy governing the entity. |
| Volume Estimate | The expected row count and growth rate. |

### Attribute Specification

| Column | Type | Nullable | Key | Constraints | Default | Description |
|---|---|---|---|---|---|---|
| `<column_name>` | `<type>` | Yes / No | PK / FK / - | Unique / Check / FK target | `<default>` | Meaning of the attribute and any business rule. |

### Relationships

| Relationship | Cardinality | Target Entity | Foreign Key | On Delete |
|---|---|---|---|---|
| `<name>` | one-to-many / many-to-one / many-to-many | `<entity>` | `<column>` | Restrict / Cascade / Set Null |

### Indexes

| Index Name | Columns | Type | Purpose |
|---|---|---|---|
| `<ix_name>` | `<columns>` | B-tree / Unique / Partial | Access pattern the index serves. |

## Sample Entity - `sales_order`

| Field | Description |
|---|---|
| Entity Name | `sales_order` |
| Logical Name | Sales Order |
| Data Category | Transactional |
| Owning Domain | Order Management |
| Data Steward | Order Management Data Steward |
| Description | One row represents a single customer sales order raised within a company and tenant. |
| Primary Key | `sales_order_id` |
| Tenant Scoping | `tenant_id`, `company_id` |
| Retention Class | Transactional-7y (seven-year statutory retention). |
| Volume Estimate | ~2M rows per tenant per year, moderate growth. |

### Attribute Specification

| Column | Type | Nullable | Key | Constraints | Default | Description |
|---|---|---|---|---|---|---|
| `sales_order_id` | `bigint` | No | PK | Identity, surrogate | generated | System-generated unique identifier of the order. |
| `tenant_id` | `uuid` | No | FK | FK -> `tenant.tenant_id` | - | Tenant that owns the row; enforces isolation. |
| `company_id` | `uuid` | No | FK | FK -> `company.company_id` | - | Legal company within the tenant. |
| `order_number` | `varchar(20)` | No | - | Unique per tenant+company | - | Human-readable business number of the order. |
| `customer_id` | `bigint` | No | FK | FK -> `customer.customer_id` | - | Customer that placed the order. |
| `order_date` | `date` | No | - | Check `order_date <= current_date` | - | Business date the order was placed. |
| `status` | `varchar(20)` | No | - | Check in (`draft`,`confirmed`,`fulfilled`,`cancelled`) | `'draft'` | Lifecycle status of the order. |
| `currency_code` | `char(3)` | No | FK | FK -> `currency.currency_code` | - | ISO 4217 currency of the order total. |
| `total_amount` | `numeric(18,4)` | No | - | Check `total_amount >= 0` | `0` | Order total in the order currency. |
| `created_at` | `timestamptz` | No | - | - | `now()` | Instant the row was created. |
| `updated_at` | `timestamptz` | No | - | - | `now()` | Instant the row was last modified. |
| `deleted_at` | `timestamptz` | Yes | - | Soft-delete marker | `null` | Instant the row was soft-deleted; null means active. |

### Relationships

| Relationship | Cardinality | Target Entity | Foreign Key | On Delete |
|---|---|---|---|---|
| places | many-to-one | `customer` | `customer_id` | Restrict |
| contains | one-to-many | `sales_order_line` | `sales_order_id` | Cascade |
| denominated_in | many-to-one | `currency` | `currency_code` | Restrict |

### Indexes

| Index Name | Columns | Type | Purpose |
|---|---|---|---|
| `pk_sales_order` | `sales_order_id` | Unique | Primary key access. |
| `ux_sales_order_number` | `tenant_id, company_id, order_number` | Unique | Enforce business-number uniqueness per company. |
| `ix_sales_order_customer` | `tenant_id, customer_id` | B-tree | Retrieve orders for a customer. |
| `ix_sales_order_active` | `tenant_id, status` | Partial (`deleted_at IS NULL`) | Query active orders by status efficiently. |

## Cross-References

- [Entity Relationship Strategy](/docs/blueprint/volume-09-database/section-c-data-modeling/12-entity-relationship-strategy.md)
- [ER Diagram Catalog](/docs/blueprint/volume-09-database/appendices/er-diagram-catalog.md)
- [Data Standards](/docs/blueprint/volume-09-database/appendices/data-standards.md)

## References

- [Volume 01 - Vision and Philosophy](/docs/blueprint/volume-01-vision-and-philosophy/README.md)
- [Document Standards](/docs/governance/document-standards.md)

## Change Log

| Version | Date | Author | Notes |
|---|---|---|---|
| 1.0 | 2026-07-12 | Lead Software Engineer | Initial approved version. |
