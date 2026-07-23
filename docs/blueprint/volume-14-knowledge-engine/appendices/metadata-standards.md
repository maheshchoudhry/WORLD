# Volume 14 - Metadata Standards

| Field | Value |
|---|---|
| Document ID | WORLD-VOL14-A4 |
| Title | Metadata Standards |
| Version | 1.0 |
| Status | Approved |
| Classification | Internal |
| Founder | Mahesh Choudhary |

## Purpose

This appendix specifies the standard metadata schema attached to every knowledge unit in Project WORLD. Metadata is what makes a unit governable, retrievable, and attributable: without it, a chunk of text is anonymous and untrustworthy. This schema fixes the fields every unit must or may carry so that provenance, access control, freshness, and relevance can be enforced uniformly across all sources. Where the Metadata Standards chapter (Chapter 19) defines the discipline, this appendix provides the concrete field-level reference.

## Scope

The document defines the metadata field set - name, type, whether required, and description - that the ingestion pipeline applies to each unit and that retrieval and governance consume. It covers the cross-cutting metadata common to all knowledge units; source-specific extensions inherit from and add to this core. It does not define the storage format or the indexing internals; it defines the contract those layers must honor. The schema is normative: a unit missing a required field is not admitted to the corpus.

## Metadata Schema

| Field | Type | Required | Description |
|---|---|---|---|
| unit_id | String (UUID) | Yes | Globally unique identifier for the knowledge unit. |
| source_id | String | Yes | Identifier of the registered knowledge source of origin. |
| title | String | Yes | Human-readable title of the unit. |
| content_type | Enum | Yes | The kind of unit: document, policy, SOP, rule, research. |
| classification | Enum | Yes | Sensitivity level: public, internal, confidential, restricted. |
| owner | String | Yes | Accountable steward or role for the unit. |
| version | String (SemVer) | Yes | Version identifier of the unit. |
| created_at | Timestamp (ISO 8601) | Yes | Time the unit was first ingested. |
| updated_at | Timestamp (ISO 8601) | Yes | Time the unit was last modified. |
| effective_date | Date | No | Date from which the unit's content is authoritative. |
| expiry_date | Date | No | Date after which the unit is considered stale. |
| language | String (ISO 639-1) | No | Primary language of the content. |
| tags | Array of String | No | Taxonomy tags for classification and filtering. |
| trust_weight | Number (0-1) | Yes | Source-derived authority score biasing retrieval. |
| access_scope | Array of String | Yes | Roles or groups permitted to retrieve the unit. |
| provenance_uri | String (URI) | Yes | Reference back to the originating artifact. |
| checksum | String | No | Content hash for change detection and integrity. |
| embedding_model | String | No | Identifier of the model used to embed the unit. |

## Field Notes

Required fields form the governance minimum: identity, source, classification, ownership, version, timestamps, trust weight, access scope, and provenance must all be present. Optional fields improve freshness handling and retrieval quality but are not gating. The `classification` and `access_scope` fields are jointly enforced at retrieval so that no unit is returned to a principal outside its scope, and `expiry_date` feeds the staleness detection of the evolution loop.

## Cross-References

- [Metadata Standards](/docs/blueprint/volume-14-knowledge-engine/section-d-structure-and-semantics/19-metadata-standards.md)
- [Knowledge Source Catalog](/docs/blueprint/volume-14-knowledge-engine/appendices/knowledge-source-catalog.md)
- [Knowledge Registry](/docs/blueprint/volume-14-knowledge-engine/section-a-knowledge-foundations/04-knowledge-registry.md)

## References

- [Volume 01 - Vision and Philosophy](/docs/blueprint/volume-01-vision-and-philosophy/README.md)
- [Document Standards](/docs/governance/document-standards.md)

## Change Log

| Version | Date | Author | Notes |
|---|---|---|---|
| 1.0 | 2026-07-12 | Lead Software Engineer | Initial approved version. |
