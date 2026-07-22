# Volume 11 - Infrastructure Terminology

| Field | Value |
|---|---|
| Document ID | WORLD-VOL11-A2 |
| Title | Infrastructure Terminology |
| Version | 1.0 |
| Status | Approved |
| Classification | Internal |
| Founder | Mahesh Choudhary |

## Purpose

This appendix defines the controlled vocabulary for Project WORLD's infrastructure tier. Where the Glossary (Appendix A1) explains what terms mean, this document fixes which terms are canonical, how they must be used, and which synonyms must be avoided. Its purpose is consistency across chapters, runbooks, IaC modules, dashboards, and operational documentation, so that one concept is always named one way. Controlled terminology reduces cognitive load during incidents, when precision and speed matter most, and prevents costly misunderstanding between teams.

## Scope

The controlled vocabulary covers the naming of core infrastructure concepts, environments, actors, artifacts, and operations used throughout Volume 11. It applies to prose, diagrams, IaC resource names, tags, and operational tooling. It does not govern business-domain nouns (owned by Volume 05), database object names (owned by Volume 09), or API contract terms (owned by Volume 10). Each entry gives the approved canonical term, its approved usage, and the terms to avoid. Deviations require review by the infrastructure governance function.

## Controlled Vocabulary

| Canonical Term | Approved Usage | Terms to Avoid |
|---|---|---|
| Environment | A named, isolated deployment context (Development, Testing, Staging, Production). | Stage, tier (when meaning environment), instance |
| Production | The live environment serving real users and data. | Prod (in formal docs), live, PRD |
| Non-Production | Any environment other than Production, collectively. | Lower environment, pre-prod (as a catch-all) |
| Workload | A deployable unit of application running on the infrastructure. | App instance, job (when a service is meant), process |
| Node | A machine (physical or virtual) providing cluster compute. | Box, server (in cluster context), host (when a node is meant) |
| Cluster | A managed group of nodes running orchestrated workloads. | Fleet, farm, pool (when a cluster is meant) |
| Container Image | The immutable, versioned build artifact. | Build, snapshot, container (when the image is meant) |
| Container | A running instance of a container image. | Image (when running is meant), pod (unless a pod is meant) |
| Deployment | The act and record of releasing a version to an environment. | Push, ship (as a noun), release (when the act is meant) |
| Release | A versioned, named collection of changes promoted through environments. | Deploy (when a version is meant), drop, cut |
| Rollback | Controlled reversion to a previous known-good version. | Revert (in ops context), downgrade, undeploy |
| Failover | Switching traffic from a failed component to a standby. | Cutover (when meaning failover), switchover (informal) |
| Incident | An unplanned disruption or degradation of service. | Outage (when partial), issue, ticket (as a synonym) |
| Runbook | A documented, repeatable operational procedure. | Playbook (when a runbook is meant), SOP, guide |
| Secret | Sensitive configuration handled through the secrets manager. | Password (generically), key (when a secret is meant), credential file |
| Configuration | Non-sensitive settings that vary by environment. | Config file (when the value set is meant), settings (loosely) |
| Infrastructure as Code | Versioned, declarative definitions of infrastructure. | Scripts (when IaC is meant), automation (loosely), templates |
| Provisioning | Creating and configuring resources via IaC. | Spinning up, standing up (in formal docs), building |
| Observability | The capability to infer state from metrics, logs, and traces. | Monitoring (when the broader capability is meant), telemetry (loosely) |
| Service Level Objective | An internal, measurable reliability target. | KPI (when an SLO is meant), goal, threshold |
| Recovery Time Objective | The target time to restore service after an incident. | Downtime budget, recovery window (loosely) |
| Recovery Point Objective | The target maximum data loss, expressed as time. | Backup window, data window (loosely) |

## Usage Principles

| Principle | Statement |
|---|---|
| One Concept, One Term | Each concept has exactly one canonical term; synonyms are not interchangeable in official artifacts. |
| Environment Names Are Fixed | The four environment names are canonical and are not abbreviated or renamed in formal documentation. |
| Image Versus Container | The immutable artifact is always the image; the running instance is always the container. |
| Incident Language Is Precise | During incidents, canonical terms are used verbatim to avoid ambiguity under time pressure. |
| Declarative First | Infrastructure is described by its desired state; imperative language is reserved for procedures. |

## Cross-References

- [Infrastructure Glossary](/docs/blueprint/volume-11-infrastructure/appendices/infrastructure-glossary.md)
- [Environment Strategy](/docs/blueprint/volume-11-infrastructure/section-h-environments-and-evolution/27-environment-strategy.md)
- [IaC Standards](/docs/blueprint/volume-11-infrastructure/appendices/iac-standards.md)

## References

- [Volume 01 - Vision and Philosophy](/docs/blueprint/volume-01-vision-and-philosophy/README.md)
- [Document Standards](/docs/governance/document-standards.md)

## Change Log

| Version | Date | Author | Notes |
|---|---|---|---|
| 1.0 | 2026-07-12 | Lead Software Engineer | Initial approved version. |
