# Volume 07 - Distribution

| Field | Value |
|---|---|
| Document ID | WORLD-VOL07-008 |
| Title | Distribution |
| Version | 1.0 |
| Status | Approved |
| Classification | Internal |
| Founder | Mahesh Choudhary |

## Purpose

Define how WORLD is configured and applied for the distribution industry. This chapter maps the distribution business model, organization, and route-to-market processes to the required ERP modules (Volume 06) and AI features (Volume 03), and specifies the KPIs, compliance, dashboards, reporting, and roadmap that make WORLD an operational AI Business Partner for distributors.

## Scope

Covers appointed and independent distribution of manufacturer products to a network of retailers and outlets, spanning territory and beat planning, secondary sales, van and field-force operations, scheme and claim management, and multi-echelon inventory. Applies to fast-moving consumer goods distributors, pharmaceutical and consumer-durable distributors, and stockists. Excludes cash-and-carry wholesale (WORLD-VOL07-007) and end-consumer retail (WORLD-VOL07-006).

## Industry Overview

Distribution operates the route-to-market layer that carries a principal's products from factory or depot to the point of sale. It is defined by dense outlet networks, fixed delivery beats, secondary-sales targets, promotional schemes, and tight settlement of claims with principals. Distributors compete on coverage, service frequency, and execution quality. WORLD models the distributor as a coverage-and-settlement engine in which every outlet, van, scheme, and claim is tracked against target in real time.

## Business Model

Distributors earn a margin or commission on the products they move, supplemented by principal schemes and settled through claims. Revenue depends on outlet coverage, order frequency, and productive calls, while profitability depends on delivery cost per drop, damage and expiry, and the speed and accuracy of claim recovery. WORLD models each territory as a coverage unit, each principal as a settlement relationship, and each van route as a cost-and-service line, giving the operator live control over reach and recovery.

## Organization

A distribution organization spans principal and category management, field sales supervision, the van and delivery fleet, warehouse operations, and claims and finance. WORLD maps these to scoped roles: the Distributor Principal owns the business and principal relationships, the Sales Supervisor manages beats and field targets, the Field Salesperson books secondary orders at the outlet, the Delivery Driver executes the drop, and the Claims Officer reconciles schemes with principals.

## Processes

The core distribution cycle runs from primary purchase from the principal through beat planning, secondary order capture, van delivery, and scheme claim settlement.

```mermaid
flowchart LR
  A[Primary Order to Principal] --> B[Receive to Depot]
  B --> C[Plan Beats and Routes]
  C --> D[Field Order Capture]
  D --> E[Load Van]
  E --> F[Deliver to Outlet]
  F --> G[Collect Payment]
  G --> H[Reconcile Secondary Sales]
  H --> I[File Scheme Claim]
  I --> J[Settle with Principal]
```

## Required ERP Modules

Distribution is assembled primarily from the Supply Chain and Sales sections of Volume 06.

| Capability | Module | Reference |
|---|---|---|
| Secondary order capture | Sales | [Sales](/docs/blueprint/volume-06-business-modules/section-b-sales-and-customer/07-sales.md) |
| Outlet and beat relationship | CRM | [CRM](/docs/blueprint/volume-06-business-modules/section-b-sales-and-customer/06-crm.md) |
| Multi-echelon stock | Inventory | [Inventory](/docs/blueprint/volume-06-business-modules/section-a-supply-chain-and-procurement/02-inventory.md) |
| Route and van delivery | Dispatch | [Dispatch](/docs/blueprint/volume-06-business-modules/section-a-supply-chain-and-procurement/05-dispatch.md) |
| Movement between depots | Logistics | [Logistics](/docs/blueprint/volume-06-business-modules/section-a-supply-chain-and-procurement/04-logistics.md) |

Sales, CRM, and Dispatch share one outlet identity, so a booked secondary order, its delivery drop, and the outlet's payment history are reconciled together against the beat plan.

## Required AI Features

The AI Business Partner (Volume 03) optimizes beat plans and van routes, forecasts outlet-level demand, recommends scheme allocation for maximum secondary sales, and predicts near-expiry risk across depots. It also validates claims against captured secondary-sales evidence to accelerate settlement. Example: the AI Business Partner detects that a high-value beat is losing productive calls because two outlets are consistently closed at the scheduled visit time, re-sequences the route to visit them in the early evening, reassigns the freed morning slot to three under-served outlets, and forecasts a recovery of secondary sales within the territory over the next cycle.

## KPIs

| KPI | Definition |
|---|---|
| Outlet coverage | Outlets billed as a share of the total universe |
| Productive call rate | Calls resulting in an order divided by total calls |
| Lines per bill | Average distinct SKUs per outlet order |
| Delivery cost per drop | Total delivery cost divided by drops completed |
| Claim settlement days | Average days to recover scheme claims |
| Expiry and damage ratio | Value of expired or damaged stock as a share of sales |

## Compliance

Distribution operations must satisfy commercial tax and e-way documentation for goods movement, product traceability and batch or expiry tracking for regulated categories, principal contract and scheme terms, and financial settlement rules. WORLD enforces batch and expiry policy through Inventory, records goods movement and settlement on the ERP Foundation (Volume 05), and applies segregation between order booking, delivery, and claim approval.

## Dashboards

A Territory dashboard shows coverage, productive calls, and secondary sales against target. A Fleet dashboard shows route adherence, drops completed, and cost per drop. A Claims dashboard shows filed, approved, and pending claims with aging and AI-flagged discrepancies.

## Reporting

Standard reports include beat productivity, outlet-wise secondary sales, scheme and claim reconciliation, near-expiry exposure, and depot stock cover. Reports are produced through the Reporting module on demand or on schedule for supervisors, principals, and finance.

## Future Roadmap

Planned evolution includes fully automated beat optimization, real-time van tracking with proof-of-delivery, AI-validated straight-through claim settlement, predictive expiry redistribution across depots, and outlet self-ordering integrated directly into the beat plan.

## Cross-References

- [Dispatch](/docs/blueprint/volume-06-business-modules/section-a-supply-chain-and-procurement/05-dispatch.md)
- [Logistics](/docs/blueprint/volume-06-business-modules/section-a-supply-chain-and-procurement/04-logistics.md)
- [Sales](/docs/blueprint/volume-06-business-modules/section-b-sales-and-customer/07-sales.md)
- [Volume 05 - ERP Foundation](/docs/blueprint/volume-05-erp-foundation/README.md)

## References

- [Volume 01 - Vision and Philosophy](/docs/blueprint/volume-01-vision-and-philosophy/README.md)
- [Document Standards](/docs/governance/document-standards.md)

## Change Log

| Version | Date | Author | Notes |
|---|---|---|---|
| 1.0 | 2026-07-12 | Lead Software Engineer | Initial approved version. |
