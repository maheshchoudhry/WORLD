# Volume 10 - REST Conventions

| Field | Value |
|---|---|
| Document ID | WORLD-VOL10-A3 |
| Title | REST Conventions |
| Version | 1.0 |
| Status | Approved |
| Classification | Internal |
| Founder | Mahesh Choudhary |

## Purpose

This appendix is the canonical reference for how WORLD builds RESTful HTTP APIs. It consolidates the resource naming, HTTP method, status code, pagination, filtering, sorting, idempotency, and error-envelope rules into one normative source. Its purpose is to make every WORLD REST API predictable: a consumer who learns one endpoint should be able to guess the shape of the next. Consistency of this kind is a product feature, because it lowers integration cost and error rates across the entire platform.

## Scope

The conventions apply to all internal, external, and public REST APIs in Project WORLD. They complement Chapter 02 (REST Standards) with reference tables and examples. They do not govern GraphQL (Chapter 03), event contracts (Section E), or gRPC service definitions, which follow their own conventions. Where a convention here conflicts with a legacy interface, the legacy interface is brought into line at its next major version.

## Resource Naming

| Rule | Convention | Example |
|---|---|---|
| Nouns, not verbs | Resources are named with nouns; actions come from methods. | `/orders` not `/getOrders` |
| Plural collections | Collections use plural nouns. | `/invoices`, `/customers` |
| Lowercase, hyphenated | Multi-word paths use kebab-case. | `/purchase-orders` |
| Hierarchy for containment | Sub-resources express ownership. | `/orders/{orderId}/line-items` |
| Identifiers in path | A single resource is addressed by its identifier. | `/customers/{customerId}` |
| No file extensions | Content type is negotiated by header, not suffix. | `Accept: application/json` |
| Query for filtering | Filtering and shaping use the query string, not new paths. | `/orders?status=open` |

## HTTP Methods

| Method | Purpose | Safe | Idempotent | Typical Success |
|---|---|---|---|---|
| GET | Retrieve a resource or collection. | Yes | Yes | 200 OK |
| POST | Create a resource or invoke a non-idempotent action. | No | No | 201 Created |
| PUT | Create or fully replace a resource at a known identifier. | No | Yes | 200 OK / 204 No Content |
| PATCH | Partially update a resource. | No | No | 200 OK |
| DELETE | Remove a resource. | No | Yes | 204 No Content |
| HEAD | Retrieve headers only for a resource. | Yes | Yes | 200 OK |
| OPTIONS | Discover permitted methods and CORS policy. | Yes | Yes | 204 No Content |

## Status Codes

| Code | Meaning | When to Use |
|---|---|---|
| 200 OK | Success with body. | Successful GET, PATCH, or PUT returning content. |
| 201 Created | Resource created. | Successful POST; include a `Location` header. |
| 202 Accepted | Accepted for async processing. | Long-running work started but not finished. |
| 204 No Content | Success without body. | Successful DELETE or PUT with no response body. |
| 400 Bad Request | Malformed or invalid request. | Validation failure or unparseable payload. |
| 401 Unauthorized | Missing or invalid authentication. | No valid token or key presented. |
| 403 Forbidden | Authenticated but not permitted. | Valid identity lacking the required scope. |
| 404 Not Found | Resource does not exist. | Unknown identifier or hidden resource. |
| 409 Conflict | State conflict. | Version conflict or duplicate creation. |
| 422 Unprocessable Entity | Semantically invalid. | Well-formed request that fails business rules. |
| 429 Too Many Requests | Rate limit exceeded. | Client exceeded its rate limit or quota. |
| 500 Internal Server Error | Unexpected server fault. | Unhandled error; never leak internals. |
| 503 Service Unavailable | Temporary unavailability. | Dependency down or maintenance; include `Retry-After`. |

## Pagination

| Aspect | Convention | Example |
|---|---|---|
| Default style | Cursor-based pagination for large or volatile collections. | `/orders?limit=50&cursor=eyJpZCI6...` |
| Page size | `limit` parameter with a sane default and maximum. | `limit=50` (default 25, max 100) |
| Next page | Opaque `cursor` returned in response metadata. | `meta.next_cursor` |
| Offset option | Offset pagination permitted only for small, stable sets. | `/audit-logs?offset=100&limit=50` |
| Metadata | Page context returned under a `meta` object. | `{ "meta": { "next_cursor": "...", "limit": 50 } }` |

## Filtering, Sorting, and Field Selection

| Capability | Convention | Example |
|---|---|---|
| Filtering | `field=value` query parameters, AND-combined. | `/orders?status=open&channel=web` |
| Range filtering | Suffix operators for ranges. | `/orders?created_at.gte=2026-07-01` |
| Sorting | `sort` with comma-separated fields; `-` prefix for descending. | `/orders?sort=-created_at,total` |
| Field selection | `fields` to request a sparse response. | `/orders?fields=id,status,total` |
| Search | `q` for free-text search where supported. | `/customers?q=acme` |

## Idempotency

| Rule | Convention |
|---|---|
| Idempotent methods | GET, PUT, DELETE, and HEAD are idempotent by contract. |
| Idempotent POST | Unsafe creates accept an `Idempotency-Key` header to de-duplicate retries. |
| Key scope | An idempotency key is unique per consumer and operation, retained for a defined window (for example, 24 hours). |
| Replay behavior | A repeated key returns the original stored response, not a new side effect. |
| Conflicts | A reused key with a different payload returns `422 Unprocessable Entity`. |

### Idempotent Create Example

```http
POST /v1/payments HTTP/1.1
Host: api.world.example
Authorization: Bearer eyJhbGciOi...
Idempotency-Key: 5f2b9c1a-7e64-4c3a-9b21-2a0d6f8e1c44
Content-Type: application/json

{ "amount": 4200, "currency": "USD", "order_id": "ord_10293" }
```

## Error Envelope

All error responses share one envelope so consumers parse errors uniformly.

```json
{
  "error": {
    "code": "VALIDATION_FAILED",
    "message": "The request failed validation.",
    "status": 422,
    "correlation_id": "c-9a3f21b7e0",
    "details": [
      { "field": "amount", "issue": "must be greater than zero" }
    ],
    "doc_url": "https://developer.world.example/errors/VALIDATION_FAILED"
  }
}
```

| Field | Meaning |
|---|---|
| code | Stable, machine-readable error identifier. |
| message | Human-readable, non-localized summary. |
| status | Mirrored HTTP status code. |
| correlation_id | Identifier linking the error to server logs and traces. |
| details | Optional array of field-level or contextual issues. |
| doc_url | Link to the catalog entry for the error code. |

## Cross-References

- [REST Standards](/docs/blueprint/volume-10-api/section-a-api-foundations/02-rest-standards.md)
- [Error Catalog](/docs/blueprint/volume-10-api/appendices/error-catalog.md)
- [OpenAPI Standards](/docs/blueprint/volume-10-api/section-d-developer-tooling/15-openapi-standards.md)
- [API Terminology](/docs/blueprint/volume-10-api/appendices/api-terminology.md)

## References

- [Volume 01 - Vision and Philosophy](/docs/blueprint/volume-01-vision-and-philosophy/README.md)
- [Document Standards](/docs/governance/document-standards.md)

## Change Log

| Version | Date | Author | Notes |
|---|---|---|---|
| 1.0 | 2026-07-12 | Lead Software Engineer | Initial approved version. |
