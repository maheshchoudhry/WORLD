# Volume 05 - ERP Terminology

| Field | Value |
|---|---|
| Document ID | WORLD-VOL05-A2 |
| Title | ERP Terminology |
| Version | 1.0 |
| Status | Approved |
| Classification | Internal |
| Founder | Mahesh Choudhary |

## Purpose

This appendix defines the controlled vocabulary of canonical WORLD ERP terms. Where the ERP Glossary (WORLD-VOL05-A1) explains what concepts mean, this document governs how they are named. It establishes the single approved term for each concept, the contexts in which it applies, and the deprecated or ambiguous terms that must be avoided. Consistent terminology across code, documents, APIs, data models, and user interfaces reduces cognitive load and prevents integration defects.

## Scope

This controlled vocabulary applies to all WORLD ERP artifacts: source code identifiers, database schemas, event and API contracts, configuration, documentation, and user-facing copy. It is normative: the approved term is mandatory in new work and preferred when refactoring existing work. It does not redefine concepts already defined in the Glossary; it selects and enforces the canonical label for each.

## Naming Principles

| Principle | Description |
|---|---|
| One concept, one term | Each business concept has exactly one approved canonical term. Synonyms are deprecated. |
| Business language first | Terms reflect ubiquitous business language, not implementation detail. |
| Singular for entities | Entity and object names are singular (Order, not Orders); collections are named explicitly. |
| No abbreviations in public contracts | Public APIs and events spell terms in full; well-known acronyms (GL, BOM, PO) are permitted where established. |
| Tenant-neutral | Terms never embed a specific customer, industry, or deployment name. |

## Controlled Vocabulary

| Concept | Approved Canonical Term | Terms to Avoid | Approved Usage Notes |
|---|---|---|---|
| The isolated instance serving one customer organization | Tenant | Client, Instance, Account, Org | Use "Tenant" for isolation boundary; "Organization" only for the business entity within a tenant. |
| A party that buys from the organization | Customer | Client, Buyer, Account (as customer) | "Account" is reserved for financial accounts only. |
| A party that supplies the organization | Vendor | Supplier, Seller, Merchant | Standardize on "Vendor" across all modules. |
| A tradable or stockable item | Material | Product, Item, Article, SKU | "Product" is the sellable presentation of a Material; "SKU" is a stock identifier, not the item concept. |
| A recorded business transaction record | Document | Record, Voucher, Entry, Slip | "Document" for the business record; "Journal Entry" only for GL postings. |
| The act of recording to the ledger | Posting | Booking, Recording, Entering | Use the verb "to post" and noun "Posting". |
| An operational production or storage location | Plant | Site, Facility, Branch | "Plant" for the operational unit; "Site" is deprecated. |
| A managed storage facility | Warehouse | Depot, Store, Stockroom | Use "Warehouse"; subdivisions are "Storage Location". |
| Cost-collecting internal unit | Cost Center | Cost Pool, Department (as cost unit) | "Department" is an HR concept; use "Cost Center" for controlling. |
| Revenue-and-cost responsible unit | Profit Center | Business Unit (as profit unit), P&L Center | Use "Profit Center" for internal profitability. |
| Stable shared reference entities | Master Data | Static Data, Base Data, Setup Data | "Reference Data" is the narrower subset of code lists. |
| A published statement that an event occurred | Domain Event | Message, Signal, Notification, Trigger | "Domain Event" in contracts; "Notification" only for user-facing alerts. |
| A deployable capability boundary | Module | Component, Subsystem, App | "Module" at business-capability level; "Service" at deployable-unit level. |
| The customer purchase commitment | Purchase Order | Indent, Requisition (as PO), PO Request | "Purchase Requisition" precedes and differs from "Purchase Order". |
| The customer sale commitment | Sales Order | Sale, Booking, Deal | Use "Sales Order"; "Deal" belongs to CRM, not ERP fulfillment. |
| The controlled routing of work | Workflow | Process (as automation), Flow, Pipeline | "Workflow" for orchestrated tasks; "Process" for the broader business process. |
| An authorization decision step | Approval | Sign-off, Sanction, Clearance | Use "Approval"; the authorized role grants an "Approval". |

## Casing And Formatting Conventions

| Context | Convention | Example |
|---|---|---|
| Business object names (docs) | Title case, singular | Sales Order |
| Code type identifiers | PascalCase | SalesOrder |
| Event names | PascalCase, past tense | SalesOrderConfirmed |
| API resource paths | lower kebab-case, plural | /sales-orders |
| Fields and attributes | camelCase | postingDate |
| Enumerations / codes | UPPER_SNAKE_CASE | GOODS_RECEIPT |

## Governance

Proposed additions or changes to this controlled vocabulary are submitted to the ERP architecture review. An approved change updates this appendix, increments its version, and is recorded in the Change Log. Until a term is approved here, contributors use the nearest existing approved term rather than coining a new one.

## Cross-References

- [ERP Glossary](/docs/blueprint/volume-05-erp-foundation/appendices/erp-glossary.md)
- [ERP Design Standards](/docs/blueprint/volume-05-erp-foundation/appendices/erp-design-standards.md)
- [Enterprise Data Standards](/docs/blueprint/volume-05-erp-foundation/appendices/enterprise-data-standards.md)

## References

- [Volume 01 - Vision and Philosophy](/docs/blueprint/volume-01-vision-and-philosophy/README.md)
- [Document Standards](/docs/governance/document-standards.md)

## Change Log

| Version | Date | Author | Summary |
|---|---|---|---|
| 1.0 | 2026-07-12 | Lead Software Engineer | Initial approved version. |
