# Volume 11 - Environment Matrix

| Field | Value |
|---|---|
| Document ID | WORLD-VOL11-A3 |
| Title | Environment Matrix |
| Version | 1.0 |
| Status | Approved |
| Classification | Internal |
| Founder | Mahesh Choudhary |

## Purpose

This appendix defines, in a single comparative matrix, how Project WORLD's four canonical environments differ across the dimensions that matter operationally. Its purpose is to make explicit what each environment is for, what guarantees it offers, and what constraints apply to it, so that engineers, reviewers, and operators share one reference when deciding where a change belongs and how it must be handled. A clear environment model is the backbone of safe, progressive delivery.

## Scope

The matrix compares the Development, Testing, Staging, and Production environments across purpose, scale, data, access, deploy trigger, monitoring, and service-level expectations. It applies to all WORLD workloads governed by Volume 11. It does not define the internal topology of any single environment (covered by Section H chapters) nor the promotion mechanics of the pipeline (covered by Section F). Where an individual workload requires a variance from this matrix, that variance must be recorded and approved by infrastructure governance.

## Environment Comparison Matrix

| Dimension | Development | Testing | Staging | Production |
|---|---|---|---|---|
| Purpose | Rapid iteration and local feature work by engineers. | Automated verification of correctness and integration. | Production-like validation before release. | Serving real users and business operations. |
| Scale | Minimal; single small instances, cost-optimized. | Small; sized for test suites and parallelism. | Production-shaped but reduced footprint. | Full, autoscaled to real demand. |
| Data | Synthetic or seeded fixtures only. | Synthetic and generated test datasets. | Anonymized or masked production-like data. | Real production data under full controls. |
| Access | Broad engineer access, self-service. | CI service accounts and engineers. | Restricted; release and QA roles. | Least-privilege; audited, break-glass only. |
| Deploy Trigger | On demand, per developer, frequent. | Automatic on every merge to mainline. | Automatic on release candidate promotion. | Gated, approved promotion from Staging. |
| Change Control | Informal; no approval required. | Automated gates (tests must pass). | Peer and QA sign-off required. | Formal approval and change record required. |
| Monitoring | Basic; local logs and lightweight metrics. | Test telemetry and coverage reporting. | Full observability, production-equivalent. | Full observability with on-call alerting. |
| Alerting | None or developer-only. | Pipeline failure notifications. | Non-paging alerts to the delivery team. | Paging alerts against SLOs, 24/7 on-call. |
| Availability Target | Best-effort; no SLA. | Best-effort; may be recreated at will. | High during release windows; no external SLA. | Formal SLA and published SLOs. |
| Backup and DR | None; environment is disposable. | None; datasets are regenerable. | Periodic; validates restore procedures. | Full backup, tested DR, defined RPO/RTO. |
| Network Exposure | Private or local only. | Private; internal reachability. | Private with controlled external test access. | Public via gateway and load balancers. |
| Cost Posture | Aggressively minimized; scale-to-zero. | Minimized; ephemeral where possible. | Moderate; balanced fidelity and cost. | Optimized for reliability first, then cost. |
| Lifespan | Ephemeral or per-engineer, short-lived. | Ephemeral per pipeline run where feasible. | Long-lived, continuously maintained. | Permanent, continuously operated. |

## Promotion Path

| Stage | From | To | Gate |
|---|---|---|---|
| Merge | Development | Testing | Automated build and unit tests pass. |
| Integrate | Testing | Staging | Integration and regression suites pass; release candidate cut. |
| Validate | Staging | Production | Peer, QA, and change approval; smoke and acceptance pass. |
| Recover | Production | Production (prior) | Rollback executed on SLO breach or failed deploy. |

## Cross-References

- [Environment Strategy](/docs/blueprint/volume-11-infrastructure/section-h-environments-and-evolution/27-environment-strategy.md)
- [Staging](/docs/blueprint/volume-11-infrastructure/section-h-environments-and-evolution/30-staging.md)
- [Production](/docs/blueprint/volume-11-infrastructure/section-h-environments-and-evolution/31-production.md)
- [Deployment Checklist](/docs/blueprint/volume-11-infrastructure/appendices/deployment-checklist.md)

## References

- [Volume 01 - Vision and Philosophy](/docs/blueprint/volume-01-vision-and-philosophy/README.md)
- [Document Standards](/docs/governance/document-standards.md)

## Change Log

| Version | Date | Author | Notes |
|---|---|---|---|
| 1.0 | 2026-07-12 | Lead Software Engineer | Initial approved version. |
