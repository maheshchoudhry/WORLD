# Volume 05 - Enterprise Data Standards

| Field | Value |
|---|---|
| Document ID | WORLD-VOL05-A4 |
| Title | Enterprise Data Standards |
| Version | 1.0 |
| Status | Approved |
| Classification | Internal |
| Founder | Mahesh Choudhary |

## Purpose

This appendix defines the enterprise data standards that govern how master data, coding schemes, classification, ownership, and data quality are managed across WORLD's ERP framework. Reliable operations and trustworthy AI-driven decisions depend on clean, well-governed data. These standards make data a managed asset with clear rules and accountable owners.

## Scope

These standards apply to all persistent business data in WORLD's ERP layer, with emphasis on master data and reference data. They define numbering and coding conventions, classification tiers, stewardship roles, and quality dimensions. They complement the design standards (WORLD-VOL05-A3) and the terminology controls (WORLD-VOL05-A2). Transactional retention and statutory archival policies are governed separately and are out of scope here.

## 1. Master Data Standards

| ID | Standard |
|---|---|
| MDS-01 | Each master data domain (Customer, Vendor, Material, Account) has a single system of record. |
| MDS-02 | Master records are created through a governed onboarding process with mandatory-field validation. |
| MDS-03 | Duplicate prevention is enforced at creation via matching on defined key attributes. |
| MDS-04 | Master records are versioned; changes are auditable with who, what, and when. |
| MDS-05 | Master records are deactivated (soft state), never physically deleted, once referenced by transactions. |
| MDS-06 | Reference data (code lists) is centrally maintained and shared, not duplicated per module. |

## 2. Coding And Numbering Schemes

| Object | Scheme | Format | Example | Assignment |
|---|---|---|---|---|
| Tenant | Prefix + sequence | TNT-###### | TNT-000042 | System |
| Customer | Prefix + sequence | CUST-######## | CUST-00010293 | System |
| Vendor | Prefix + sequence | VEND-######## | VEND-00004821 | System |
| Material | Prefix + sequence | MAT-######## | MAT-00567120 | System |
| GL Account | Structured numeric | NNNNNN | 400100 | Governed |
| Cost Center | Prefix + numeric | CC-###### | CC-100200 | Governed |
| Profit Center | Prefix + numeric | PC-###### | PC-200100 | Governed |
| Sales Order | Type + year + sequence | SO-YYYY-######## | SO-2026-00012045 | System |
| Purchase Order | Type + year + sequence | PO-YYYY-######## | PO-2026-00008830 | System |

### Numbering Rules

| ID | Rule |
|---|---|
| NUM-01 | Business numbers are unique within their type and tenant. |
| NUM-02 | Number ranges are configurable per tenant but never overlap across types. |
| NUM-03 | Meaningful segments (year, type) are prefixes only; core identity remains a non-semantic sequence. |
| NUM-04 | Once assigned, a business number is immutable for the life of the record. |

## 3. Data Classification

| Tier | Label | Description | Handling |
|---|---|---|---|
| 1 | Public | Non-sensitive, shareable externally | No restriction |
| 2 | Internal | Default business data | Access limited to authorized tenant users |
| 3 | Confidential | Commercially sensitive (pricing, contracts) | Need-to-know, encrypted at rest and in transit |
| 4 | Restricted | Regulated or personal data (PII, financial identifiers) | Strict least-privilege, audited access, retention controls |

Every data element is assigned a classification tier; the highest tier present in a record governs its handling.

## 4. Data Ownership And Stewardship

| Role | Responsibility |
|---|---|
| Data Owner | Accountable for a data domain; approves definitions, classification, and access policy. |
| Data Steward | Maintains data quality day to day; resolves issues and enforces standards. |
| Data Custodian | Operates the systems storing the data; ensures security, backup, and availability. |
| Data Consumer | Uses data within granted permissions; reports quality issues. |

| ID | Standard |
|---|---|
| OWN-01 | Every master data domain has exactly one accountable Data Owner. |
| OWN-02 | Every domain has at least one assigned Data Steward. |
| OWN-03 | Access to Confidential and Restricted data requires Data Owner approval. |

## 5. Data Quality Dimensions

| Dimension | Definition | Example Measure |
|---|---|---|
| Accuracy | Data correctly reflects the real-world value. | % records passing validation against source of truth |
| Completeness | All required attributes are present. | % records with no missing mandatory fields |
| Consistency | Data agrees across systems and records. | % cross-system matches |
| Uniqueness | No unintended duplicate records exist. | Duplicate rate per domain |
| Timeliness | Data is current and available when needed. | Average age of critical fields |
| Validity | Data conforms to defined formats and rules. | % records passing format and range checks |
| Integrity | Relationships and references are intact. | % records with valid foreign references |

### Quality Governance Rules

| ID | Rule |
|---|---|
| DQ-01 | Each critical data domain defines target thresholds for its quality dimensions. |
| DQ-02 | Quality is measured continuously; breaches raise issues to the Data Steward. |
| DQ-03 | Validation runs at data entry and periodically thereafter. |
| DQ-04 | Quality metrics are reported to Data Owners on a defined cadence. |

## Cross-References

- [ERP Design Standards](/docs/blueprint/volume-05-erp-foundation/appendices/erp-design-standards.md)
- [ERP Terminology](/docs/blueprint/volume-05-erp-foundation/appendices/erp-terminology.md)
- [Integration Templates](/docs/blueprint/volume-05-erp-foundation/appendices/integration-templates.md)

## References

- [Volume 01 - Vision and Philosophy](/docs/blueprint/volume-01-vision-and-philosophy/README.md)
- [Document Standards](/docs/governance/document-standards.md)

## Change Log

| Version | Date | Author | Summary |
|---|---|---|---|
| 1.0 | 2026-07-12 | Lead Software Engineer | Initial approved version. |
