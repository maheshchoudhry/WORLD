# Volume 06 - Module Terminology

| Field | Value |
|---|---|
| Document ID | WORLD-VOL06-A2 |
| Title | Module Terminology |
| Version | 1.0 |
| Status | Approved |
| Classification | Internal |
| Founder | Mahesh Choudhary |

## Purpose

This appendix defines the controlled vocabulary for WORLD's business modules: the canonical module names, the approved terms for core module concepts, and the terms to avoid. It ensures that documentation, user interfaces, APIs, and conversations reference each module and concept by a single, consistent name across all 32 modules and eight domain sections.

## Scope

The controlled vocabulary governs module naming, cross-module process names, and shared concept labels used in Volume 06. It complements the definitions in WORLD-VOL06-A1 (Business Module Glossary) by specifying which term is canonical and which alternatives are deprecated. It aligns with the ERP-foundation terminology of Volume 05 and does not override statutory or regulatory terms where those are legally required.

## Naming Principles

| Principle | Description |
|---|---|
| One canonical name | Each module and concept has exactly one approved name; synonyms are documented and deprecated. |
| Business-first language | Names reflect the business capability, not the underlying technology or vendor. |
| Singular module names | Module names are expressed as the capability domain (for example, Procurement, not Procurements). |
| Stable across layers | The same canonical name is used in documentation, UI labels, API resources, and analytics. |
| Domain-scoped clarity | Where a term is ambiguous across domains, it is qualified by its domain (for example, Sales Order vs. Purchase Order). |

## Canonical Module Names

| Section | Canonical Module Name | Approved Usage | Terms to Avoid |
|---|---|---|---|
| A | Procurement | Sourcing and purchasing of goods and services. | Purchasing module, Buying |
| A | Inventory | Management of stock quantities, valuation, and movements. | Stock module, Materials |
| A | Warehouse | Physical storage, bin management, pick-pack operations. | Store, Godown module |
| A | Logistics | Transportation planning and carrier management. | Transport module, Shipping |
| A | Dispatch | Release and hand-off of goods for delivery. | Despatch, Outbound module |
| B | CRM | Lead, contact, account, and opportunity management. | Customer module, Contacts app |
| B | Sales | Quotation, sales order, and fulfilment coordination. | Selling, Order module |
| B | POS | In-person retail point-of-sale transactions. | Till, Cash register module |
| B | E-Commerce | Online storefront and digital order capture. | Web store, Online shop module |
| C | Production | Execution of production orders on the shop floor. | Make module, Factory |
| C | Production Planning | Demand-driven scheduling and material planning. | Planning module, PP |
| C | Manufacturing | Discrete and process manufacturing operations. | Mfg, Works module |
| C | Quality | Inspection, non-conformance, and quality control. | QA module, QC app |
| C | Maintenance | Asset upkeep and work-order-based servicing. | Repairs module, PM |
| D | Finance | Financial control, ledgers, and reporting oversight. | Fin module, Money |
| D | Accounting | Journal posting, subledgers, and reconciliation. | Bookkeeping module, Accts |
| D | Banking | Bank accounts, statements, and reconciliation. | Bank module, Treasury app |
| D | Budgeting | Financial planning, allocation, and variance control. | Budgets app, Planning finance |
| D | Assets | Fixed-asset lifecycle and depreciation. | Fixed Assets app, FA module |
| E | HR | Employee master data and organizational structure. | Personnel module, HRMS |
| E | Payroll | Compensation calculation and disbursement. | Salary module, Pay app |
| E | Attendance | Time capture and shift adherence. | Timesheet module, T&A |
| E | Recruitment | Hiring pipeline from requisition to onboarding. | Hiring module, TA app |
| F | Projects | Project structure, planning, and delivery. | Project management app, PM office |
| F | Task Management | Task assignment, tracking, and completion. | To-do module, Tasks app |
| F | Documents | Document storage, versioning, and control. | Files module, DMS app |
| G | Workflow | Orchestration of multi-step business processes. | Process engine app, BPM |
| G | Approvals | Authorization gates and approval matrices. | Sign-off module, Authorizations |
| G | Notifications | Event-driven alerts and messaging. | Alerts module, Messaging app |
| H | Reporting | Operational and statutory report generation. | Reports app, MIS |
| H | Dashboards | Interactive, role-based visual analytics. | KPI screens, Dash app |
| H | AI Integration | Embedding AI capabilities across modules. | AI module, ML app |

## Cross-Module Process Terms

| Canonical Process Name | Approved Usage | Terms to Avoid |
|---|---|---|
| Procure-to-Pay (P2P) | Requisition through vendor payment. | Purchase-to-pay, PTP |
| Order-to-Cash (O2C) | Customer order through cash collection. | Sale-to-cash, OTC |
| Hire-to-Retire (H2R) | Recruitment through employee separation. | Recruit-to-retire, HTR |
| Plan-to-Produce (P2Prod) | Planning through manufactured output. | Plan-to-make, PTM |
| Record-to-Report (R2R) | Transaction posting through financial reporting. | Close-to-report, RTR |

## Concept Term Standards

| Concept | Canonical Term | Terms to Avoid |
|---|---|---|
| Internal purchase request | Purchase Requisition | Indent, Purchase request note |
| Vendor commitment document | Purchase Order | Supply order, PO note |
| Confirmed customer demand | Sales Order | Customer order, Booking |
| Stock unit identifier | SKU | Item code (as label), Part no. |
| Replenishment trigger level | Reorder Point | Min level, Order level |
| External supplier party | Vendor | Supplier (in labels), Party |
| Buyer-side counterparty | Customer | Client (in labels), Buyer |
| Performance measure | KPI | Metric (as heading), Measure |

## Cross-References

- [Business Module Glossary](/docs/blueprint/volume-06-business-modules/appendices/business-module-glossary.md)
- [Module Templates](/docs/blueprint/volume-06-business-modules/appendices/module-templates.md)
- [Integration Map](/docs/blueprint/volume-06-business-modules/appendices/integration-map.md)

## References

- [Volume 01 - Vision and Philosophy](/docs/blueprint/volume-01-vision-and-philosophy/README.md)
- [Document Standards](/docs/governance/document-standards.md)

## Change Log

| Version | Date | Author | Summary |
|---|---|---|---|
| 1.0 | 2026-07-12 | Lead Software Engineer | Initial approved version. |
