# Volume 06 - Module Templates

| Field | Value |
|---|---|
| Document ID | WORLD-VOL06-A3 |
| Title | Module Templates |
| Version | 1.0 |
| Status | Approved |
| Classification | Internal |
| Founder | Mahesh Choudhary |

## Purpose

This appendix provides the reusable authoring templates that keep every business module in Volume 06 consistent, complete, and enterprise-grade. It defines the standard 19-section module documentation template and three supporting specification templates: the master-data specification, the transaction specification, and the KPI specification. Authors copy these templates as the starting point for new or revised module documentation.

## Scope

The templates govern the structure and required content of module chapters and their embedded specifications within Volume 06. They standardize headings, tables, and field sets so that modules are directly comparable. They do not prescribe physical database schemas (see Volume 09) nor UI design specifications; they define the documentation contract that each module chapter must satisfy.

## 1. Standard Module Documentation Template

Every module chapter follows this 19-section structure in the order shown. Each section is mandatory; where a section does not apply, authors state "Not applicable" with a brief justification rather than omitting the heading.

| # | Section | Required Content |
|---|---|---|
| 1 | Purpose | The business reason the module exists and the capability it delivers. |
| 2 | Business Value | The measurable value and outcomes the module creates for the organization. |
| 3 | Objectives | The specific goals the module is designed to achieve. |
| 4 | Responsibilities | The functional responsibilities owned by the module. |
| 5 | Business Process | The end-to-end process the module supports, with a process narrative. |
| 6 | Master Data | The reference entities the module owns or consumes (see Section 2 template). |
| 7 | Transactions | The transactional documents and events the module produces (see Section 3 template). |
| 8 | Business Rules | The validation, control, and policy rules the module enforces. |
| 9 | Workflow | The orchestrated approval and processing flow, with a Mermaid diagram. |
| 10 | Inputs | The data, events, and documents the module receives from other modules. |
| 11 | Outputs | The data, events, and documents the module publishes to other modules. |
| 12 | Dependencies | The upstream and downstream modules the module relies on or serves. |
| 13 | KPIs | The key performance indicators the module owns (see Section 4 template). |
| 14 | Reports | The standard operational and statutory reports the module produces. |
| 15 | Dashboards | The role-based dashboards and visual analytics the module surfaces. |
| 16 | Roles | The business roles that interact with the module. |
| 17 | Permissions | The access levels granted to each role, aligned with RBAC. |
| 18 | AI Features | The embedded AI capabilities and how they assist users. |
| 19 | Future Expansion | Planned enhancements and extension points. |

### 1.1 Section Skeleton (copy-ready)

```markdown
## Purpose
<One paragraph: why this module exists and the capability it delivers.>

## Business Value
<Bullet list of measurable outcomes.>

## Objectives
<Numbered list of specific goals.>

## Responsibilities
<Bullet list of functional responsibilities owned by the module.>

## Business Process
<Narrative of the end-to-end process, followed by a step table.>

## Master Data
<Master-data specification table(s) per Section 2.>

## Transactions
<Transaction specification table(s) per Section 3.>

## Business Rules
<Rule table: Rule ID, Rule, Enforcement, Rationale.>

## Workflow
<Mermaid flowchart plus a step description.>

## Inputs
<Table: Source Module, Data or Event, Purpose.>

## Outputs
<Table: Target Module, Data or Event, Purpose.>

## Dependencies
<Table: Module, Direction, Dependency Description.>

## KPIs
<KPI specification table(s) per Section 4.>

## Reports
<Table: Report, Purpose, Audience.>

## Dashboards
<Table: Dashboard, Audience, Key Widgets.>

## Roles
<Table: Role, Description.>

## Permissions
<Table: Role, Access Level, Notes.>

## AI Features
<Table: Feature, Description, Human Oversight.>

## Future Expansion
<Bullet list of planned enhancements and extension points.>

## Cross-References
<2-4 links within Volume 06.>

## References
<Links to Volume 01 README and Document Standards.>

## Change Log
| Version | Date | Author | Summary |
|---|---|---|---|
| 1.0 | <date> | Lead Software Engineer | Initial approved version. |
```

