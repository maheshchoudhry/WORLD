# Volume 12 - Compliance Matrix

| Field | Value |
|---|---|
| Document ID | WORLD-VOL12-A6 |
| Title | Compliance Matrix |
| Version | 1.0 |
| Status | Approved |
| Classification | Internal |
| Founder | Mahesh Choudhary |

## Purpose

This appendix maps Project WORLD's security domains to the established external standards and frameworks that inform them. Its purpose is to demonstrate, at a glance, how WORLD's security tier aligns with widely recognized expectations for trust, privacy, and control, and to give auditors and customers a defensible bridge between internal design and external obligation. A compliance matrix turns "we take security seriously" into a traceable claim: each domain can be shown to correspond to named requirements in named frameworks.

## Scope

The matrix maps the security domains of Volume 12 to five widely used frameworks: SOC 2, ISO/IEC 27001, the EU General Data Protection Regulation (GDPR), the NIST Cybersecurity Framework (CSF), and PCI DSS. The mapping is at the level of framework areas, trust principles, and named domains. To preserve accuracy, this document deliberately does not cite specific clause, control, or article numbers, which change across framework versions and must be confirmed against the authoritative published text during a formal assessment. The matrix is an alignment aid and a starting point for audit scoping, not a certification or a substitute for a qualified assessment.

## Framework Overview

| Framework | Issuing Body | Nature |
|---|---|---|
| SOC 2 | AICPA | Attestation against the Trust Services Criteria. |
| ISO/IEC 27001 | ISO and IEC | Certifiable information security management system standard. |
| GDPR | European Union | Regulation governing the protection of personal data. |
| NIST CSF | US National Institute of Standards and Technology | Voluntary framework organized around core functions. |
| PCI DSS | PCI Security Standards Council | Standard for protecting payment card data. |

## Compliance Matrix

| WORLD Security Domain | SOC 2 (Trust Services Criteria) | ISO/IEC 27001 | GDPR | NIST CSF | PCI DSS |
|---|---|---|---|---|---|
| Identity and Access | Security, Confidentiality | Access control theme | Integrity and confidentiality principle | Protect function | Strong access control area |
| Cryptography and Secrets | Security, Confidentiality | Cryptography theme | Security of processing principle | Protect function | Protect stored and transmitted data area |
| Network Security | Security, Availability | Communications and network security theme | Security of processing principle | Protect function | Secure network and systems area |
| Application Security | Security, Processing Integrity | Secure development theme | Data protection by design principle | Protect function | Secure systems and software area |
| Data Security and Privacy | Confidentiality, Privacy | Information handling theme | Lawfulness, minimization, and rights principles | Protect function | Protect stored data area |
| Endpoint and Session | Security | Endpoint and asset management theme | Security of processing principle | Protect function | Access and system security areas |
| Threat Detection and Response | Security, Availability | Monitoring and incident management themes | Breach notification principle | Detect and Respond functions | Monitoring and testing areas |
| Compliance and Continuity | Availability | Business continuity theme | Accountability principle | Recover function | Security policy and continuity areas |
| Governance and Evolution | Security (control environment) | Leadership and improvement themes | Accountability principle | Govern and Identify functions | Security management policy area |

## Notes on Use

| Note | Guidance |
|---|---|
| Version sensitivity | Confirm mappings against the specific published version of each framework in force at assessment time. |
| No fabricated identifiers | Clause, control, and article numbers are intentionally omitted and must be sourced from authoritative texts. |
| Scope confirmation | A formal audit determines which systems and data fall within each framework's scope. |
| Living document | The matrix is reviewed when frameworks are revised or when WORLD's domains change materially. |

## Cross-References

- [Security Controls Catalog](/docs/blueprint/volume-12-security/appendices/security-controls-catalog.md)
- [Security Philosophy](/docs/blueprint/volume-12-security/section-a-security-foundations/01-security-philosophy.md)
- [References](/docs/blueprint/volume-12-security/appendices/references.md)

## References

- [Volume 01 - Vision and Philosophy](/docs/blueprint/volume-01-vision-and-philosophy/README.md)
- [Document Standards](/docs/governance/document-standards.md)

## Change Log

| Version | Date | Author | Notes |
|---|---|---|---|
| 1.0 | 2026-07-12 | Lead Software Engineer | Initial approved version. |
