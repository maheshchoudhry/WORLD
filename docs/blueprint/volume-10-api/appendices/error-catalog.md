# Volume 10 - Error Catalog

| Field | Value |
|---|---|
| Document ID | WORLD-VOL10-A5 |
| Title | Error Catalog |
| Version | 1.0 |
| Status | Approved |
| Classification | Internal |
| Founder | Mahesh Choudhary |

## Purpose

This appendix defines the standard API error model for Project WORLD and catalogs the canonical error codes that WORLD APIs return. Its purpose is to make failure as predictable as success: every WORLD API reports errors with the same envelope, the same stable codes, and the same retry semantics, so consumers can handle them programmatically. A shared error language turns error handling from guesswork into a contract.

## Scope

The catalog governs the error envelope, the meaning of each standard error code, its associated HTTP status, and whether the condition is safely retryable. It applies to all REST and webhook responses across WORLD. Domain-specific error codes extend this catalog but must reuse the same envelope and follow the same naming discipline. Transport-level failures handled entirely by the gateway (for example, TLS negotiation) are out of scope.

## Standard Error Model

Every error response uses a single envelope with a stable, machine-readable `code`.

| Field | Type | Description |
|---|---|---|
| error.code | string | Stable, uppercase, machine-readable identifier. |
| error.message | string | Human-readable, non-localized summary. |
| error.status | integer | Mirrored HTTP status code. |
| error.correlation_id | string | Identifier linking the error to logs and traces. |
| error.details | array | Optional field-level or contextual issues. |
| error.doc_url | string | Link to this catalog entry for the code. |

## Standard Error Codes

| HTTP Status | Error Code | Meaning | Retryable |
|---|---|---|---|
| 400 | BAD_REQUEST | The request is malformed or cannot be parsed. | No |
| 400 | INVALID_PARAMETER | A query or path parameter is invalid. | No |
| 401 | UNAUTHENTICATED | No valid authentication credential was supplied. | No |
| 401 | TOKEN_EXPIRED | The access token has expired. | Yes (after refresh) |
| 403 | FORBIDDEN | The caller lacks permission for this operation. | No |
| 403 | INSUFFICIENT_SCOPE | The token is missing a required scope. | No |
| 404 | NOT_FOUND | The requested resource does not exist. | No |
| 405 | METHOD_NOT_ALLOWED | The HTTP method is not supported for this resource. | No |
| 409 | CONFLICT | The request conflicts with the current resource state. | No |
| 409 | DUPLICATE_RESOURCE | A resource with the same identity already exists. | No |
| 412 | PRECONDITION_FAILED | An `If-Match` or version precondition failed. | No |
| 422 | VALIDATION_FAILED | The request is well-formed but fails business validation. | No |
| 422 | IDEMPOTENCY_KEY_REUSED | The idempotency key was reused with a different payload. | No |
| 429 | RATE_LIMITED | The client exceeded its rate limit or quota. | Yes (after Retry-After) |
| 500 | INTERNAL_ERROR | An unexpected server error occurred. | Yes |
| 502 | UPSTREAM_ERROR | A dependency returned an invalid response. | Yes |
| 503 | SERVICE_UNAVAILABLE | The service is temporarily unavailable. | Yes (after Retry-After) |
| 504 | UPSTREAM_TIMEOUT | A dependency did not respond in time. | Yes |

## Error Envelope Example

```json
{
  "error": {
    "code": "VALIDATION_FAILED",
    "message": "The request failed validation.",
    "status": 422,
    "correlation_id": "c-9a3f21b7e0",
    "details": [
      { "field": "currency", "issue": "must be a valid ISO 4217 code" },
      { "field": "total", "issue": "must be greater than zero" }
    ],
    "doc_url": "https://developer.world.example/errors/VALIDATION_FAILED"
  }
}
```

## Handling Guidance

| Guideline | Practice |
|---|---|
| Branch on code | Consumers branch on `error.code`, never on the free-text `message`. |
| Respect retryability | Retry only codes marked retryable, honoring any `Retry-After` header. |
| Log correlation IDs | Record `correlation_id` on the client to accelerate support and tracing. |
| Never leak internals | 5xx messages are generic; stack traces and internal identifiers are never exposed. |
| Backoff on 429 and 503 | Apply exponential backoff with jitter for throttling and unavailability. |

## Cross-References

- [REST Conventions](/docs/blueprint/volume-10-api/appendices/rest-conventions.md)
- [API Security](/docs/blueprint/volume-10-api/section-f-operations-and-quality/20-api-security.md)
- [Rate Limiting](/docs/blueprint/volume-10-api/section-c-api-security-and-access/12-rate-limiting.md)
- [Integration Templates](/docs/blueprint/volume-10-api/appendices/integration-templates.md)

## References

- [Volume 01 - Vision and Philosophy](/docs/blueprint/volume-01-vision-and-philosophy/README.md)
- [Document Standards](/docs/governance/document-standards.md)

## Change Log

| Version | Date | Author | Notes |
|---|---|---|---|
| 1.0 | 2026-07-12 | Lead Software Engineer | Initial approved version. |
