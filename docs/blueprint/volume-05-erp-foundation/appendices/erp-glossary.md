# Volume 05 - ERP Glossary

| Field | Value |
|---|---|
| Document ID | WORLD-VOL05-A1 |
| Title | ERP Glossary |
| Version | 1.0 |
| Status | Approved |
| Classification | Internal |
| Founder | Mahesh Choudhary |

## Purpose

This appendix provides an alphabetized, authoritative glossary of Enterprise Resource Planning (ERP) terms used throughout Volume 05 - ERP Foundation. It establishes a shared understanding of core concepts so that architects, engineers, and business stakeholders working on WORLD's operational layer interpret terminology consistently. Definitions are written to be precise, tool-agnostic, and applicable to WORLD's AI-Native Business Operating System.

## Scope

The glossary covers foundational ERP vocabulary spanning master data, transactions, organizational structures, financial accounting, logistics, and multi-tenancy. It defines terms as they are used within WORLD's ERP framework. It does not define WORLD-specific canonical naming conventions (see WORLD-VOL05-A2, ERP Terminology) nor design or data standards (see WORLD-VOL05-A3 and WORLD-VOL05-A4). Terms are listed once at their most natural entry point.

## Glossary

| Term | Definition |
|---|---|
| Accounting Period | A defined interval of time (typically a month or quarter) for which financial transactions are grouped, closed, and reported. |
| Aggregate | A cluster of domain objects treated as a single consistency boundary for data changes, with one root entity governing access. |
| Approval Matrix | A structured mapping of transaction types and value thresholds to the roles authorized to approve them. |
| Bill of Materials (BOM) | A structured list of components, sub-assemblies, and quantities required to manufacture or assemble a finished product. |
| Business Object | A named, persistent representation of a real-world business concept (for example, Order, Invoice, Product) with defined attributes and behavior. |
| Chart of Accounts (COA) | The organized, coded list of all General Ledger accounts available for recording financial transactions in an organization. |
| Company Code | The smallest organizational unit for which a complete, self-contained set of accounts can be maintained for external reporting. |
| Cost Center | An organizational unit to which costs are assigned for internal accounting and controlling, without directly generating revenue. |
| Document | A persistent record of a business transaction or event, carrying a unique identifier, header, and line items. |
| Document Flow | The linked chain of related documents that trace a business process end to end (for example, quotation to order to delivery to invoice). |
| Document Type | A classification that governs a document's numbering, allowed accounts, field behavior, and posting rules. |
| Dunning | The systematic process of communicating with customers to collect overdue receivables. |
| Enterprise Resource Planning (ERP) | An integrated system of applications and shared data that manages an organization's core operational and financial processes. |
| Event | An immutable statement that something of business significance has occurred, published for other components to react to. |
| Fiscal Year | The 12-month period an organization uses for financial reporting, which may differ from the calendar year. |
| General Ledger (GL) | The central accounting record that consolidates all financial postings into accounts for producing statutory financial statements. |
| Goods Issue | The logistics transaction recording that materials have left inventory, reducing stock and typically triggering a financial posting. |
| Goods Receipt | The logistics transaction recording that materials have entered inventory, increasing stock and updating valuation. |
| Idempotency | The property whereby processing the same request or event more than once produces the same result as processing it exactly once. |
| Journal Entry | A recorded financial posting consisting of balanced debit and credit line items affecting General Ledger accounts. |
| Ledger | A book or store of accounts in which financial postings are recorded and balanced. |
| Master Data | Relatively stable, shared reference data describing core entities such as customers, vendors, materials, and accounts. |
| Material | A tradable or manageable item (raw material, semi-finished, or finished good) tracked in inventory and planning. |
| Movement Type | A code that classifies an inventory movement and determines its stock and accounting effects. |
| Organizational Unit | A structural element (company code, plant, warehouse, sales area) that models an enterprise's operational hierarchy. |
| Period-End Close | The controlled process of finalizing, reconciling, and locking transactions for an accounting period. |
| Plant | An operational location where goods are produced, stored, or from which services are provided. |
| Posting | The act of recording a transaction into the General Ledger or a subsidiary ledger, updating account balances. |
| Posting Date | The date on which a transaction is recognized in the accounting records, determining its accounting period. |
| Profit Center | An organizational unit responsible for both revenues and costs, used to measure internal profitability. |
| Purchase Order (PO) | A formal, authorized commitment issued to a vendor to supply specified goods or services at agreed terms. |
| Reconciliation | The process of comparing two sets of records to confirm they agree and to resolve discrepancies. |
| Reference Data | Standardized code lists and lookup values (currencies, units of measure, country codes) shared across the system. |
| Sales Order | A confirmed customer request to deliver specified goods or services, initiating the order-to-cash process. |
| Segregation of Duties (SoD) | A control principle that distributes critical steps of a process across different people or roles to prevent fraud and error. |
| Service (Application) | A deployable unit that exposes capabilities through well-defined interfaces and owns its data. |
| Stock Keeping Unit (SKU) | A distinct, individually tracked item identifier used to manage inventory at the most granular level. |
| Storage Location | A subdivision of a plant or warehouse where stock is physically held. |
| Subledger | A detailed ledger (for example, accounts payable or receivable) that summarizes into a control account in the General Ledger. |
| Tenant | An isolated logical instance of the system serving a single customer organization, with its own data and configuration. |
| Three-Way Match | A control that verifies purchase order, goods receipt, and invoice agree before an invoice is paid. |
| Transaction | A discrete business event that changes the state of the system and is recorded, often producing one or more documents. |
| Unit of Measure (UoM) | The standardized quantity in which a material is counted, stored, or transacted (each, kilogram, litre). |
| Valuation | The monetary value assigned to inventory or assets according to defined accounting rules. |
| Vendor | An external party that supplies goods or services to the organization; also referred to as a supplier. |
| Warehouse | A facility or managed space for receiving, storing, and dispatching materials, often with bin-level management. |
| Workflow | A defined sequence of tasks, decisions, and approvals that moves a business process toward completion. |

## Cross-References

- [Volume 05 - ERP Foundation Overview](/docs/blueprint/volume-05-erp-foundation/README.md)
- [ERP Terminology](/docs/blueprint/volume-05-erp-foundation/appendices/erp-terminology.md)
- [ERP Design Standards](/docs/blueprint/volume-05-erp-foundation/appendices/erp-design-standards.md)

## References

- [Volume 01 - Vision and Philosophy](/docs/blueprint/volume-01-vision-and-philosophy/README.md)
- [Document Standards](/docs/governance/document-standards.md)

## Change Log

| Version | Date | Author | Summary |
|---|---|---|---|
| 1.0 | 2026-07-12 | Lead Software Engineer | Initial approved version. |
