# Volume 12 - Security Glossary

| Field | Value |
|---|---|
| Document ID | WORLD-VOL12-A1 |
| Title | Security Glossary |
| Version | 1.0 |
| Status | Approved |
| Classification | Internal |
| Founder | Mahesh Choudhary |

## Purpose

This appendix provides a single, authoritative glossary of the security terms used throughout Volume 12. Its purpose is to remove ambiguity: when a chapter, a threat model, or an incident review uses a term such as *zero trust*, *least privilege*, or *blast radius*, this glossary fixes its meaning for Project WORLD. Security is a discipline in which imprecise language causes real harm, because controls, threats, and obligations can only be reasoned about together when their authors mean the same thing by the same word. A shared vocabulary is therefore a precondition for a coherent security tier.

## Scope

The glossary defines security and privacy terms that appear in Volume 12, Sections A through H, together with a small number of adjacent terms needed to make those definitions self-contained. Definitions are concise and vendor-neutral. It does not redefine infrastructure terms (governed by Volume 11), API terms (governed by Volume 10), or database terms (governed by Volume 09), and it does not fix concrete technology or product choices. Where a term has a broader meaning in general usage, the definition given here is the WORLD-canonical one for security contexts.

## Glossary

| Term | Definition |
|---|---|
| Access Control | The enforcement of rules that determine which subjects may perform which actions on which resources. |
| Access Token | A short-lived, verifiable credential presented to prove an authenticated, authorized session. |
| Attack Surface | The total set of points through which an unauthorized actor could attempt to enter or extract data. |
| Attribute-Based Access Control (ABAC) | An authorization model that grants access based on evaluated attributes of subject, resource, action, and context. |
| Audit Log | An append-only, tamper-evident record of security-relevant events for accountability and investigation. |
| Authentication (AuthN) | The process of verifying that a subject is who or what it claims to be. |
| Authorization (AuthZ) | The process of determining whether an authenticated subject may perform a requested action. |
| Blast Radius | The scope of systems, data, or users that a single compromise or failure can affect. |
| Certificate | A signed digital document binding a public key to an identity, issued by a certificate authority. |
| Certificate Authority (CA) | A trusted entity that issues, signs, and revokes digital certificates. |
| Ciphertext | Data that has been transformed by encryption so that it is unreadable without the key. |
| Confidentiality | The property that information is disclosed only to authorized subjects. |
| Credential | Any secret or token used to prove identity, such as a password, key, or certificate. |
| Cryptographic Key | A secret value that parameterizes an encryption, signing, or verification operation. |
| Data at Rest | Data stored on a persistent medium, as distinct from data moving across a network. |
| Data in Transit | Data moving across a network between endpoints. |
| Defense in Depth | A strategy of layering independent controls so that no single failure results in compromise. |
| Detective Control | A control that identifies and signals that an incident or policy violation has occurred. |
| Encryption | The reversible transformation of plaintext into ciphertext using a cryptographic key. |
| Endpoint | A device or workload that connects to and interacts with the system, such as a laptop or server. |
| Federation | The trust arrangement that lets identities from one domain be accepted in another. |
| Hardening | The process of reducing attack surface by removing or restricting unnecessary functionality. |
| Hash | A fixed-length, one-way digest of data used for integrity checks and verification. |
| Identity | The canonical representation of a subject (human, service, or device) within the system. |
| Identity Provider (IdP) | A service that authenticates subjects and issues assertions about their identity. |
| Incident | A confirmed or suspected event that harms, or threatens to harm, confidentiality, integrity, or availability. |
| Indicator of Compromise (IoC) | An observable artifact that suggests a system has been breached. |
| Integrity | The property that information and systems are accurate and have not been tampered with. |
| Key Management | The lifecycle governance of cryptographic keys: generation, storage, rotation, and destruction. |
| Key Rotation | The periodic replacement of a cryptographic key to limit exposure from compromise. |
| Least Privilege | The principle that a subject is granted only the minimum access required for its task. |
| Mutual TLS (mTLS) | A protocol in which both client and server present certificates to authenticate each other. |
| Multi-Factor Authentication (MFA) | Authentication requiring two or more independent factors from distinct categories. |
| Non-Repudiation | The assurance that a subject cannot credibly deny having performed a recorded action. |
| Penetration Test | An authorized, simulated attack to identify and validate exploitable weaknesses. |
| Phishing | A social-engineering attack that deceives a subject into revealing credentials or taking harmful action. |
| Plaintext | Readable data before encryption or after decryption. |
| Preventive Control | A control that stops an incident or policy violation from occurring. |
| Principal | The authenticated subject on whose behalf a request is made. |
| Privilege Escalation | The act of gaining higher access rights than were originally granted. |
| Public Key Infrastructure (PKI) | The system of authorities, policies, and certificates that manages public-key trust. |
| Corrective Control | A control that limits damage and restores systems after an incident has occurred. |
| Rate Limiting | Restricting the number of requests a subject may make in a time window to resist abuse. |
| Residual Risk | The risk that remains after controls have been applied. |
| Role-Based Access Control (RBAC) | An authorization model that grants access through roles assigned to subjects. |
| Secret | Sensitive configuration such as a credential, key, or token that must be stored and accessed securely. |
| Secrets Management | The governed storage, distribution, and rotation of secrets through a controlled system. |
| Security Information and Event Management (SIEM) | A system that aggregates, correlates, and alerts on security events. |
| Separation of Duties | The division of a sensitive task among multiple subjects to prevent unilateral misuse. |
| Session | A bounded, authenticated interaction between a subject and the system. |
| Single Sign-On (SSO) | A capability that lets a subject authenticate once and access multiple systems. |
| STRIDE | A threat-classification model: Spoofing, Tampering, Repudiation, Information disclosure, Denial of service, Elevation of privilege. |
| Threat | A potential cause of an unwanted incident that may harm a system or asset. |
| Threat Actor | An individual or group that carries out, or intends to carry out, a threat. |
| Threat Model | A structured analysis of assets, threats, and mitigations for a system or feature. |
| Token | A verifiable artifact that represents identity, authorization, or session state. |
| Vulnerability | A weakness that a threat can exploit to cause harm. |
| Zero Trust | A security model that assumes no implicit trust and verifies every request explicitly. |

## Cross-References

- [Security Philosophy](/docs/blueprint/volume-12-security/section-a-security-foundations/01-security-philosophy.md)
- [Zero Trust Architecture](/docs/blueprint/volume-12-security/section-a-security-foundations/02-zero-trust-architecture.md)
- [Security Terminology](/docs/blueprint/volume-12-security/appendices/security-terminology.md)

## References

- [Volume 01 - Vision and Philosophy](/docs/blueprint/volume-01-vision-and-philosophy/README.md)
- [Document Standards](/docs/governance/document-standards.md)

## Change Log

| Version | Date | Author | Notes |
|---|---|---|---|
| 1.0 | 2026-07-12 | Lead Software Engineer | Initial approved version. |
