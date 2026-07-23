# Volume 12 - Security Controls Catalog

| Field | Value |
|---|---|
| Document ID | WORLD-VOL12-A3 |
| Title | Security Controls Catalog |
| Version | 1.0 |
| Status | Approved |
| Classification | Internal |
| Founder | Mahesh Choudhary |

## Purpose

This appendix catalogs the security controls that implement Volume 12's security posture. Its purpose is to give designers, reviewers, and auditors a single, structured inventory of the safeguards WORLD relies on, organized by domain and classified by control type. A named, typed control catalog turns abstract security principles into concrete, testable obligations: each entry can be assigned an owner, mapped to a standard, verified in a review, and referenced in a threat model or an incident report.

## Scope

The catalog covers preventive, detective, and corrective controls across the security domains of Volume 12: identity and access, cryptography and secrets, network, application, data, endpoint and session, threat detection and response, and governance. Each entry gives a control identifier, the control name, its type, and a concise description of what it does. The catalog is control-level and platform-neutral; it does not prescribe specific products, nor does it restate detailed procedures, which live in the relevant chapters and playbooks. Control types follow the standard classification: preventive controls stop incidents, detective controls surface them, and corrective controls contain and recover from them.

## Control Types

| Type | Intent |
|---|---|
| Preventive | Stops an unwanted event from occurring in the first place. |
| Detective | Identifies and signals that an unwanted event has occurred or is underway. |
| Corrective | Limits damage and restores normal operation after an event. |

## Identity and Access Controls

| ID | Control | Type | Description |
|---|---|---|---|
| IA-01 | Multi-Factor Authentication | Preventive | Requires two or more independent factors for all human access to sensitive systems. |
| IA-02 | Least-Privilege Authorization | Preventive | Grants subjects only the minimum permissions required for their function. |
| IA-03 | Role-Based Access Control | Preventive | Assigns permissions through governed roles rather than direct grants. |
| IA-04 | Attribute-Based Access Control | Preventive | Evaluates subject, resource, action, and context attributes at request time. |
| IA-05 | Just-in-Time Privileged Access | Preventive | Elevates privileges only for a bounded time against an approved request. |
| IA-06 | Access Certification Review | Detective | Periodically reviews and reattests entitlements to catch access creep. |
| IA-07 | Automated Deprovisioning | Corrective | Revokes access promptly when a subject changes role or leaves. |

## Cryptography and Secrets Controls

| ID | Control | Type | Description |
|---|---|---|---|
| CR-01 | Encryption in Transit | Preventive | Protects data moving between endpoints using strong transport encryption. |
| CR-02 | Encryption at Rest | Preventive | Encrypts stored data so that media compromise does not disclose plaintext. |
| CR-03 | Centralized Secrets Management | Preventive | Stores and distributes secrets through a governed, access-controlled system. |
| CR-04 | Key Rotation | Corrective | Replaces cryptographic keys on a schedule and on suspected compromise. |
| CR-05 | Certificate Lifecycle Management | Preventive | Issues, renews, and revokes certificates before expiry causes exposure or outage. |
| CR-06 | Secret Exposure Detection | Detective | Scans code, images, and logs for leaked secrets and credentials. |

## Network Controls

| ID | Control | Type | Description |
|---|---|---|---|
| NW-01 | Network Segmentation | Preventive | Divides the network into isolated zones to contain lateral movement. |
| NW-02 | Default-Deny Firewalling | Preventive | Permits only explicitly allowed traffic between zones and services. |
| NW-03 | Mutual TLS Between Services | Preventive | Authenticates both parties on internal service-to-service connections. |
| NW-04 | Intrusion Detection | Detective | Monitors network traffic for signatures and anomalies indicating attack. |
| NW-05 | Distributed Denial-of-Service Protection | Corrective | Absorbs and filters volumetric attacks to preserve availability. |

## Application Controls

| ID | Control | Type | Description |
|---|---|---|---|
| AP-01 | Input Validation | Preventive | Rejects malformed or malicious input at trust boundaries. |
| AP-02 | Output Encoding | Preventive | Encodes output in context to prevent injection and cross-site scripting. |
| AP-03 | Secure Software Development Lifecycle | Preventive | Embeds threat modeling, review, and testing into delivery. |
| AP-04 | Dependency Vulnerability Scanning | Detective | Identifies known vulnerabilities in third-party components. |
| AP-05 | Web Application Firewall | Preventive | Filters application-layer requests against known attack patterns. |
| AP-06 | Rate Limiting | Preventive | Constrains request volume per subject to resist abuse and brute force. |

## Data Controls

| ID | Control | Type | Description |
|---|---|---|---|
| DA-01 | Data Classification | Preventive | Labels data by sensitivity to drive proportionate handling. |
| DA-02 | Data Loss Prevention | Detective | Detects and blocks unauthorized exfiltration of sensitive data. |
| DA-03 | Tokenization and Masking | Preventive | Replaces or obscures sensitive fields where full values are unnecessary. |
| DA-04 | Backup and Restore | Corrective | Maintains recoverable copies to restore integrity after loss or tampering. |
| DA-05 | Data Retention and Disposal | Preventive | Retains data only as long as required and disposes of it securely. |

## Endpoint and Session Controls

| ID | Control | Type | Description |
|---|---|---|---|
| EP-01 | Endpoint Hardening | Preventive | Applies secure baselines and removes unnecessary services from devices. |
| EP-02 | Endpoint Detection and Response | Detective | Monitors endpoints for malicious behavior and enables containment. |
| EP-03 | Session Timeout and Revocation | Corrective | Ends idle or compromised sessions and invalidates their tokens. |
| EP-04 | Device Trust Verification | Preventive | Requires device posture checks before granting access. |

## Threat Detection and Response Controls

| ID | Control | Type | Description |
|---|---|---|---|
| TD-01 | Centralized Audit Logging | Detective | Records security-relevant events to a tamper-evident store. |
| TD-02 | Security Information and Event Management | Detective | Correlates events across sources to surface incidents. |
| TD-03 | Threat Intelligence Enrichment | Detective | Augments alerts with indicators of compromise and actor context. |
| TD-04 | Incident Response Playbooks | Corrective | Provides prepared, repeatable procedures to contain and recover. |
| TD-05 | Automated Alerting | Detective | Notifies responders when defined thresholds or patterns are met. |

## Governance Controls

| ID | Control | Type | Description |
|---|---|---|---|
| GV-01 | Security Policy Framework | Preventive | Establishes the mandatory rules that govern security behavior. |
| GV-02 | Risk Assessment | Detective | Identifies, analyzes, and prioritizes security risks. |
| GV-03 | Third-Party Risk Management | Preventive | Assesses and monitors the security posture of vendors and partners. |
| GV-04 | Compliance Monitoring | Detective | Verifies ongoing conformance to applicable standards and obligations. |
| GV-05 | Security Awareness Training | Preventive | Educates people to recognize and resist social-engineering and misuse. |

## Cross-References

- [Security Philosophy](/docs/blueprint/volume-12-security/section-a-security-foundations/01-security-philosophy.md)
- [Threat Model Template](/docs/blueprint/volume-12-security/appendices/threat-model-template.md)
- [Compliance Matrix](/docs/blueprint/volume-12-security/appendices/compliance-matrix.md)

## References

- [Volume 01 - Vision and Philosophy](/docs/blueprint/volume-01-vision-and-philosophy/README.md)
- [Document Standards](/docs/governance/document-standards.md)

## Change Log

| Version | Date | Author | Notes |
|---|---|---|---|
| 1.0 | 2026-07-12 | Lead Software Engineer | Initial approved version. |
