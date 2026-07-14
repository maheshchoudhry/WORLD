# Volume 07 - Compliance Catalog

| Field | Value |
|---|---|
| Document ID | WORLD-VOL07-A4 |
| Title | Compliance Catalog |
| Version | 1.0 |
| Status | Approved |
| Classification | Internal |
| Founder | Mahesh Choudhary |

## Purpose

This appendix catalogs the well-known compliance standards, regulations, and frameworks that commonly apply to the 18 industries of Volume 07. It gives industry solution owners and implementation teams a grounded reference to real, established obligations so that industry configurations account for the applicable regulatory context rather than treating compliance as an afterthought.

## Scope

Entries name recognized standards and regulations, summarize their intent, and identify the industries to which they most commonly apply. The catalog is representative, not exhaustive, and does not reproduce clause numbers, legal text, or jurisdiction-specific thresholds; the authoritative source is always the issuing body and the applicable local law. Determining which obligations bind a given deployment is performed during industry onboarding with qualified advisors.

## Cross-Industry Standards

| Standard / Framework | Focus | Typical Applicability |
|---|---|---|
| ISO 9001 | Quality management systems. | All industries with formal quality programs. |
| ISO 27001 | Information security management systems. | All industries handling sensitive data. |
| ISO 14001 | Environmental management systems. | Production, process, and asset-intensive industries. |
| ISO 45001 | Occupational health and safety management. | Manufacturing, construction, logistics, and process industries. |
| GDPR | Protection of personal data of individuals in the EU. | Any industry processing EU personal data. |
| SOC 2 | Controls for security, availability, and confidentiality of service data. | Services and technology-enabled operations. |
| PCI DSS | Security of payment card data. | Retail, hospitality, e-commerce, and any card-accepting business. |

## Section A - Production & Process Industries

| Industry | Standard / Regulation | Focus |
|---|---|---|
| Dairy | FSSAI regulations; Codex Alimentarius; HACCP | Food safety, hygiene, and dairy product standards. |
| Dairy | ISO 22000 | Food safety management systems across the chain. |
| Manufacturing | ISO 9001; ISO 14001; ISO 45001 | Quality, environmental, and safety management. |
| Manufacturing | CE marking; RoHS; REACH | Product conformity and restricted-substance compliance. |
| Food Processing | HACCP; FSSAI; FDA Food Safety Modernization Act (FSMA) | Preventive food safety and hazard control. |
| Food Processing | BRCGS; ISO 22000; GMP | Global food safety certification and manufacturing practice. |
| Pharmaceutical | GMP / GxP (Good Manufacturing, Laboratory, Distribution Practice) | End-to-end pharmaceutical quality assurance. |
| Pharmaceutical | US FDA 21 CFR Part 11; WHO GMP; EU GMP | Electronic records, signatures, and manufacturing standards. |
| Pharmaceutical | Drug serialization / track-and-trace (e.g., US DSCSA, EU FMD) | Unit-level traceability and anti-counterfeiting. |
| Agriculture | GlobalG.A.P.; organic certification schemes | Good agricultural practice and produce integrity. |
| Agriculture | FSSAI; pesticide and residue regulations | Input safety and produce compliance. |

## Section B - Trade & Distribution

| Industry | Standard / Regulation | Focus |
|---|---|---|
| Retail | PCI DSS | Payment card data security. |
| Retail | Consumer protection and labeling regulations; GST/VAT | Fair trade, product labeling, and indirect tax. |
| Wholesale | GST/VAT; e-invoicing mandates | Indirect tax and statutory invoicing. |
| Wholesale | Weights and measures regulations | Accurate quantity and measurement in trade. |
| Distribution | Good Distribution Practice (GDP) | Integrity of goods, notably pharmaceuticals, in transit and storage. |
| Distribution | Hazardous materials handling (e.g., ADR, IATA DGR) | Safe handling and transport of dangerous goods. |
| Automobile | ISO/TS 16949 (IATF 16949) | Automotive quality management for the supply chain. |
| Automobile | Vehicle safety and emissions regulations; warranty law | Type approval, emissions, and consumer warranty obligations. |

## Section C - Services & Public Sector

| Industry | Standard / Regulation | Focus |
|---|---|---|
| Healthcare | HIPAA | Privacy and security of protected health information (US). |
| Healthcare | HL7 / FHIR; ICD; SNOMED CT | Clinical data interoperability and coding standards. |
| Healthcare | NABH / Joint Commission accreditation | Hospital quality and patient safety accreditation. |
| Education | FERPA | Privacy of student education records (US). |
| Education | Accreditation and curriculum regulations | Institutional quality and program recognition. |
| Hospitality | PCI DSS; food safety (HACCP/FSSAI) | Payment security and food and beverage safety. |
| Hospitality | Fire, safety, and licensing regulations | Guest safety and operating licenses. |
| Professional Services | ISO 27001; SOC 2 | Information security and service controls. |
| Professional Services | Professional bodies and anti-money-laundering (AML/KYC) rules | Professional conduct and client due diligence. |

## Section D - Infrastructure & Assets

| Industry | Standard / Regulation | Focus |
|---|---|---|
| Construction | ISO 45001; local building codes | Site safety and structural compliance. |
| Construction | ISO 19650 (BIM); environmental permits | Information management for built assets and environmental control. |
| Real Estate | Property registration, zoning, and tenancy laws | Title, land use, and lease compliance. |
| Real Estate | Building safety and energy performance regulations | Occupant safety and energy standards. |
| Logistics | ISO 28000; C-TPAT / AEO programs | Supply chain security and trusted-trader status. |
| Logistics | Customs and trade compliance; Incoterms | Cross-border movement and trade terms. |
| Transportation | Vehicle safety, driver hours, and licensing regulations | Road safety and operator compliance. |
| Transportation | ADR / IATA / IMDG dangerous goods rules | Safe carriage of hazardous goods by mode. |

## Section E - Extensibility

| Area | Approach | Focus |
|---|---|---|
| Future Industry Framework | Compliance profile configuration | New industries inherit cross-industry standards and add vertical-specific obligations identified during instantiation. |

## Cross-References

- [Industry Glossary](/docs/blueprint/volume-07-industry-solutions/appendices/industry-glossary.md)
- [Industry KPI Catalog](/docs/blueprint/volume-07-industry-solutions/appendices/industry-kpi-catalog.md)
- [Dashboard & Reporting Templates](/docs/blueprint/volume-07-industry-solutions/appendices/dashboard-and-reporting-templates.md)
- [References](/docs/blueprint/volume-07-industry-solutions/appendices/references.md)

## References

- [Volume 01 - Vision and Philosophy](/docs/blueprint/volume-01-vision-and-philosophy/README.md)
- [Document Standards](/docs/governance/document-standards.md)

## Change Log

| Version | Date | Author | Summary |
|---|---|---|---|
| 1.0 | 2026-07-12 | Lead Software Engineer | Initial approved version. |
