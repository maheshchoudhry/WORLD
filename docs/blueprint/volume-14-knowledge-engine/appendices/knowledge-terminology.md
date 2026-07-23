# Volume 14 - Knowledge Terminology

| Field | Value |
|---|---|
| Document ID | WORLD-VOL14-A2 |
| Title | Knowledge Terminology |
| Version | 1.0 |
| Status | Approved |
| Classification | Internal |
| Founder | Mahesh Choudhary |

## Purpose

This appendix defines the controlled vocabulary for the knowledge tier of Project WORLD: the preferred terms every chapter, diagram, and catalog must use, and the terms to avoid because they are ambiguous, conflated, or misleading. Where the glossary (Appendix A1) fixes meanings, this appendix fixes usage. Consistent terminology matters because the Knowledge Engine grounds consequential AI decisions, and imprecise language about retrieval, sources, or structure erodes the clarity that governance and trust depend on.

## Scope

The document establishes the canonical term for each concept, lists common alternatives that must not be used in Volume 14, and states the reason. It also gives usage conventions for describing knowledge behaviour precisely. It governs terminology within Volume 14 only; adjacent vocabularies for agents, security, and the database are owned by Volumes 13, 12, and 09 respectively. It does not redefine the concepts themselves, which the glossary covers.

## Controlled Vocabulary

| Preferred Term | Use For | Do Not Use |
|---|---|---|
| Knowledge Unit | The atomic governed, retrievable element | record, chunk (for this sense), item |
| Knowledge Source | An accountable origin of knowledge | data feed, repository (bare), dump |
| Retrieval | Selecting relevant units for a query | search (for this sense), lookup, fetch |
| Semantic Search | Meaning-based vector search | smart search, AI search |
| Embedding | The vector representation of content | vectorization output, encoding (bare) |
| Grounding | Anchoring output in retrieved sources | referencing, backing |
| Provenance | Recorded origin, owner, and version | source tag, metadata (for this sense) |
| Corpus | The full governed body of units | dataset, knowledge base (bare) |
| Trust Weight | Source authority score biasing ranking | priority, rank (bare), score (bare) |
| Ontology | Formal concept-and-relationship model | schema (for this sense), taxonomy |
| Taxonomy | Hierarchical category classification | ontology, tagging (bare) |
| Citation | Attributable link from answer to unit | footnote, mention |

## Terms to Avoid

| Term to Avoid | Reason | Use Instead |
|---|---|---|
| The AI knows | Overstates model cognition as human knowing | the AI retrieves / is grounded in |
| Single source of truth (for a document) | Conflates a document with the governed unit and its provenance | authoritative source with recorded provenance |
| Search the AI | Conflates retrieval with the model | retrieve from the corpus |
| Ontology and taxonomy (interchangeably) | They are distinct structures | ontology for relationships, taxonomy for hierarchy |
| Vector database is the knowledge | Conflates an index with the governed corpus | vector store indexes the corpus |
| Always up to date | False assurance; freshness is governed, not guaranteed | maintained under the evolution loop |
| Perfect recall | No retrieval is exhaustive | tuned for recall at a measured level |
| Self-learning knowledge | Implies ungoverned change | improved under the governed evolution loop |

## Usage Conventions

Describe knowledge behaviour in terms of governed action and evidence: prefer "the answer is grounded in the retrieved policy" over "the AI knew the policy." Always distinguish the source (the accountable origin), the unit (the retrievable element), and the index (the searchable structure); never use one word for all three. Pair any claim of freshness or accuracy with the mechanism that maintains it - the evolution loop or the quality metric - rather than asserting it absolutely. Reserve *ontology* for relationship models and *taxonomy* for hierarchies, and never treat them as synonyms.

## Cross-References

- [Knowledge Glossary](/docs/blueprint/volume-14-knowledge-engine/appendices/knowledge-glossary.md)
- [Ontology Catalog](/docs/blueprint/volume-14-knowledge-engine/appendices/ontology-catalog.md)
- [Ontology](/docs/blueprint/volume-14-knowledge-engine/section-d-structure-and-semantics/17-ontology.md)

## References

- [Volume 01 - Vision and Philosophy](/docs/blueprint/volume-01-vision-and-philosophy/README.md)
- [Document Standards](/docs/governance/document-standards.md)

## Change Log

| Version | Date | Author | Notes |
|---|---|---|---|
| 1.0 | 2026-07-12 | Lead Software Engineer | Initial approved version. |
