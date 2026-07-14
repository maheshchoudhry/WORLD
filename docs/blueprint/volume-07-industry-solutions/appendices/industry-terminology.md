# Volume 07 - Industry Terminology

| Field | Value |
|---|---|
| Document ID | WORLD-VOL07-A2 |
| Title | Industry Terminology |
| Version | 1.0 |
| Status | Approved |
| Classification | Internal |
| Founder | Mahesh Choudhary |

## Purpose

This appendix defines the controlled vocabulary for WORLD's industry solutions: the canonical industry names, the approved terms for core industry-solution concepts, and the terms to avoid. It ensures that documentation, configurations, user interfaces, and conversations reference each industry and solution concept by a single, consistent name across all 18 industries and five sections.

## Scope

The controlled vocabulary governs industry naming, section naming, and shared solution-concept labels used in Volume 07. It complements the definitions in WORLD-VOL07-A1 (Industry Glossary) by specifying which term is canonical and which alternatives are deprecated. It aligns with the module terminology of Volume 06 (WORLD-VOL06-A2) and does not override statutory, regulatory, or clinical terms where those are legally or professionally required.

## Naming Principles

| Principle | Description |
|---|---|
| One canonical name | Each industry and solution concept has exactly one approved name; synonyms are documented and deprecated. |
| Business-first language | Names reflect the industry capability or business meaning, not a specific tool or vendor. |
| Vertical-neutral core | Industry names extend the industry-independent core; they never fork the underlying module vocabulary of Volume 06. |
| Stable across layers | The same canonical name is used in documentation, configuration, UI labels, and analytics. |
| Regulatory deference | Where a regulator or profession mandates a term, that term is used verbatim in the relevant context. |

## Canonical Industry Names

| Section | Canonical Industry Name | Approved Usage | Terms to Avoid |
|---|---|---|---|
| A | Dairy | Milk procurement, processing, and dairy product operations. | Milk business, Dairy farm module |
| A | Manufacturing | Discrete and process production of finished goods. | Factory solution, Mfg vertical |
| A | Food Processing | Conversion of agricultural inputs into food products. | Food industry, F&B processing |
| A | Pharmaceutical | Regulated production of medicinal products. | Pharma module, Drugs vertical |
| A | Agriculture | Crop and livestock primary production. | Agri module, Farming solution |
| B | Retail | Sale of goods to end consumers across channels. | Shop solution, Store vertical |
| B | Wholesale | Bulk sale of goods to resellers and businesses. | Bulk trade, Distributor sales |
| B | Distribution | Movement and supply of goods to downstream channels. | Distributor module, Supply vertical |
| B | Automobile | Vehicle sales, service, parts, and dealership operations. | Auto module, Car business |
| C | Healthcare | Delivery of clinical and health services. | Hospital module, Medical vertical |
| C | Education | Delivery and administration of learning. | School solution, Edu module |
| C | Hospitality | Lodging, food service, and guest experience. | Hotel module, Hosp vertical |
| C | Professional Services | Delivery of expertise-based client engagements. | Consulting module, Services firm app |
| D | Construction | Delivery of built assets through projects. | Contracting module, Build vertical |
| D | Real Estate | Development, leasing, and management of property. | Property module, Realty solution |
| D | Logistics | Storage and movement of goods as a service. | 3PL module, Freight vertical |
| D | Transportation | Movement of goods or people via fleets. | Transport module, Fleet solution |
| E | Future Industry Framework | Pattern-based extension of WORLD to new verticals. | New industry kit, Generic vertical |

## Section Names

| Section | Canonical Section Name | Terms to Avoid |
|---|---|---|
| A | Production & Process Industries | Makers, Producers group |
| B | Trade & Distribution | Commerce, Selling group |
| C | Services & Public Sector | Services group, Non-industrial |
| D | Infrastructure & Assets | Heavy industry, Asset group |
| E | Extensibility | Misc, Others |

## Solution-Concept Term Standards

| Concept | Canonical Term | Approved Usage | Terms to Avoid |
|---|---|---|---|
| Configuration of the core for a vertical | Industry Solution | A packaged configuration mapping an industry to modules, AI, KPIs, and compliance. | Industry app, Vertical build |
| Mapping of an industry to required modules | Module Mapping | The Core / Recommended / Optional assignment of Volume 06 modules to an industry. | Module list, Feature map |
| Industry-specific process variant | Process Configuration | A configured variant of a standard business process for a vertical. | Custom flow, Bespoke process |
| Regulatory obligation applicable to an industry | Compliance Requirement | A named standard or regulation the industry must satisfy. | Rule, Legal item |
| Representative measure for an industry | Industry KPI | A vertical-relevant performance indicator defined in WORLD-VOL07-A5. | Industry metric, Vertical stat |
| Pre-built industry dashboard or report | Solution Template | A reusable dashboard or report layout for an industry role. | Screen pack, Report bundle |
| Extension of WORLD to an unlisted vertical | Industry Instantiation | The act of configuring a new industry via the Future Industry Framework. | New build, Vertical spin-up |

## Cross-References

- [Industry Glossary](/docs/blueprint/volume-07-industry-solutions/appendices/industry-glossary.md)
- [Industry-ERP Module Matrix](/docs/blueprint/volume-07-industry-solutions/appendices/industry-erp-module-matrix.md)
- [Future Industry Framework](/docs/blueprint/volume-07-industry-solutions/section-e-extensibility/18-future-industry-framework.md)
- [Module Terminology (Volume 06)](/docs/blueprint/volume-06-business-modules/appendices/module-terminology.md)

## References

- [Volume 01 - Vision and Philosophy](/docs/blueprint/volume-01-vision-and-philosophy/README.md)
- [Document Standards](/docs/governance/document-standards.md)

## Change Log

| Version | Date | Author | Summary |
|---|---|---|---|
| 1.0 | 2026-07-12 | Lead Software Engineer | Initial approved version. |
