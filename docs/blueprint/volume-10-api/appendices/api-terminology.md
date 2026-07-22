# Volume 10 - API Terminology

| Field | Value |
|---|---|
| Document ID | WORLD-VOL10-A2 |
| Title | API Terminology |
| Version | 1.0 |
| Status | Approved |
| Classification | Internal |
| Founder | Mahesh Choudhary |

## Purpose

This appendix defines the controlled vocabulary for Project WORLD's API tier. Where the Glossary (Appendix A1) explains what terms mean, this document fixes which terms are canonical, how they must be used, and which synonyms must be avoided. Its purpose is consistency across chapters, code, OpenAPI documents, SDKs, and developer-facing documentation, so that one concept is always named one way. Controlled terminology reduces cognitive load for both internal engineers and external integrators.

## Scope

The controlled vocabulary covers the naming of core API concepts, actors, artifacts, and operations used throughout Volume 10. It applies to prose, diagrams, schema field names, and public documentation. It does not govern business-domain nouns (owned by Volume 05) or database object names (owned by Volume 09). Each entry gives the approved canonical term, its approved usage, and the terms to avoid. Deviations require review by the API governance function.

## Controlled Vocabulary

| Canonical Term | Approved Usage | Terms to Avoid |
|---|---|---|
| Consumer | The application or service that calls a WORLD API. | User (when meaning an app), caller-app, client-app |
| Provider | The WORLD service that owns and exposes an API. | Producer (except for events), server-side |
| Resource | A noun-based, addressable REST entity. | Object, entity (in REST prose), record |
| Endpoint | A method-plus-path operation on a resource. | Route (except at the gateway), URL, API call |
| Event | An immutable fact published to the event bus. | Message (when a business fact is meant), notification |
| Message | The transport-level envelope carrying an event or command. | Event (when transport is meant), packet |
| Webhook | A provider-to-consumer HTTP callback subscription. | Callback URL, reverse API, push endpoint |
| Access Token | The short-lived credential presented on API calls. | Auth token, session token, API token |
| API Key | The static application credential for server-to-server calls. | Secret key, app secret, client key |
| Scope | A named permission bound to a token. | Role (at token level), permission-string |
| Rate Limit | The configured request ceiling per client and window. | Quota (when meaning per-window), throttle limit |
| Quota | The longer-horizon allowance (for example, per month). | Rate limit (when meaning per-window), cap |
| Idempotency Key | The client token that de-duplicates writes. | Request ID (for de-dup), dedupe token |
| Correlation ID | The identifier that links related calls across services. | Trace ID (when meaning correlation), request key |
| Error Code | The stable, machine-readable error identifier. | Error message (as identifier), status text |
| Version | An explicit, released API contract version. | Revision, build, iteration |
| Deprecation | The formal, announced obsolescence of an API element. | Retirement (that is the later removal), sunset (as a verb) |
| Sunset | The scheduled date an element stops being served. | Kill date, end-of-life (in headers) |
| Schema | The typed structure of a payload or model. | Model (in OpenAPI prose), shape, format |
| Gateway | The single managed ingress for external API traffic. | Proxy, edge server, load balancer |
| SDK | The official generated or maintained client library. | Wrapper, connector, client (when a library is meant) |

## Usage Principles

| Principle | Statement |
|---|---|
| One Concept, One Term | Each concept has exactly one canonical term; synonyms are not interchangeable in official artifacts. |
| Nouns for Resources | Resources are named with plural nouns; verbs are expressed through HTTP methods, not resource names. |
| Consumer-First Language | Documentation addresses the integrating consumer, favouring their perspective over internal implementation words. |
| Stable Machine Identifiers | Error codes, scopes, and event names are stable strings and must not be renamed within a major version. |
| Explicit Over Implicit | Versions, deprecations, and sunset dates are always stated explicitly, never assumed. |

## Cross-References

- [API Glossary](/docs/blueprint/volume-10-api/appendices/api-glossary.md)
- [REST Conventions](/docs/blueprint/volume-10-api/appendices/rest-conventions.md)
- [Versioning](/docs/blueprint/volume-10-api/section-c-api-security-and-access/11-versioning.md)

## References

- [Volume 01 - Vision and Philosophy](/docs/blueprint/volume-01-vision-and-philosophy/README.md)
- [Document Standards](/docs/governance/document-standards.md)

## Change Log

| Version | Date | Author | Notes |
|---|---|---|---|
| 1.0 | 2026-07-12 | Lead Software Engineer | Initial approved version. |
