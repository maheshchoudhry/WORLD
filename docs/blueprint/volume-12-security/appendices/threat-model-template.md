# Volume 12 - Threat Model Template

| Field | Value |
|---|---|
| Document ID | WORLD-VOL12-A4 |
| Title | Threat Model Template |
| Version | 1.0 |
| Status | Approved |
| Classification | Internal |
| Founder | Mahesh Choudhary |

## Purpose

This appendix provides a reusable threat-model template for Project WORLD, based on the STRIDE methodology. Its purpose is to make threat modeling a repeatable, comparable discipline rather than an ad hoc exercise: every feature, service, or trust boundary can be analyzed with the same structure, so that assets, threats, and mitigations are captured consistently and can be reviewed, tracked, and audited. Threat modeling is the point at which security shifts from reactive to proactive, and a shared template ensures that shift happens the same way across every team.

## Scope

The template covers the identification of assets and trust boundaries, the enumeration of threats using the six STRIDE categories, the mapping of each threat to a mitigating control, and the assessment of residual risk. It applies to new features, significant changes, and periodic reviews of existing systems. It is methodology-level and does not prescribe a specific tool; teams may capture the model in any medium that preserves the structure below. A completed worked example is included to demonstrate the expected depth and style.

## STRIDE Categories

| Category | Threat | Violated Property |
|---|---|---|
| Spoofing | Impersonating another identity. | Authentication |
| Tampering | Modifying data or code without authorization. | Integrity |
| Repudiation | Denying an action without a record to prove otherwise. | Non-repudiation |
| Information Disclosure | Exposing data to unauthorized subjects. | Confidentiality |
| Denial of Service | Degrading or denying availability to legitimate users. | Availability |
| Elevation of Privilege | Gaining rights beyond those granted. | Authorization |

## How to Use This Template

| Step | Activity |
|---|---|
| 1. Scope | Define the system, feature, or change under analysis and its boundaries. |
| 2. Diagram | Draw data flows and mark trust boundaries where data crosses privilege levels. |
| 3. Identify Assets | List the assets worth protecting and their sensitivity. |
| 4. Enumerate Threats | For each asset and boundary, walk the six STRIDE categories. |
| 5. Mitigate | Map each credible threat to one or more controls from the Controls Catalog. |
| 6. Rate Residual Risk | Assess likelihood and impact after mitigation; record the residual rating. |
| 7. Track | Assign owners and due dates to any actions and review on change. |

## Threat Model Template

| Asset | Threat | STRIDE Category | Mitigation | Residual Risk |
|---|---|---|---|---|
| _\<asset\>_ | _\<threat description\>_ | _\<STRIDE category\>_ | _\<control(s) applied\>_ | _\<Low / Medium / High\>_ |

## Risk Rating Guide

| Rating | Meaning |
|---|---|
| Low | Unlikely to occur, or limited impact even if it does; accept and monitor. |
| Medium | Plausible occurrence with meaningful impact; mitigate on a defined timeline. |
| High | Likely occurrence or severe impact; mitigate before release. |

## Worked Example: User Authentication Service

The following is a filled sample for a user-facing authentication service that issues session tokens after verifying credentials.

| Asset | Threat | STRIDE Category | Mitigation | Residual Risk |
|---|---|---|---|---|
| User credentials | Attacker guesses passwords through automated attempts | Spoofing | MFA (IA-01), rate limiting (AP-06), account lockout | Low |
| Session token | Attacker steals a token in transit and replays it | Spoofing | Encryption in transit (CR-01), short-lived tokens, session revocation (EP-03) | Low |
| Login request | Attacker alters request parameters to bypass checks | Tampering | Input validation (AP-01), integrity-protected transport | Low |
| Authentication event | User denies a sensitive action was theirs | Repudiation | Centralized audit logging (TD-01), non-repudiable event records | Low |
| Credential store | Attacker reads stored password material | Information Disclosure | Encryption at rest (CR-02), salted one-way hashing, secrets management (CR-03) | Low |
| Login endpoint | Attacker floods the endpoint to deny service | Denial of Service | Rate limiting (AP-06), DDoS protection (NW-05), web application firewall (AP-05) | Medium |
| Session privileges | User escalates to administrative rights | Elevation of Privilege | Least-privilege authorization (IA-02), RBAC (IA-03), server-side authorization checks | Low |

## Cross-References

- [Security Controls Catalog](/docs/blueprint/volume-12-security/appendices/security-controls-catalog.md)
- [Authentication](/docs/blueprint/volume-12-security/section-b-identity-and-access/04-authentication.md)
- [Incident Response Playbook](/docs/blueprint/volume-12-security/appendices/incident-response-playbook.md)

## References

- [Volume 01 - Vision and Philosophy](/docs/blueprint/volume-01-vision-and-philosophy/README.md)
- [Document Standards](/docs/governance/document-standards.md)

## Change Log

| Version | Date | Author | Notes |
|---|---|---|---|
| 1.0 | 2026-07-12 | Lead Software Engineer | Initial approved version. |
