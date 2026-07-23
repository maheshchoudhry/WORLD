# 🌍 Project WORLD

> **WORLD** is an **AI-Native Business Operating System** — an intelligent **AI Business Partner** built to help founders think better, decide better, execute faster, and continuously improve their businesses.
>
> **WORLD is NOT** an ERP, a CRM, an Accounting Software, or a Chatbot. **WORLD is an AI Business Partner.**

## Repository Purpose
This repository is the **single source of truth** for Project WORLD. All knowledge — governance, architecture, specifications, and implementation — lives here and is documented. Documentation precedes implementation.

## Master Blueprint
Development follows the frozen [Master Blueprint](/docs/blueprint/README.md): 26 volumes across five parts, built in approved order.

- [Volume 01 - Vision & Philosophy](/docs/blueprint/volume-01-vision-and-philosophy/README.md) — Completed
- [Volume 02 - Business Foundation](/docs/blueprint/volume-02-business-foundation/README.md) — Completed
- [Volume 03 - AI Business Partner](/docs/blueprint/volume-03-ai-business-partner/README.md) — Completed
- [Volume 04 - Business Intelligence & Decision Science](/docs/blueprint/volume-04-business-intelligence-and-decision-science/README.md) — Completed
- [Volume 05 - ERP Foundation](/docs/blueprint/volume-05-erp-foundation/README.md) — Completed
- [Volume 06 - Business Modules](/docs/blueprint/volume-06-business-modules/README.md) — Completed
- [Volume 07 - Industry Solutions](/docs/blueprint/volume-07-industry-solutions/README.md) — Completed
- [Volume 08 - Architecture](/docs/blueprint/volume-08-architecture/README.md) — Completed
- [Volume 09 - Database](/docs/blueprint/volume-09-database/README.md) — Completed
- [Volume 10 - API](/docs/blueprint/volume-10-api/README.md) — Completed
- [Volume 11 - Infrastructure](/docs/blueprint/volume-11-infrastructure/README.md) — Completed
- [Volume 12 - Security](/docs/blueprint/volume-12-security/README.md) — Completed
- [Volume 13 - AI Agents](/docs/blueprint/volume-13-ai-agents/README.md) — Completed
- [Volume 14 - Knowledge Engine](/docs/blueprint/volume-14-knowledge-engine/README.md) — Completed

_Parts A and B complete. Part C - Technology in progress (Volumes 08-14 complete)._

## Repository Structure
```
WORLD/
├── docs/              # Documentation framework (source of truth)
│   ├── blueprint/     # Master Blueprint volumes
│   ├── governance/    # Standards, policies, glossary, templates
│   ├── business/      # Vision, business model, product definition
│   ├── ai/            # AI product & behavior specifications
│   ├── architecture/  # System architecture & decision records
│   ├── engineering/   # Engineering standards & practices
│   ├── security/      # Security architecture & policies
│   ├── database/      # Data models, schemas, migrations
│   ├── api/           # API specifications & contracts
│   ├── ui-ux/         # Design system & user flows
│   ├── roadmap/       # Product & engineering roadmap
│   ├── research/      # Research notes & experiments
│   └── assets/        # Static assets referenced by docs
├── platform/          # Application platform code
├── ai/                # AI system implementation
├── security/          # Security tooling & policy-as-code
├── infrastructure/    # IaC, environments, deployment
├── scripts/           # Automation scripts
├── tools/             # Developer tooling
├── tests/             # Cross-cutting test suites
├── .github/           # GitHub configuration & templates
├── README.md
├── CHANGELOG.md
└── CONTRIBUTING.md
```

## Documentation Overview
All documentation lives under [`docs/`](/docs/README.md) and follows a consistent, scalable framework. Every section contains a `README.md` (overview) and an `index.md` (document index table). Every document is authored from the master [document template](/docs/governance/document-template.md) and conforms to the standards defined in [governance](/docs/governance/README.md).

## Folder Navigation
| Section | Path |
|---|---|
| Master Blueprint | [`docs/blueprint/`](/docs/blueprint/README.md) |
| Documentation Hub | [`docs/`](/docs/README.md) |
| Governance | [`docs/governance/`](/docs/governance/README.md) |
| Business | [`docs/business/`](/docs/business/README.md) |
| AI | [`docs/ai/`](/docs/ai/README.md) |
| Architecture | [`docs/architecture/`](/docs/architecture/README.md) |
| Engineering | [`docs/engineering/`](/docs/engineering/README.md) |
| Security | [`docs/security/`](/docs/security/README.md) |
| Database | [`docs/database/`](/docs/database/README.md) |
| API | [`docs/api/`](/docs/api/README.md) |
| UI/UX | [`docs/ui-ux/`](/docs/ui-ux/README.md) |
| Roadmap | [`docs/roadmap/`](/docs/roadmap/README.md) |
| Research | [`docs/research/`](/docs/research/README.md) |
| Assets | [`docs/assets/`](/docs/assets/README.md) |

## Related
- [CONTRIBUTING.md](/CONTRIBUTING.md)
- [CHANGELOG.md](/CHANGELOG.md)
