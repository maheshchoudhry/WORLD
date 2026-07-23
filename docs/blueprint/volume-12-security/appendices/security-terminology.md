# Volume 12 - Security Terminology

| Field | Value |
|---|---|
| Document ID | WORLD-VOL12-A2 |
| Title | Security Terminology |
| Version | 1.0 |
| Status | Approved |
| Classification | Internal |
| Founder | Mahesh Choudhary |

## Purpose

This appendix defines the controlled vocabulary for Project WORLD's security tier. Where the Glossary (Appendix A1) explains what terms mean, this document fixes which terms are canonical, how they must be used, and which synonyms must be avoided. Its purpose is consistency across chapters, policies, threat models, incident reports, and control catalogs, so that one concept is always named one way. Controlled terminology matters most during incidents and audits, when precision, speed, and defensibility are all required at once, and where a loose synonym can misdirect a response or weaken an attestation.

## Scope

The controlled vocabulary covers the naming of core security concepts, actors, controls, credentials, and events used throughout Volume 12. It applies to prose, diagrams, policy documents, control identifiers, and security tooling. It does not govern business-domain nouns (owned by Volume 05), infrastructure resource names (owned by Volume 11), or API contract terms (owned by Volume 10). Each entry gives the approved canonical term, its approved usage, and the terms to avoid. Deviations require review by the security governance function.

## Controlled Vocabulary

| Canonical Term | Approved Usage | Terms to Avoid |
|---|---|---|
| Authentication | Verifying the claimed identity of a subject. | Login (as a synonym for the process), sign-in (in formal docs), auth (bare) |
| Authorization | Deciding whether an authenticated subject may act. | Permissioning, access check (loosely), auth (bare) |
| Identity | The canonical record of a subject in the system. | Account (when identity is meant), user (for non-human subjects), profile |
| Principal | The authenticated subject making a request. | User (when a service is meant), caller (loosely), requester |
| Credential | A secret or token proving identity. | Password (generically), login details, key (when a broader credential is meant) |
| Secret | Sensitive value handled through the secrets manager. | Password (generically), API key (when any secret is meant), config value |
| Multi-Factor Authentication | Authentication using two or more independent factors. | Two-step (in formal docs), 2FA (when more than two factors apply), strong auth |
| Least Privilege | Granting only the minimum access required. | Minimal access (loosely), need-to-know (when access is meant), lockdown |
| Zero Trust | The model of never trusting implicitly and always verifying. | Perimeterless (loosely), trustless, ZT (bare in prose) |
| Control | A safeguard that reduces security risk. | Measure (loosely), feature (when a control is meant), setting |
| Threat | A potential cause of an unwanted incident. | Risk (when a threat is meant), attack (when only potential), vulnerability |
| Vulnerability | A weakness that a threat can exploit. | Bug (when security-relevant), flaw (loosely), hole |
| Risk | The effect of uncertainty, as likelihood times impact. | Threat (when risk is meant), exposure (loosely), danger |
| Incident | A confirmed or suspected harmful security event. | Breach (when unconfirmed), event (when it warrants response), issue |
| Breach | A confirmed unauthorized access to or disclosure of data. | Incident (when a breach is confirmed), hack, leak (loosely) |
| Encryption | Reversible transformation of data using a key. | Encoding (when encryption is meant), hashing (when encryption is meant), scrambling |
| Hashing | One-way digest for integrity or verification. | Encryption (when hashing is meant), encoding (loosely) |
| Audit Log | The append-only, tamper-evident event record. | Log (generically), history, trail (loosely) |
| Certificate | A signed binding of a public key to an identity. | Cert (in formal docs), SSL cert (when TLS is meant), key (when a certificate is meant) |
| Session | A bounded authenticated interaction. | Connection (when a session is meant), login (as a noun), token |

## Usage Principles

| Principle | Statement |
|---|---|
| One Concept, One Term | Each concept has exactly one canonical term; synonyms are not interchangeable in official artifacts. |
| Authentication Versus Authorization | Verifying identity is always authentication; deciding permitted actions is always authorization. |
| Threat, Vulnerability, Risk Are Distinct | These three terms are never used interchangeably; each has a precise, separate meaning. |
| Incident Language Is Precise | During response, canonical terms are used verbatim, and "breach" is reserved for confirmed unauthorized access. |
| Verify Explicitly | Security prose favors explicit verification language over any implication of implicit trust. |

## Cross-References

- [Security Glossary](/docs/blueprint/volume-12-security/appendices/security-glossary.md)
- [Authentication](/docs/blueprint/volume-12-security/section-b-identity-and-access/04-authentication.md)
- [Authorization](/docs/blueprint/volume-12-security/section-b-identity-and-access/05-authorization.md)

## References

- [Volume 01 - Vision and Philosophy](/docs/blueprint/volume-01-vision-and-philosophy/README.md)
- [Document Standards](/docs/governance/document-standards.md)

## Change Log

| Version | Date | Author | Notes |
|---|---|---|---|
| 1.0 | 2026-07-12 | Lead Software Engineer | Initial approved version. |
