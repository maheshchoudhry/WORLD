# Volume 10 - References

| Field | Value |
|---|---|
| Document ID | WORLD-VOL10-A7 |
| Title | References |
| Version | 1.0 |
| Status | Approved |
| Classification | Internal |
| Founder | Mahesh Choudhary |

## Purpose

This appendix collects the established, real-world API works and standards on which Volume 10 draws. Its purpose is intellectual honesty and traceability: WORLD's API tier is not invented in a vacuum but stands on a body of well-known specifications, standards, and reference works. Naming those sources lets a reader verify the reasoning, go deeper, and understand which ideas WORLD has adopted, adapted, or deliberately departed from.

## Scope

The document lists foundational references grouped by topic, covering REST and web architecture, HTTP, API description formats, response conventions, authentication and authorization, query and RPC APIs, asynchronous and event-driven APIs, and API security. Each entry names the work and its author or issuing body; formal citation details can be resolved from these names through their official publishers or standards bodies. To preserve accuracy, this appendix does not fabricate URLs or invent bibliographic identifiers. It is a curated starting point, not an exhaustive bibliography.

## REST and Web Architecture

| Reference | Author / Origin | Relevance to WORLD |
|---|---|---|
| Architectural Styles and the Design of Network-based Software Architectures | Roy T. Fielding | The doctoral dissertation defining REST, foundation of Section A. |
| RESTful Web Services | Leonard Richardson and Sam Ruby | Practical resource-oriented design behind the REST conventions. |
| Web API Design: The Missing Link | Google Cloud (API design guide) | Reference for pragmatic resource and method conventions. |
| API Design Patterns | JJ Geewax | Reference for standard method and resource patterns. |

## HTTP and Core Standards

| Reference | Author / Origin | Relevance to WORLD |
|---|---|---|
| RFC 9110 - HTTP Semantics | IETF | Authoritative source for methods, status codes, and headers. |
| RFC 9111 - HTTP Caching | IETF | Basis for caching, ETags, and conditional requests. |
| RFC 7807 / RFC 9457 - Problem Details for HTTP APIs | IETF | Influence on the WORLD error envelope in Appendix A5. |
| RFC 3339 - Date and Time on the Internet | IETF | Timestamp format used in payloads and event contracts. |

## API Description and Conventions

| Reference | Author / Origin | Relevance to WORLD |
|---|---|---|
| OpenAPI Specification | OpenAPI Initiative (Linux Foundation) | The contract format used in Appendix A4 and Chapter 15. |
| JSON:API Specification | JSON:API community | Reference for conventional JSON document structure. |
| JSON Schema | JSON Schema organization | Basis for payload validation within OpenAPI components. |

## Authentication and Authorization

| Reference | Author / Origin | Relevance to WORLD |
|---|---|---|
| RFC 6749 - The OAuth 2.0 Authorization Framework | IETF | Foundation of token-based authorization in Chapter 08. |
| OpenID Connect Core | OpenID Foundation | Identity layer over OAuth 2.0 for authenticated users. |
| RFC 7519 - JSON Web Token (JWT) | IETF | Token format underpinning bearer authentication. |
| OAuth 2.0 Security Best Current Practice | IETF OAuth Working Group | Guidance for hardening the authorization flows. |

## Query and RPC APIs

| Reference | Author / Origin | Relevance to WORLD |
|---|---|---|
| GraphQL Specification | GraphQL Foundation | Foundation of the GraphQL strategy in Chapter 03. |
| gRPC | Cloud Native Computing Foundation | Reference for typed service-to-service RPC in Section E. |
| Protocol Buffers | Google | Interface definition and serialization for gRPC contracts. |

## Asynchronous and Event-Driven APIs

| Reference | Author / Origin | Relevance to WORLD |
|---|---|---|
| AsyncAPI Specification | AsyncAPI Initiative (Linux Foundation) | Description format for event and message-driven APIs. |
| CloudEvents | Cloud Native Computing Foundation | Reference for the event envelope structure in Section E. |
| Enterprise Integration Patterns | Gregor Hohpe and Bobby Woolf | Foundational messaging patterns behind the event bus. |

## API Security

| Reference | Author / Origin | Relevance to WORLD |
|---|---|---|
| OWASP API Security Top 10 | OWASP Foundation | Threat framework driving the controls in Chapter 20. |
| OWASP Application Security Verification Standard | OWASP Foundation | Reference for verification requirements in API security. |
| RFC 6750 - OAuth 2.0 Bearer Token Usage | IETF | Rules for presenting and validating bearer tokens. |

## Cross-References

- [API Glossary](/docs/blueprint/volume-10-api/appendices/api-glossary.md)
- [REST Conventions](/docs/blueprint/volume-10-api/appendices/rest-conventions.md)
- [OpenAPI Template](/docs/blueprint/volume-10-api/appendices/openapi-template.md)

## References

- [Volume 01 - Vision and Philosophy](/docs/blueprint/volume-01-vision-and-philosophy/README.md)
- [Document Standards](/docs/governance/document-standards.md)

## Change Log

| Version | Date | Author | Notes |
|---|---|---|---|
| 1.0 | 2026-07-12 | Lead Software Engineer | Initial approved version. |
