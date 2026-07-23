# Volume 12 - References

| Field | Value |
|---|---|
| Document ID | WORLD-VOL12-A7 |
| Title | References |
| Version | 1.0 |
| Status | Approved |
| Classification | Internal |
| Founder | Mahesh Choudhary |

## Purpose

This appendix collects the established, real-world security works, standards, and frameworks on which Volume 12 draws. Its purpose is intellectual honesty and traceability: WORLD's security tier is not invented in a vacuum but stands on a mature body of specifications, catalogs, and reference practice. Naming those sources lets a reader verify the reasoning, go deeper, and understand which ideas WORLD has adopted, adapted, or deliberately extended.

## Scope

The document lists foundational references grouped by topic, covering security frameworks and control catalogs, identity and access, application and API security, hardening baselines, zero trust, threat intelligence and detection, and privacy and compliance. Each entry names the work and its author or issuing body; formal citation details can be resolved from these names through their official publishers or standards bodies. To preserve accuracy, this appendix does not fabricate URLs or invent bibliographic identifiers. It is a curated starting point, not an exhaustive bibliography.

## Security Frameworks and Control Catalogs

| Reference | Author / Origin | Relevance to WORLD |
|---|---|---|
| NIST Cybersecurity Framework (CSF) | US National Institute of Standards and Technology | Core functions structuring WORLD's security posture. |
| NIST SP 800-53 Security and Privacy Controls | US National Institute of Standards and Technology | Reference catalog behind the Controls Catalog. |
| ISO/IEC 27001 Information Security Management | ISO and IEC | Reference for the security management system. |
| ISO/IEC 27002 Information Security Controls | ISO and IEC | Reference for control selection and implementation guidance. |

## Identity and Access

| Reference | Author / Origin | Relevance to WORLD |
|---|---|---|
| NIST SP 800-63 Digital Identity Guidelines | US National Institute of Standards and Technology | Reference for authentication assurance and identity proofing. |
| OAuth 2.0 Authorization Framework | IETF | Foundation for delegated authorization. |
| OpenID Connect | OpenID Foundation | Reference for federated authentication and SSO. |
| Role-Based Access Control Model | David Ferraiolo and Richard Kuhn (NIST) | Foundational model behind RBAC in Section B. |

## Application and API Security

| Reference | Author / Origin | Relevance to WORLD |
|---|---|---|
| OWASP Top 10 | Open Worldwide Application Security Project | Reference for common web application risks. |
| OWASP API Security Top 10 | Open Worldwide Application Security Project | Reference for API-specific risks in Section D. |
| OWASP Application Security Verification Standard | Open Worldwide Application Security Project | Reference for application security requirements. |
| OWASP Threat Modeling and STRIDE | OWASP / Microsoft | Basis for the Threat Model Template in Appendix A4. |

## Hardening and Baselines

| Reference | Author / Origin | Relevance to WORLD |
|---|---|---|
| CIS Benchmarks | Center for Internet Security | Reference for system and cloud hardening baselines. |
| CIS Critical Security Controls | Center for Internet Security | Prioritized reference set of defensive actions. |
| NIST SP 800-123 Server Security | US National Institute of Standards and Technology | Reference for server hardening. |
| CSA Cloud Controls Matrix | Cloud Security Alliance | Reference for cloud control domains in Section D. |

## Zero Trust

| Reference | Author / Origin | Relevance to WORLD |
|---|---|---|
| NIST SP 800-207 Zero Trust Architecture | US National Institute of Standards and Technology | Foundation for the Zero Trust chapter in Section A. |
| BeyondCorp | Google | Reference implementation of enterprise zero trust. |
| Zero Trust Networks | Evan Gilman and Doug Barth | Conceptual reference for perimeterless design. |

## Threat Intelligence and Detection

| Reference | Author / Origin | Relevance to WORLD |
|---|---|---|
| MITRE ATT&CK | MITRE Corporation | Reference knowledge base of adversary tactics and techniques. |
| NIST SP 800-61 Computer Security Incident Handling | US National Institute of Standards and Technology | Foundation for the Incident Response Playbook in Appendix A5. |
| MITRE D3FEND | MITRE Corporation | Reference framework mapping defensive countermeasures. |
| Pyramid of Pain | David Bianco | Reference model for the value of indicators of compromise. |

## Privacy and Compliance

| Reference | Author / Origin | Relevance to WORLD |
|---|---|---|
| SOC 2 Trust Services Criteria | AICPA | Reference for the attestation criteria in the Compliance Matrix. |
| General Data Protection Regulation (GDPR) | European Union | Reference for personal data protection obligations. |
| PCI DSS | PCI Security Standards Council | Reference for payment card data protection. |
| ISO/IEC 27701 Privacy Information Management | ISO and IEC | Reference for privacy management extending 27001. |

## Cross-References

- [Security Glossary](/docs/blueprint/volume-12-security/appendices/security-glossary.md)
- [Compliance Matrix](/docs/blueprint/volume-12-security/appendices/compliance-matrix.md)
- [Security Controls Catalog](/docs/blueprint/volume-12-security/appendices/security-controls-catalog.md)

## References

- [Volume 01 - Vision and Philosophy](/docs/blueprint/volume-01-vision-and-philosophy/README.md)
- [Document Standards](/docs/governance/document-standards.md)

## Change Log

| Version | Date | Author | Notes |
|---|---|---|---|
| 1.0 | 2026-07-12 | Lead Software Engineer | Initial approved version. |
