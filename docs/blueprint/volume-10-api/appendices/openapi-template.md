# Volume 10 - OpenAPI Template

| Field | Value |
|---|---|
| Document ID | WORLD-VOL10-A4 |
| Title | OpenAPI Template |
| Version | 1.0 |
| Status | Approved |
| Classification | Internal |
| Founder | Mahesh Choudhary |

## Purpose

This appendix provides a reusable OpenAPI 3.x skeleton that every WORLD REST API begins from. Its purpose is to make specifications consistent and complete: by starting from one template, every team produces documents with the same structure for information, servers, paths, schemas, security, and errors. A shared skeleton accelerates authoring, enables reliable SDK and documentation generation, and makes contract review predictable.

## Scope

The template covers the core OpenAPI sections needed to describe a WORLD REST API: `info`, `servers`, `tags`, `paths`, reusable `components` (schemas, responses, parameters, and security schemes), and a global `security` declaration. It aligns with the REST Conventions (Appendix A3) and the Error Catalog (Appendix A5). It is a starting skeleton, not an exhaustive specification, and teams extend it with their domain resources. GraphQL and AsyncAPI contracts are described by their own formats and are out of scope here.

## OpenAPI 3.x Skeleton

```yaml
openapi: 3.1.0
info:
  title: WORLD Orders API
  version: 1.0.0
  description: >-
    Canonical REST API for the Orders domain of Project WORLD.
    Follows WORLD REST Conventions (Appendix A3) and the Error Catalog (Appendix A5).
  contact:
    name: WORLD API Platform
    url: https://developer.world.example
  license:
    name: Proprietary - Internal
servers:
  - url: https://api.world.example/v1
    description: Production
  - url: https://sandbox.api.world.example/v1
    description: Sandbox
tags:
  - name: Orders
    description: Create, retrieve, and manage orders.
security:
  - oauth2: [orders.read]
paths:
  /orders:
    get:
      summary: List orders
      operationId: listOrders
      tags: [Orders]
      security:
        - oauth2: [orders.read]
      parameters:
        - $ref: '#/components/parameters/Limit'
        - $ref: '#/components/parameters/Cursor'
        - name: status
          in: query
          schema: { type: string, enum: [open, paid, cancelled] }
      responses:
        '200':
          description: A page of orders.
          content:
            application/json:
              schema:
                type: object
                properties:
                  data:
                    type: array
                    items: { $ref: '#/components/schemas/Order' }
                  meta: { $ref: '#/components/schemas/PageMeta' }
        '401': { $ref: '#/components/responses/Unauthorized' }
        '429': { $ref: '#/components/responses/RateLimited' }
    post:
      summary: Create an order
      operationId: createOrder
      tags: [Orders]
      security:
        - oauth2: [orders.write]
      parameters:
        - $ref: '#/components/parameters/IdempotencyKey'
      requestBody:
        required: true
        content:
          application/json:
            schema: { $ref: '#/components/schemas/OrderCreate' }
      responses:
        '201':
          description: Order created.
          headers:
            Location:
              schema: { type: string }
              description: URL of the created order.
          content:
            application/json:
              schema: { $ref: '#/components/schemas/Order' }
        '422': { $ref: '#/components/responses/ValidationFailed' }
  /orders/{orderId}:
    get:
      summary: Retrieve an order
      operationId: getOrder
      tags: [Orders]
      parameters:
        - name: orderId
          in: path
          required: true
          schema: { type: string }
      responses:
        '200':
          description: The requested order.
          content:
            application/json:
              schema: { $ref: '#/components/schemas/Order' }
        '404': { $ref: '#/components/responses/NotFound' }
components:
  parameters:
    Limit:
      name: limit
      in: query
      schema: { type: integer, default: 25, minimum: 1, maximum: 100 }
    Cursor:
      name: cursor
      in: query
      schema: { type: string }
    IdempotencyKey:
      name: Idempotency-Key
      in: header
      required: false
      schema: { type: string, format: uuid }
  schemas:
    Order:
      type: object
      required: [id, status, total, currency, created_at]
      properties:
        id: { type: string, example: ord_10293 }
        status: { type: string, enum: [open, paid, cancelled] }
        total: { type: integer, description: Amount in minor units. }
        currency: { type: string, example: USD }
        created_at: { type: string, format: date-time }
    OrderCreate:
      type: object
      required: [customer_id, total, currency]
      properties:
        customer_id: { type: string }
        total: { type: integer, minimum: 1 }
        currency: { type: string }
    PageMeta:
      type: object
      properties:
        next_cursor: { type: string, nullable: true }
        limit: { type: integer }
    Error:
      type: object
      required: [error]
      properties:
        error:
          type: object
          required: [code, message, status]
          properties:
            code: { type: string }
            message: { type: string }
            status: { type: integer }
            correlation_id: { type: string }
            details:
              type: array
              items:
                type: object
                properties:
                  field: { type: string }
                  issue: { type: string }
  responses:
    Unauthorized:
      description: Authentication is missing or invalid.
      content:
        application/json:
          schema: { $ref: '#/components/schemas/Error' }
    NotFound:
      description: The resource was not found.
      content:
        application/json:
          schema: { $ref: '#/components/schemas/Error' }
    ValidationFailed:
      description: The request failed validation.
      content:
        application/json:
          schema: { $ref: '#/components/schemas/Error' }
    RateLimited:
      description: The rate limit was exceeded.
      headers:
        Retry-After:
          schema: { type: integer }
      content:
        application/json:
          schema: { $ref: '#/components/schemas/Error' }
  securitySchemes:
    oauth2:
      type: oauth2
      flows:
        clientCredentials:
          tokenUrl: https://auth.world.example/oauth/token
          scopes:
            orders.read: Read orders.
            orders.write: Create and modify orders.
    apiKey:
      type: apiKey
      in: header
      name: X-API-Key
```

## Authoring Guidance

| Guideline | Practice |
|---|---|
| Design-first | Author the specification before implementation; the contract is the source of truth. |
| Reuse components | Define shared schemas, parameters, and responses once under `components` and reference them. |
| Stable operationIds | Give every operation a stable `operationId`; SDK method names derive from it. |
| Consistent errors | Reference the shared `Error` schema for all failure responses. |
| Explicit security | Declare `security` globally and override per operation where scopes differ. |
| Version in path | Encode the major version in the server URL (`/v1`) and in `info.version`. |
| Examples everywhere | Provide realistic examples for schemas and responses to improve generated docs. |
| Lint in CI | Validate every specification against a style ruleset in continuous integration before merge. |

## Cross-References

- [OpenAPI Standards](/docs/blueprint/volume-10-api/section-d-developer-tooling/15-openapi-standards.md)
- [API Documentation](/docs/blueprint/volume-10-api/section-d-developer-tooling/14-api-documentation.md)
- [REST Conventions](/docs/blueprint/volume-10-api/appendices/rest-conventions.md)
- [Error Catalog](/docs/blueprint/volume-10-api/appendices/error-catalog.md)

## References

- [Volume 01 - Vision and Philosophy](/docs/blueprint/volume-01-vision-and-philosophy/README.md)
- [Document Standards](/docs/governance/document-standards.md)

## Change Log

| Version | Date | Author | Notes |
|---|---|---|---|
| 1.0 | 2026-07-12 | Lead Software Engineer | Initial approved version. |
