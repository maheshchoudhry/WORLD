# Volume 06 - Roles & Permissions Matrix

| Field | Value |
|---|---|
| Document ID | WORLD-VOL06-A7 |
| Title | Roles & Permissions Matrix |
| Version | 1.0 |
| Status | Approved |
| Classification | Internal |
| Founder | Mahesh Choudhary |

## Purpose

This appendix provides a representative role-based access control (RBAC) matrix across WORLD's business modules. It maps common business roles to the modules they use and the level of access each role holds, giving a consistent baseline for permission design. The matrix aligns with the ERP-foundation permissions model and the Approvals module, and it supports segregation of duties across the 32 modules.

## Scope

The matrix covers representative roles mapped against the eight domain sections at an access-level granularity. It defines a baseline that tenants refine through the governed permissions model; it is not a complete enumeration of every fine-grained permission. Field-level and record-level controls, delegation of authority, and approval thresholds are governed by the Approvals module (WORLD-VOL06-028) and the ERP Foundation (Volume 05).

## Access Levels

| Level | Symbol | Meaning |
|---|---|---|
| None | - | No access to the module. |
| Read | R | View records and reports only. |
| Write | W | Create and edit records (includes Read). |
| Approve | A | Authorize transactions at defined thresholds. |
| Admin | X | Full configuration and administration of the module. |

## Role Definitions

| Role | Description |
|---|---|
| System Administrator | Configures the platform and administers all modules. |
| Procurement Manager | Owns sourcing, purchasing, and vendor relationships. |
| Warehouse Operator | Executes receiving, storage, and pick-pack tasks. |
| Sales Representative | Manages leads, opportunities, and sales orders. |
| Production Supervisor | Runs shop-floor production and confirms output. |
| Quality Inspector | Performs inspections and dispositions non-conformances. |
| Finance Controller | Oversees ledgers, close, budgets, and financial control. |
| Accounts Payable Clerk | Processes vendor invoices and payments. |
| HR Administrator | Maintains employee data and organizational structure. |
| Payroll Officer | Runs payroll and manages compensation processing. |
| Project Manager | Plans and delivers projects and tasks. |
| Business Analyst | Builds reports and dashboards and consumes insights. |

## Matrix - Sections A to D

Columns use the domain-section abbreviations: SC = Supply Chain, SL = Sales & Customer, MF = Manufacturing, FIN = Finance.

| Role | SC | SL | MF | FIN |
|---|---|---|---|---|
| System Administrator | X | X | X | X |
| Procurement Manager | A | R | R | R |
| Warehouse Operator | W | R | R | - |
| Sales Representative | R | A | - | R |
| Production Supervisor | R | R | A | - |
| Quality Inspector | R | - | W | - |
| Finance Controller | R | R | R | A |
| Accounts Payable Clerk | R | - | - | W |
| HR Administrator | - | - | - | R |
| Payroll Officer | - | - | - | W |
| Project Manager | R | R | R | R |
| Business Analyst | R | R | R | R |

## Matrix - Sections E to H

Columns use the domain-section abbreviations: HC = Human Capital, PP = Projects & Productivity, PS = Platform Services, II = Intelligence & Insights.

| Role | HC | PP | PS | II |
|---|---|---|---|---|
| System Administrator | X | X | X | X |
| Procurement Manager | - | W | W | R |
| Warehouse Operator | - | R | R | R |
| Sales Representative | - | W | W | R |
| Production Supervisor | - | W | W | R |
| Quality Inspector | - | R | W | R |
| Finance Controller | R | R | A | R |
| Accounts Payable Clerk | - | R | W | R |
| HR Administrator | A | W | W | R |
| Payroll Officer | W | R | W | R |
| Project Manager | R | A | W | R |
| Business Analyst | R | R | R | A |

## Segregation-of-Duties Highlights

| Control | Description |
|---|---|
| Purchase versus payment | The Procurement Manager approves purchases; the Accounts Payable Clerk processes payments, keeping the two duties separate. |
| Production versus quality | The Production Supervisor confirms output; the Quality Inspector disposes of it, preventing self-approval. |
| Payroll versus finance | The Payroll Officer prepares pay; the Finance Controller approves the resulting postings. |
| Configuration versus operation | Only the System Administrator holds Admin rights, separating configuration from day-to-day operation. |

## Cross-References

- [Workflow Templates](/docs/blueprint/volume-06-business-modules/appendices/workflow-templates.md)
- [Integration Map](/docs/blueprint/volume-06-business-modules/appendices/integration-map.md)
- [Module Terminology](/docs/blueprint/volume-06-business-modules/appendices/module-terminology.md)

## References

- [Volume 01 - Vision and Philosophy](/docs/blueprint/volume-01-vision-and-philosophy/README.md)
- [Document Standards](/docs/governance/document-standards.md)

## Change Log

| Version | Date | Author | Summary |
|---|---|---|---|
| 1.0 | 2026-07-12 | Lead Software Engineer | Initial approved version. |
