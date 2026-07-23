# Volume 14 - Knowledge Glossary

| Field | Value |
|---|---|
| Document ID | WORLD-VOL14-A1 |
| Title | Knowledge Glossary |
| Version | 1.0 |
| Status | Approved |
| Classification | Internal |
| Founder | Mahesh Choudhary |

## Purpose

This appendix provides a single, authoritative glossary of the knowledge, retrieval, and semantic terms used throughout Volume 14. Its purpose is to remove ambiguity: when a chapter uses a term such as *embedding*, *chunking*, or *grounding*, this glossary fixes its meaning for Project WORLD. The Knowledge Engine draws vocabulary from information retrieval, knowledge representation, and language-model practice, and reasoning about it coherently requires that every author mean the same thing by the same word. A shared vocabulary is a precondition for a governable knowledge tier.

## Scope

The glossary defines the knowledge-source, retrieval, structure, and governance terms that appear in Volume 14, Sections A through F, together with a small number of adjacent terms needed to make those definitions self-contained. Definitions are concise and vendor-neutral. It does not redefine agent terms (governed by Volume 13), security terms (Volume 12), or database terms (Volume 09). Where a term has a broader meaning in general usage, the definition given here is the WORLD-canonical one for the knowledge context.

## Glossary

| Term | Definition |
|---|---|
| ANN (Approximate Nearest Neighbor) | An algorithm that finds near-closest vectors quickly by trading exactness for speed. |
| Chunk | A bounded segment of a source document sized for embedding and retrieval. |
| Chunking | The process of dividing a source into retrievable chunks. |
| Citation | An attributable reference from an answer back to the source unit that grounds it. |
| Context Engine | The component that assembles the relevant knowledge context for a query. |
| Context Window | The bounded span of tokens a model can consider in a single inference. |
| Corpus | The complete governed body of knowledge units in the Knowledge Engine. |
| Cosine Similarity | A measure of similarity between two vectors based on the angle between them. |
| DIKW | The Data-Information-Knowledge-Wisdom hierarchy describing how raw data becomes understanding. |
| Dense Retrieval | Retrieval based on learned vector embeddings rather than exact terms. |
| Drift | The gradual divergence of the corpus from current reality over time. |
| Embedding | A numeric vector representation of text or data used for similarity and retrieval. |
| Entity | A distinct real-world thing represented as a node in the knowledge graph or ontology. |
| Faithfulness | The degree to which an answer is grounded in its supporting evidence. |
| Grounding | Anchoring generated output in retrieved, authoritative sources. |
| Graph RAG | Retrieval-augmented generation that traverses a knowledge graph to gather connected context. |
| Hybrid Retrieval | Retrieval that combines dense (vector) and sparse (keyword) methods. |
| Hallucination | A fluent but unsupported or incorrect generated output. |
| Index | A structure that makes knowledge units efficiently searchable. |
| Ingestion | The pipeline that admits, normalizes, and indexes source units into the corpus. |
| Knowledge Graph | A network of entities and relationships representing structured knowledge. |
| Knowledge Registry | The authoritative catalog of what knowledge exists, its owner, and its classification. |
| Knowledge Source | An accountable origin of a class of enterprise knowledge. |
| Knowledge Unit | The smallest governed, versioned, retrievable element of knowledge. |
| Lexical Search | Search that matches literal terms rather than meaning. |
| Metadata | Structured descriptive fields attached to a knowledge unit. |
| Ontology | A formal specification of the concepts, entities, and relationships in a domain. |
| Provenance | The recorded origin, owner, and version history of a knowledge unit. |
| Query Expansion | Enriching a query with related terms or concepts to improve recall. |
| Query Rewriting | Reformulating a query to better match how knowledge is stored. |
| RAG (Retrieval-Augmented Generation) | Generating output conditioned on evidence retrieved from a knowledge source. |
| Recall | The fraction of relevant units a retrieval returns out of all relevant units. |
| Reranking | Reordering retrieved candidates with a stronger relevance model. |
| Relevance | The degree to which a retrieved unit answers the query. |
| Retrieval | The act of selecting the most relevant knowledge units for a query. |
| Semantic Search | Search based on meaning and vector similarity rather than literal terms. |
| Sparse Retrieval | Term-based retrieval such as keyword or BM25 matching. |
| Staleness | The condition of a unit being outdated relative to current truth. |
| Taxonomy | A hierarchical classification of knowledge into categories. |
| Token | The unit of text a model processes; the basis of context and cost accounting. |
| Trust Weight | A source-level score biasing retrieval toward more authoritative origins. |
| Vector | An array of numbers representing content in an embedding space. |
| Vector Store | A database that indexes embeddings for similarity search. |
| Versioning | The governed recording of successive states of a knowledge unit. |

## Cross-References

- [Knowledge Terminology](/docs/blueprint/volume-14-knowledge-engine/appendices/knowledge-terminology.md)
- [Retrieval Patterns](/docs/blueprint/volume-14-knowledge-engine/appendices/retrieval-patterns.md)
- [Embeddings](/docs/blueprint/volume-14-knowledge-engine/section-c-retrieval-and-context/14-embeddings.md)

## References

- [Volume 01 - Vision and Philosophy](/docs/blueprint/volume-01-vision-and-philosophy/README.md)
- [Document Standards](/docs/governance/document-standards.md)

## Change Log

| Version | Date | Author | Notes |
|---|---|---|---|
| 1.0 | 2026-07-12 | Lead Software Engineer | Initial approved version. |
