# Volume 10 - API Glossary

| Field | Value |
|---|---|
| Document ID | WORLD-VOL10-A1 |
| Title | API Glossary |
| Version | 1.0 |
| Status | Approved |
| Classification | Internal |
| Founder | Mahesh Choudhary |

## Purpose

This appendix provides a single, authoritative glossary of the API terms used throughout Volume 10. Its purpose is to remove ambiguity: when a chapter, an interface contract, or a design review uses a term such as *idempotency*, *bearer token*, or *back-pressure*, this glossary fixes its meaning for Project WORLD. A shared vocabulary is a precondition for a coherent API tier, because REST resources, GraphQL schemas, event contracts, gateways, and SDKs can only interoperate if their authors mean the same thing by the same word.

## Scope

The glossary defines API and integration terms that appear in Volume 10, Sections A through G, together with a small number of adjacent terms needed to make those definitions self-contained. Definitions are concise and platform-neutral. It does not redefine database terms (governed by Volume 09) nor architectural terms (governed by Volume 08), and it does not fix concrete technology choices. Where a term has a broader meaning in general usage, the definition given here is the WORLD-canonical one.

## Glossary

| Term | Definition |
|---|---|
| API Gateway | A managed entry point that fronts backend services to handle routing, authentication, rate limiting, and observability for API traffic. |
| API Key | A static, opaque credential issued to a client to identify and authorize calling applications, typically for server-to-server access. |
| AsyncAPI | A specification for describing message-driven and event-driven APIs, the asynchronous counterpart to OpenAPI. |
| Authentication (AuthN) | The process of verifying the identity of a caller (a user, service, or application). |
| Authorization (AuthZ) | The process of determining whether an authenticated caller is permitted to perform a requested operation. |
| Back-pressure | A flow-control signal by which a consumer slows a producer to prevent overload in a streaming or messaging system. |
| Bearer Token | A credential that grants access to whoever presents it (the bearer), commonly a signed JWT or opaque access token. |
| Breaking Change | A change to an API contract that requires consumers to modify their code to keep working. |
| Circuit Breaker | A resilience pattern that stops calls to a failing dependency for a cooldown period to prevent cascading failure. |
| Client (Consumer) | Any application or service that calls an API. |
| Contract | The formal, versioned agreement describing an API's requests, responses, errors, and behavior. |
| CORS | Cross-Origin Resource Sharing; the browser mechanism that governs which origins may call an API from client-side code. |
| Cursor Pagination | A pagination technique that returns an opaque pointer to the next page rather than a numeric offset. |
| Dead-Letter Queue (DLQ) | A queue that receives messages that cannot be processed successfully after retries, for later inspection. |
| Deprecation | The formal marking of an API element as obsolete and scheduled for removal, while it remains temporarily available. |
| Endpoint | A specific, addressable URL and method combination through which an API operation is invoked. |
| Envelope | A consistent wrapper structure around a response or error payload (for example, data, meta, and error fields). |
| ETag | An entity-tag header identifying a specific version of a resource, used for caching and optimistic concurrency. |
| Event | An immutable record that something of business significance has happened, published for interested consumers. |
| Event Bus | The shared messaging backbone that transports events between producers and consumers asynchronously. |
| Event Contract | The versioned schema and semantics of an event, defining its name, payload, and delivery guarantees. |
| Exponential Backoff | A retry strategy that increases the wait between attempts geometrically, usually with random jitter. |
| Gateway Route | A configured mapping from an inbound API path to a backend service target at the gateway. |
| GraphQL | A query language and runtime that lets clients request exactly the fields they need from a typed schema. |
| gRPC | A high-performance RPC framework using HTTP/2 and Protocol Buffers for typed, binary service-to-service calls. |
| HATEOAS | Hypermedia as the Engine of Application State; a REST constraint where responses embed links to related actions. |
| Idempotency | The property that applying an operation more than once has the same effect as applying it once. |
| Idempotency Key | A client-supplied token that lets a server safely de-duplicate repeated write requests. |
| JSON:API | A specification defining a conventional structure for JSON request and response documents. |
| JWT | JSON Web Token; a compact, signed token format carrying claims about a subject between parties. |
| Mutual TLS (mTLS) | A protocol in which both client and server present certificates to authenticate each other. |
| OpenAPI | A machine-readable specification format for describing RESTful HTTP APIs and their schemas. |
| Idempotent Method | An HTTP method (GET, PUT, DELETE, HEAD) whose repeated invocation yields the same server state. |
| OAuth 2.0 | An authorization framework that issues scoped access tokens to clients on a resource owner's behalf. |
| OIDC | OpenID Connect; an identity layer on top of OAuth 2.0 that provides authenticated user identity via ID tokens. |
| Payload | The body of a request, response, or message carrying the actual data. |
| Polling | A pattern where a client repeatedly requests a resource to detect changes, contrasted with webhooks. |
| Rate Limiting | The controlled restriction of how many requests a client may make within a time window. |
| Resource | A named, addressable business concept exposed by a REST API (for example, an order or an invoice). |
| REST | Representational State Transfer; an architectural style for networked APIs built on HTTP resources and methods. |
| RPC | Remote Procedure Call; an interaction style that models an API as callable functions rather than resources. |
| Scope | A named permission attached to an access token that bounds what the token may do. |
| SDK | Software Development Kit; a client library that wraps an API in an idiomatic, language-native interface. |
| Service Mesh | An infrastructure layer that manages service-to-service traffic, security, and observability transparently. |
| Throttling | The deliberate slowing or rejection of requests once a rate or concurrency threshold is exceeded. |
| Token Introspection | An endpoint that lets a resource server validate and inspect the metadata of an access token. |
| Versioning | The discipline of evolving an API through explicit versions so consumers are not broken unexpectedly. |
| Webhook | An HTTP callback by which a provider pushes an event to a consumer-registered URL. |

## Cross-References

- [API Philosophy](/docs/blueprint/volume-10-api/section-a-api-foundations/01-api-philosophy.md)
- [REST Standards](/docs/blueprint/volume-10-api/section-a-api-foundations/02-rest-standards.md)
- [API Terminology](/docs/blueprint/volume-10-api/appendices/api-terminology.md)

## References

- [Volume 01 - Vision and Philosophy](/docs/blueprint/volume-01-vision-and-philosophy/README.md)
- [Document Standards](/docs/governance/document-standards.md)

## Change Log

| Version | Date | Author | Notes |
|---|---|---|---|
| 1.0 | 2026-07-12 | Lead Software Engineer | Initial approved version. |
