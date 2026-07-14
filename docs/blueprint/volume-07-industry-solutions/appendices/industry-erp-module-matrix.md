# Volume 07 - Industry-ERP Module Matrix

| Field | Value |
|---|---|
| Document ID | WORLD-VOL07-A3 |
| Title | Industry-ERP Module Matrix |
| Version | 1.0 |
| Status | Approved |
| Classification | Internal |
| Founder | Mahesh Choudhary |

## Purpose

This appendix maps the 18 industries of Volume 07 to the business modules of Volume 06, indicating for each pairing whether a module is Core, Recommended, or Optional to the industry solution. It gives implementation teams a fast, authoritative starting point for scoping an industry deployment and ensures module selection is consistent with the canonical module catalog.

## Scope

The matrix covers the differentiating operational modules that vary meaningfully by industry. A set of universal-core modules applies to every industry and is listed separately rather than repeated per row. Assignments express the default posture of the industry solution; a specific customer deployment may adjust them within the Core / Recommended / Optional framework.

## Legend

| Mark | Meaning |
|---|---|
| C | Core - essential to the industry solution; enabled by default. |
| R | Recommended - commonly enabled to realize full value. |
| O | Optional - enabled where the business model requires it. |
| Cfg | Configured per instantiation via the Future Industry Framework. |

## Universal-Core Modules

The following Volume 06 modules are Core for every industry and are therefore not repeated in the matrix below: Finance, Accounting, Banking, Budgeting, HR, Payroll, Attendance, Workflow, Approvals, Notifications, Reporting, Dashboards, and AI Integration. Documents and Task Management are Recommended for every industry.

## Column Key

| Abbreviation | Volume 06 Module |
|---|---|
| Proc | Procurement |
| Inv | Inventory |
| Whse | Warehouse |
| Log | Logistics |
| Disp | Dispatch |
| Sales | Sales |
| CRM | CRM |
| POS | POS |
| ECom | E-Commerce |
| Prod | Production |
| PPln | Production Planning |
| Qual | Quality |
| Maint | Maintenance |
| Asset | Assets |
| Proj | Projects |

## Industry-Module Matrix

| Industry | Proc | Inv | Whse | Log | Disp | Sales | CRM | POS | ECom | Prod | PPln | Qual | Maint | Asset | Proj |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| Dairy | C | C | C | C | C | C | R | O | O | C | C | C | C | R | O |
| Manufacturing | C | C | C | R | C | C | R | O | O | C | C | C | C | C | R |
| Food Processing | C | C | C | C | C | C | R | O | O | C | C | C | C | R | O |
| Pharmaceutical | C | C | C | C | C | C | R | O | O | C | C | C | C | R | R |
| Agriculture | C | C | C | R | R | C | O | O | R | R | R | R | R | R | O |
| Retail | C | C | R | R | R | C | C | C | R | O | O | O | O | R | O |
| Wholesale | C | C | C | C | C | C | C | O | R | O | O | O | O | R | O |
| Distribution | C | C | C | C | C | C | R | O | R | O | O | O | O | R | O |
| Automobile | C | C | C | R | R | C | C | R | R | R | R | R | C | R | R |
| Healthcare | C | C | R | R | R | R | C | R | O | O | O | R | R | C | R |
| Education | R | R | O | O | O | R | C | R | R | O | O | O | R | C | C |
| Hospitality | C | C | R | O | R | C | C | C | R | R | O | R | R | C | O |
| Professional Services | R | O | O | O | O | C | C | O | O | O | O | O | O | R | C |
| Construction | C | C | R | R | R | R | R | O | O | R | R | R | R | C | C |
| Real Estate | R | O | O | O | O | C | C | O | R | O | O | O | R | C | R |
| Logistics | R | C | C | C | C | C | R | O | R | O | R | O | R | C | O |
| Transportation | R | R | R | C | C | C | R | R | R | O | R | O | C | C | O |
| Future Industry Framework | Cfg | Cfg | Cfg | Cfg | Cfg | Cfg | Cfg | Cfg | Cfg | Cfg | Cfg | Cfg | Cfg | Cfg | Cfg |

## Notes

- The Future Industry Framework row is configured per instantiation; module posture is derived from the target industry's business model during onboarding, using the same Core / Recommended / Optional framework.
- Where an industry marks Production or Manufacturing as Core, the corresponding Quality and Production Planning modules are typically enabled together to preserve process integrity.
- Assets is Core for asset-intensive industries (Healthcare, Education, Hospitality, Construction, Real Estate, Logistics, Transportation, and the process industries) and Recommended elsewhere.

## Cross-References

- [Industry Terminology](/docs/blueprint/volume-07-industry-solutions/appendices/industry-terminology.md)
- [Industry KPI Catalog](/docs/blueprint/volume-07-industry-solutions/appendices/industry-kpi-catalog.md)
- [Volume 06 - Business Modules Overview](/docs/blueprint/volume-06-business-modules/README.md)
- [Integration Map (Volume 06)](/docs/blueprint/volume-06-business-modules/appendices/integration-map.md)

## References

- [Volume 01 - Vision and Philosophy](/docs/blueprint/volume-01-vision-and-philosophy/README.md)
- [Document Standards](/docs/governance/document-standards.md)

## Change Log

| Version | Date | Author | Summary |
|---|---|---|---|
| 1.0 | 2026-07-12 | Lead Software Engineer | Initial approved version. |
