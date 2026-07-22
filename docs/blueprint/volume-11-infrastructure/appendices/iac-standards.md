# Volume 11 - IaC Standards

| Field | Value |
|---|---|
| Document ID | WORLD-VOL11-A5 |
| Title | IaC Standards |
| Version | 1.0 |
| Status | Approved |
| Classification | Internal |
| Founder | Mahesh Choudhary |

## Purpose

This appendix defines the standards that govern how Project WORLD authors, structures, and operates Infrastructure as Code (IaC). Its purpose is to make infrastructure reproducible, reviewable, and safe to change: infrastructure that is defined in versioned code can be reasoned about, peer-reviewed, tested, and rolled back like any other software. These standards are deliberately tool-neutral and criteria-based, so they hold regardless of which IaC tooling a given workload adopts.

## Scope

The standards cover module structure, state management, naming, tagging, review and promotion, and drift detection for all infrastructure managed as code in WORLD. They apply to every environment defined in the Environment Matrix (Appendix A3). They express required criteria and outcomes rather than mandating a specific product or syntax. Manual, out-of-band changes to managed infrastructure are prohibited except through the documented break-glass procedure, which itself must be reconciled back into code.

## Module Structure

| Standard | Requirement |
|---|---|
| Single Responsibility | Each module manages one coherent capability and exposes a narrow, documented interface. |
| Composability | Modules are composed from smaller modules; large monolithic definitions are not permitted. |
| Explicit Inputs and Outputs | Every input is typed and documented; every consumed output is declared, not implied. |
| No Hardcoded Values | Environment-specific values are passed as inputs, never embedded in the module body. |
| Versioned and Pinned | Modules and their providers are versioned and pinned to explicit, reviewed versions. |
| Documented | Each module ships a description of purpose, inputs, outputs, and example usage. |

## State Management

| Standard | Requirement |
|---|---|
| Remote and Shared | State is stored in a durable, remote backend, never on a local workstation. |
| Locked | State access is locked during operations to prevent concurrent, conflicting changes. |
| Encrypted | State is encrypted at rest and in transit, as it may contain sensitive values. |
| Segmented | State is partitioned by environment and by blast radius, not held in one global file. |
| Access-Controlled | State read and write access follows least privilege and is audited. |
| Recoverable | State is versioned and backed up so a corrupted or lost state can be restored. |

## Naming Standards

| Standard | Requirement |
|---|---|
| Consistent Convention | Resources follow one documented naming convention across all workloads. |
| Environment-Qualified | Names encode the environment so resources are unambiguous at a glance. |
| Human-Readable | Names are descriptive and predictable, avoiding opaque abbreviations. |
| Collision-Safe | Naming guarantees global uniqueness where the platform requires it. |
| Stable | Names are stable across changes; renaming that forces resource replacement is avoided. |

## Tagging Standards

| Tag | Purpose | Requirement |
|---|---|---|
| owner | Accountable team or individual. | Mandatory on every resource. |
| environment | The environment the resource belongs to. | Mandatory; drawn from the canonical environment names. |
| service | The workload or service the resource supports. | Mandatory. |
| cost-center | Financial allocation for FinOps reporting. | Mandatory. |
| data-classification | Sensitivity of any data handled. | Mandatory where data is stored or processed. |
| managed-by | The IaC system that owns the resource. | Mandatory to distinguish managed from manual resources. |

## Review and Promotion

| Standard | Requirement |
|---|---|
| Version Controlled | All IaC lives in version control; no infrastructure change bypasses it. |
| Peer Reviewed | Every change is reviewed by at least one qualified engineer before merge. |
| Plan Before Apply | The proposed change plan is generated and reviewed before it is applied. |
| Automated Checks | Linting, policy-as-code, and security scans run in the pipeline and must pass. |
| Progressive Promotion | Changes flow through non-production environments before Production, mirroring the app path. |
| Auditable | Who changed what, when, and why is recorded and retrievable. |

## Drift Detection

| Standard | Requirement |
|---|---|
| Continuous Detection | Managed infrastructure is periodically compared against declared state. |
| Alert on Drift | Detected drift raises a notification to the owning team. |
| Reconcile, Not Patch | Drift is resolved by updating code and reapplying, not by manual edits. |
| Break-Glass Reconciliation | Emergency manual changes are reconciled back into code within a defined window. |
| No Silent Divergence | Persistent, unexplained drift is treated as an operational defect. |

## Cross-References

- [Configuration Management](/docs/blueprint/volume-11-infrastructure/section-d-storage-and-configuration/14-configuration-management.md)
- [CD Infrastructure](/docs/blueprint/volume-11-infrastructure/section-f-cicd-and-resilience/20-cd-infrastructure.md)
- [Infrastructure Terminology](/docs/blueprint/volume-11-infrastructure/appendices/infrastructure-terminology.md)

## References

- [Volume 01 - Vision and Philosophy](/docs/blueprint/volume-01-vision-and-philosophy/README.md)
- [Document Standards](/docs/governance/document-standards.md)

## Change Log

| Version | Date | Author | Notes |
|---|---|---|---|
| 1.0 | 2026-07-12 | Lead Software Engineer | Initial approved version. |
