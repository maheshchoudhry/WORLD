# Volume 11 - Infrastructure Glossary

| Field | Value |
|---|---|
| Document ID | WORLD-VOL11-A1 |
| Title | Infrastructure Glossary |
| Version | 1.0 |
| Status | Approved |
| Classification | Internal |
| Founder | Mahesh Choudhary |

## Purpose

This appendix provides a single, authoritative glossary of the infrastructure terms used throughout Volume 11. Its purpose is to remove ambiguity: when a chapter, a runbook, or a design review uses a term such as *blast radius*, *immutable infrastructure*, or *recovery point objective*, this glossary fixes its meaning for Project WORLD. A shared vocabulary is a precondition for a coherent infrastructure tier, because cloud regions, containers, load balancers, pipelines, and observability signals can only be reasoned about together if their authors mean the same thing by the same word.

## Scope

The glossary defines infrastructure and operations terms that appear in Volume 11, Sections A through H, together with a small number of adjacent terms needed to make those definitions self-contained. Definitions are concise and platform-neutral. It does not redefine API terms (governed by Volume 10), database terms (governed by Volume 09), or architectural terms (governed by Volume 08), and it does not fix concrete technology or vendor choices. Where a term has a broader meaning in general usage, the definition given here is the WORLD-canonical one.

## Glossary

| Term | Definition |
|---|---|
| Autoscaling | The automatic adjustment of compute capacity up or down in response to observed load or a schedule. |
| Availability Zone | An isolated failure domain within a cloud region, with independent power, cooling, and networking. |
| Blast Radius | The scope of systems, users, or data affected when a given component or change fails. |
| Blue-Green Deployment | A release technique running two identical environments and switching traffic from old (blue) to new (green). |
| Canary Deployment | A release technique that exposes a new version to a small traffic slice before full rollout. |
| Chaos Engineering | The disciplined practice of injecting controlled failure to validate resilience assumptions. |
| Cold Standby | A recovery posture where standby capacity is provisioned only when a failover is required. |
| Configuration Drift | Divergence between the declared desired state and the actual running state of infrastructure. |
| Container | A lightweight, isolated, portable unit that packages an application with its runtime dependencies. |
| Container Image | An immutable, versioned artifact from which containers are instantiated. |
| Container Registry | A managed store that holds and distributes versioned container images. |
| Content Delivery Network (CDN) | A geographically distributed cache layer that serves content close to end users. |
| Control Plane | The management layer that schedules, configures, and reconciles workloads and infrastructure. |
| Data Plane | The layer that carries and processes actual application traffic and workloads. |
| Declarative Configuration | A specification of the desired end state, leaving the how of convergence to the tooling. |
| Disaster Recovery (DR) | The strategy and procedures to restore service after a major, region-level, or catastrophic failure. |
| DNS (Domain Name System) | The distributed system that resolves human-readable names to network addresses. |
| Edge Location | A point of presence near end users used for caching, termination, or routing. |
| Environment | A named, isolated deployment context such as Development, Testing, Staging, or Production. |
| Ephemeral Infrastructure | Short-lived resources created on demand and discarded rather than maintained in place. |
| Failover | The automatic or manual switch of traffic from a failed component to a healthy standby. |
| Golden Image | A pre-hardened, versioned base image used as the standard starting point for provisioning. |
| Health Check | A periodic probe that determines whether an instance or service is able to serve traffic. |
| High Availability (HA) | A design property that keeps a service operational despite the failure of individual components. |
| Horizontal Scaling | Adding or removing instances of a service to change capacity (scaling out or in). |
| Hot Standby | A recovery posture where standby capacity runs continuously, ready to take traffic immediately. |
| Immutable Infrastructure | An operating model where servers are replaced rather than modified in place. |
| Infrastructure as Code (IaC) | The management of infrastructure through versioned, machine-readable definition files. |
| Ingress | The controlled entry point governing external traffic into a cluster or network. |
| Kubernetes | An open-source platform for automating deployment, scaling, and operation of containerized workloads. |
| Load Balancer | A component that distributes incoming traffic across multiple healthy backend targets. |
| Log Aggregation | The collection, centralization, and indexing of logs from many sources for search and analysis. |
| Metric | A numeric measurement of a system property sampled over time, such as latency or utilization. |
| Namespace | A logical partition that scopes and isolates resources within a shared cluster or system. |
| Node | A physical or virtual machine that provides compute capacity to a cluster. |
| Object Storage | A storage model that manages data as discrete objects with metadata, addressed by key. |
| Observability | The degree to which internal system state can be inferred from external outputs (metrics, logs, traces). |
| Orchestration | The automated coordination of workloads, scheduling, scaling, and lifecycle across infrastructure. |
| Pod | The smallest deployable unit in Kubernetes, wrapping one or more tightly coupled containers. |
| Provisioning | The act of creating and configuring infrastructure resources so they are ready for use. |
| Recovery Point Objective (RPO) | The maximum acceptable amount of data loss, measured as time, after an incident. |
| Recovery Time Objective (RTO) | The maximum acceptable duration to restore a service after an incident. |
| Reverse Proxy | A server that fronts backend services to handle routing, termination, and traffic policy. |
| Rollback | The controlled reversion of a system to a previous known-good version or state. |
| Runbook | A documented, repeatable procedure for performing an operational task or handling an incident. |
| Secret | Sensitive configuration such as a credential, key, or token that must be stored and accessed securely. |
| Service Level Agreement (SLA) | A commitment to a consumer defining the expected level of service and consequences of breach. |
| Service Level Objective (SLO) | An internal target for a measurable aspect of service, such as availability or latency. |
| Service Mesh | An infrastructure layer that manages service-to-service traffic, security, and observability transparently. |
| Sidecar | A helper container deployed alongside a primary workload to extend or support it. |
| Span | A single timed operation within a distributed trace, representing one unit of work. |
| State (IaC) | The recorded mapping between declared IaC resources and the real provisioned resources they manage. |
| Tag | A key-value label attached to a resource for ownership, cost allocation, and lifecycle management. |
| Trace | An end-to-end record of a request as it propagates across services, composed of spans. |
| Vertical Scaling | Changing the capacity of a single instance by adding or removing resources (scaling up or down). |
| Virtual Private Cloud (VPC) | A logically isolated, private network segment provisioned within a cloud provider. |
| Warm Standby | A recovery posture where scaled-down standby capacity runs and is scaled up on failover. |

## Cross-References

- [Cloud Strategy](/docs/blueprint/volume-11-infrastructure/section-a-cloud-and-deployment/01-cloud-strategy.md)
- [Infrastructure Terminology](/docs/blueprint/volume-11-infrastructure/appendices/infrastructure-terminology.md)
- [Environment Matrix](/docs/blueprint/volume-11-infrastructure/appendices/environment-matrix.md)

## References

- [Volume 01 - Vision and Philosophy](/docs/blueprint/volume-01-vision-and-philosophy/README.md)
- [Document Standards](/docs/governance/document-standards.md)

## Change Log

| Version | Date | Author | Notes |
|---|---|---|---|
| 1.0 | 2026-07-12 | Lead Software Engineer | Initial approved version. |