## 2. Master-Data Specification Template

Use this template to document each master-data entity a module owns or consumes.

| Attribute | Description |
|---|---|
| Entity Name | Canonical name of the master-data entity. |
| Owning Module | The single module responsible for the entity's lifecycle. |
| Purpose | The business role the entity plays. |
| Key Identifier | The unique business key for the entity. |
| Core Attributes | The essential fields that define the entity. |
| Lifecycle States | The valid statuses and permitted transitions. |
| Governing Rules | Validation and uniqueness rules that apply. |
| Consumers | Modules that read the entity. |

### 2.1 Worked Example - Vendor (owned by Procurement)

| Attribute | Value |
|---|---|
| Entity Name | Vendor |
| Owning Module | Procurement |
| Purpose | Represents an external party supplying goods or services. |
| Key Identifier | Vendor ID |
| Core Attributes | Legal name, tax identifier, payment terms, currency, status. |
| Lifecycle States | Draft, Active, Blocked, Inactive. |
| Governing Rules | Unique tax identifier; approval required to activate. |
| Consumers | Inventory, Accounting, Banking, Finance. |

## 3. Transaction Specification Template

Use this template to document each transactional document a module produces.

| Attribute | Description |
|---|---|
| Transaction Name | Canonical name of the transaction document. |
| Owning Module | The module that creates and controls the transaction. |
| Trigger | The event or request that initiates the transaction. |
| Header Fields | Key document-level fields. |
| Line Fields | Key line-item fields. |
| Lifecycle States | Valid statuses and permitted transitions. |
| Postings or Effects | Financial or inventory effects produced. |
| Emitted Events | Domain events published on state change. |

### 3.1 Worked Example - Purchase Order (owned by Procurement)

| Attribute | Value |
|---|---|
| Transaction Name | Purchase Order |
| Owning Module | Procurement |
| Trigger | Approved purchase requisition. |
| Header Fields | PO number, vendor, currency, delivery date, status. |
| Line Fields | Item, quantity, unit price, tax, expected date. |
| Lifecycle States | Draft, Approved, Sent, Received, Closed, Cancelled. |
| Postings or Effects | Commitment recorded; goods receipt updates inventory. |
| Emitted Events | PurchaseOrderApproved, PurchaseOrderReceived. |

## 4. KPI Specification Template

Use this template to document each KPI a module owns.

| Attribute | Description |
|---|---|
| KPI Name | Canonical name of the metric. |
| Owning Module | The module accountable for the metric. |
| Definition | Plain-language meaning of the metric. |
| Formula | The calculation, with inputs named. |
| Unit | The unit of measure (percentage, days, count, currency). |
| Frequency | The measurement cadence. |
| Target Direction | Whether higher or lower is better. |
| Data Source | The transactions or entities the metric is derived from. |

### 4.1 Worked Example - On-Time Delivery (owned by Logistics)

| Attribute | Value |
|---|---|
| KPI Name | On-Time Delivery |
| Owning Module | Logistics |
| Definition | Share of deliveries completed on or before the promised date. |
| Formula | (On-time deliveries / Total deliveries) x 100 |
| Unit | Percentage |
| Frequency | Daily and monthly |
| Target Direction | Higher is better |
| Data Source | Dispatch and delivery confirmations. |

## Cross-References

- [Module Terminology](/docs/blueprint/volume-06-business-modules/appendices/module-terminology.md)
- [KPI Catalog](/docs/blueprint/volume-06-business-modules/appendices/kpi-catalog.md)
- [Workflow Templates](/docs/blueprint/volume-06-business-modules/appendices/workflow-templates.md)

## References

- [Volume 01 - Vision and Philosophy](/docs/blueprint/volume-01-vision-and-philosophy/README.md)
- [Document Standards](/docs/governance/document-standards.md)

## Change Log

| Version | Date | Author | Summary |
|---|---|---|---|
| 1.0 | 2026-07-12 | Lead Software Engineer | Initial approved version. |
