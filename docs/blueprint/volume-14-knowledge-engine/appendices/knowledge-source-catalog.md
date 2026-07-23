# Volume 14 - Knowledge Source Catalog

| Field | Value |
|---|---|
| Document ID | WORLD-VOL14-A5 |
| Title | Knowledge Source Catalog |
| Version | 1.0 |
| Status | Approved |
| Classification | Internal |
| Founder | Mahesh Choudhary |

## Purpose

This appendix catalogs the standard knowledge source types that feed the Knowledge Engine of Project WORLD. Where Chapter 05 defines the source contract and Chapters 06 to 10 detail the first-class source types, this appendix provides the at-a-glance reference: for each source type, its native format, accountable owner, refresh cadence, and sensitivity. Its purpose is operational clarity - anyone onboarding, governing, or auditing a source can see in one table what each source is, who owns it, how fresh it stays, and how sensitive it is.

## Scope

The document tabulates the recognized knowledge source types with their format, ownership, refresh cadence, and default sensitivity. It covers the cross-enterprise source catalog; industry- and tenant-specific sources register under these types. It does not specify connector implementation, ingestion internals, or retrieval mechanics, which are covered in Sections B and C. The catalog is a reference and a governance aid, not a connector specification.

## Source Catalog

| Source | Format | Owner | Refresh | Sensitivity |
|---|---|---|---|---|
| Document Library | PDF, DOCX, HTML, Markdown | Knowledge Steward | On change (event-driven) | Internal |
| Policy Set | Governed prose | Compliance Owner | On approval cycle | Internal |
| SOP Catalogue | Structured procedure | Process Owner | On approval cycle | Internal |
| Business Rules | Executable logic (rule engine) | Rules Owner | On rule change | Confidential |
| Research Repository | Reports, studies, citations | Research Lead | Periodic (batch) | Confidential |
| Product Data | Structured records (ERP) | Product Owner | Near-real-time | Internal |
| Customer Records | Structured records (ERP/CRM) | Data Owner | Near-real-time | Restricted |
| Financial Records | Structured records (ERP) | Finance Owner | Near-real-time | Restricted |
| Meeting & Decision Notes | Text, transcripts | Team Lead | On capture | Confidential |
| External Reference Data | Feeds, standards, regulations | Data Owner | Scheduled (periodic) | Public |

## Catalog Notes

Refresh cadence and sensitivity together drive how a source is governed. Near-real-time sources such as customer and financial records demand incremental change detection and the tightest access scopes, while approval-cycle sources such as policies and SOPs change deliberately and carry review provenance. Sensitivity sets the default `classification` and `access_scope` metadata (Appendix A4) applied at ingestion; restricted sources are never returned outside their scope regardless of query. Every source in this catalog registers with a named owner in the Knowledge Registry before any unit is admitted.

## Cross-References

- [Knowledge Sources](/docs/blueprint/volume-14-knowledge-engine/section-b-knowledge-sources/05-knowledge-sources.md)
- [Metadata Standards](/docs/blueprint/volume-14-knowledge-engine/appendices/metadata-standards.md)
- [Knowledge Registry](/docs/blueprint/volume-14-knowledge-engine/section-a-knowledge-foundations/04-knowledge-registry.md)

## References

- [Volume 01 - Vision and Philosophy](/docs/blueprint/volume-01-vision-and-philosophy/README.md)
- [Document Standards](/docs/governance/document-standards.md)

## Change Log

| Version | Date | Author | Notes |
|---|---|---|---|
| 1.0 | 2026-07-12 | Lead Software Engineer | Initial approved version. |
