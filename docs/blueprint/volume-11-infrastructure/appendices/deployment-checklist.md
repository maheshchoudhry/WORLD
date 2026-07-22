# Volume 11 - Deployment Checklist

| Field | Value |
|---|---|
| Document ID | WORLD-VOL11-A6 |
| Title | Deployment Checklist |
| Version | 1.0 |
| Status | Approved |
| Classification | Internal |
| Founder | Mahesh Choudhary |

## Purpose

This appendix provides the canonical checklists that govern every Project WORLD deployment to Production. Its purpose is to make releases safe and boring: a deployment that follows a disciplined, verifiable checklist is far less likely to cause an incident than one that relies on memory. The checklists turn the implicit knowledge of experienced release engineers into an explicit, auditable sequence that anyone on the team can follow with confidence.

## Scope

The checklists cover the four phases of a release: pre-deployment preparation, the deployment itself, post-deployment verification, and rollback. They apply to Production deployments and, in reduced form, to Staging. They complement the Runbook Templates (Appendix A4) by providing the concrete tick-list an operator works through, whereas the runbooks provide the procedural narrative. Each item is expressed as a verifiable check; a deployment does not proceed while any mandatory item in the current phase is unmet.

## Pre-Deployment Checklist

- [ ] Release version is tagged, immutable, and traceable to a merge.
- [ ] All required approvals and the change record are in place.
- [ ] The change has passed all pipeline gates in Staging.
- [ ] Staging validation and acceptance tests are green.
- [ ] No active change freeze applies to the target window.
- [ ] The target environment is healthy and within SLOs.
- [ ] A current backup or restore point exists and is verified.
- [ ] Database migrations are reviewed and are backward-compatible.
- [ ] A rollback plan is documented and the prior version is identified.
- [ ] On-call is aware and available for the deployment window.
- [ ] Stakeholders are notified of the planned window.
- [ ] Feature flags for the release are configured to a safe default.

## Deployment Checklist

- [ ] Deployment is executed through the pipeline, not manually.
- [ ] The deployment window is announced as started.
- [ ] Progressive rollout (canary or blue-green) is used, not a big-bang cutover.
- [ ] Canary health signals are observed before widening traffic.
- [ ] Error rates, latency, and saturation are watched live.
- [ ] Smoke tests pass against the newly deployed version.
- [ ] Key SLOs remain within target during rollout.
- [ ] Full traffic promotion occurs only after the canary is healthy.
- [ ] Any schema migration completed successfully and reversibly.

## Post-Deployment Checklist

- [ ] Health checks are green across all instances.
- [ ] Dashboards show metrics within normal ranges.
- [ ] No new or elevated alerts are firing.
- [ ] Logs show no unexpected error patterns.
- [ ] A critical-path business transaction is verified end to end.
- [ ] The deployment is recorded with version, time, and operator.
- [ ] Stakeholders are notified that the deployment is complete.
- [ ] A heightened-observation period is observed before closing the window.
- [ ] Temporary deployment resources are cleaned up.

## Rollback Checklist

- [ ] The decision to roll back is declared and communicated.
- [ ] Any in-progress rollout is halted immediately.
- [ ] The last known-good version and artifact are identified.
- [ ] Rollback is executed through the pipeline.
- [ ] Configuration is reconciled to the prior version.
- [ ] Reversible migrations are reversed per the documented plan.
- [ ] Health checks and SLOs return to normal.
- [ ] Consumer-facing behavior is confirmed restored.
- [ ] The rollback is recorded and linked to the originating change.
- [ ] A follow-up is raised to root-cause the failure.

## Cross-References

- [Deployment Strategy](/docs/blueprint/volume-11-infrastructure/section-a-cloud-and-deployment/02-deployment-strategy.md)
- [Runbook Templates](/docs/blueprint/volume-11-infrastructure/appendices/runbook-templates.md)
- [Environment Matrix](/docs/blueprint/volume-11-infrastructure/appendices/environment-matrix.md)

## References

- [Volume 01 - Vision and Philosophy](/docs/blueprint/volume-01-vision-and-philosophy/README.md)
- [Document Standards](/docs/governance/document-standards.md)

## Change Log

| Version | Date | Author | Notes |
|---|---|---|---|
| 1.0 | 2026-07-12 | Lead Software Engineer | Initial approved version. |
