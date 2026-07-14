# Volume 06 - KPI Catalog

| Field | Value |
|---|---|
| Document ID | WORLD-VOL06-A4 |
| Title | KPI Catalog |
| Version | 1.0 |
| Status | Approved |
| Classification | Internal |
| Founder | Mahesh Choudhary |

## Purpose

This appendix consolidates the representative key performance indicators (KPIs) across WORLD's business modules into a single reference. It gives leaders, module owners, and analysts a consistent definition and formula for each metric, and it names the single module accountable for producing it. The catalog supports comparable measurement across domains and feeds the Dashboards and Reporting modules.

## Scope

The catalog lists representative KPIs per module domain (Sections A-H). Each entry specifies the metric, its plain-language definition, its calculation formula, and its owning module. It is not exhaustive; module chapters may define additional KPIs following the KPI specification template in WORLD-VOL06-A3. Metric ownership follows the single-owner principle to prevent conflicting definitions.

## Reading the Catalog

| Column | Meaning |
|---|---|
| Metric | Canonical KPI name. |
| Definition | Plain-language meaning of the metric. |
| Formula | Calculation with named inputs; percentages multiplied by 100. |
| Owning Module | The single module accountable for the metric. |

## Section A - Supply Chain & Procurement

| Metric | Definition | Formula | Owning Module |
|---|---|---|---|
| Purchase Order Cycle Time | Average time from requisition approval to PO issue. | Sum(PO issue - requisition approval) / Number of POs | Procurement |
| Supplier On-Time Rate | Share of vendor deliveries received on or before due date. | (On-time receipts / Total receipts) x 100 | Procurement |
| Inventory Turnover | Number of times inventory is sold and replaced in a period. | Cost of goods sold / Average inventory value | Inventory |
| Stock Accuracy | Agreement between recorded and physically counted stock. | (Accurate count lines / Total count lines) x 100 | Inventory |
| Warehouse Order Fulfilment Rate | Share of orders picked and packed in full. | (Orders fulfilled in full / Total orders) x 100 | Warehouse |
| On-Time Delivery | Share of deliveries completed by the promised date. | (On-time deliveries / Total deliveries) x 100 | Logistics |
| Dispatch Accuracy | Share of dispatches with correct items and quantities. | (Accurate dispatches / Total dispatches) x 100 | Dispatch |

## Section B - Sales & Customer

| Metric | Definition | Formula | Owning Module |
|---|---|---|---|
| Lead Conversion Rate | Share of leads that become won opportunities. | (Won opportunities / Qualified leads) x 100 | CRM |
| Sales Win Rate | Share of closed opportunities that are won. | (Won opportunities / Closed opportunities) x 100 | Sales |
| Average Order Value | Average revenue value per sales order. | Total order revenue / Number of orders | Sales |
| POS Transactions per Hour | Throughput of the point-of-sale terminal. | Number of POS transactions / Operating hours | POS |
| Cart Abandonment Rate | Share of online carts not converted to orders. | (Abandoned carts / Created carts) x 100 | E-Commerce |

## Section C - Manufacturing & Operations

| Metric | Definition | Formula | Owning Module |
|---|---|---|---|
| Production Yield | Share of good units produced against total started. | (Good units / Total units started) x 100 | Production |
| Schedule Adherence | Share of planned orders completed on schedule. | (On-schedule orders / Planned orders) x 100 | Production Planning |
| Overall Equipment Effectiveness (OEE) | Composite of availability, performance, and quality. | Availability x Performance x Quality | Manufacturing |
| First Pass Yield | Share of units passing inspection without rework. | (Units passing first time / Units inspected) x 100 | Quality |
| Mean Time Between Failures (MTBF) | Average operating time between equipment failures. | Total operating time / Number of failures | Maintenance |

## Section D - Finance

| Metric | Definition | Formula | Owning Module |
|---|---|---|---|
| Gross Profit Margin | Share of revenue retained after cost of goods sold. | ((Revenue - COGS) / Revenue) x 100 | Finance |
| Period-End Close Time | Days taken to close an accounting period. | Close completion date - Period end date | Accounting |
| Bank Reconciliation Rate | Share of bank lines matched during reconciliation. | (Matched lines / Total statement lines) x 100 | Banking |
| Budget Variance | Deviation of actuals from approved budget. | ((Actual - Budget) / Budget) x 100 | Budgeting |
| Asset Utilization | Share of asset useful capacity actively in use. | (Assets in use / Total depreciable assets) x 100 | Assets |

## Section E - Human Capital

| Metric | Definition | Formula | Owning Module |
|---|---|---|---|
| Employee Turnover Rate | Share of employees leaving in a period. | (Separations / Average headcount) x 100 | HR |
| Payroll Accuracy | Share of payslips issued without correction. | (Accurate payslips / Total payslips) x 100 | Payroll |
| Attendance Rate | Share of scheduled working time actually attended. | (Attended hours / Scheduled hours) x 100 | Attendance |
| Time to Hire | Average days from requisition to accepted offer. | Sum(Offer accepted - Requisition raised) / Hires | Recruitment |

## Section F - Projects & Productivity

| Metric | Definition | Formula | Owning Module |
|---|---|---|---|
| Project On-Time Completion | Share of projects delivered by the baseline date. | (On-time projects / Completed projects) x 100 | Projects |
| Task Completion Rate | Share of tasks completed by their due date. | (On-time tasks / Total due tasks) x 100 | Task Management |
| Document Approval Cycle Time | Average time to approve a controlled document. | Sum(Approval - submission) / Number of documents | Documents |

## Section G - Platform Services

| Metric | Definition | Formula | Owning Module |
|---|---|---|---|
| Workflow Throughput Time | Average end-to-end duration of a workflow instance. | Sum(Completion - start) / Completed instances | Workflow |
| Approval Turnaround Time | Average time from approval request to decision. | Sum(Decision - request) / Approval requests | Approvals |
| Notification Delivery Rate | Share of notifications successfully delivered. | (Delivered notifications / Sent notifications) x 100 | Notifications |

## Section H - Intelligence & Insights

| Metric | Definition | Formula | Owning Module |
|---|---|---|---|
| Report Generation Success Rate | Share of scheduled reports produced without error. | (Successful runs / Scheduled runs) x 100 | Reporting |
| Dashboard Adoption Rate | Share of target users actively viewing dashboards. | (Active dashboard users / Target users) x 100 | Dashboards |
| AI Suggestion Acceptance Rate | Share of AI recommendations accepted by users. | (Accepted suggestions / Total suggestions) x 100 | AI Integration |

## Cross-References

- [Module Templates](/docs/blueprint/volume-06-business-modules/appendices/module-templates.md)
- [Business Module Glossary](/docs/blueprint/volume-06-business-modules/appendices/business-module-glossary.md)
- [Integration Map](/docs/blueprint/volume-06-business-modules/appendices/integration-map.md)

## References

- [Volume 01 - Vision and Philosophy](/docs/blueprint/volume-01-vision-and-philosophy/README.md)
- [Document Standards](/docs/governance/document-standards.md)

## Change Log

| Version | Date | Author | Summary |
|---|---|---|---|
| 1.0 | 2026-07-12 | Lead Software Engineer | Initial approved version. |
