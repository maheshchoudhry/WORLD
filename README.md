# 🌍 Project WORLD

> **WORLD** is an **AI-Native Business Operating System** — an intelligent **AI Business Partner** built to help founders think better, decide better, execute faster, and continuously improve their businesses.
>
> **WORLD is NOT** an ERP, a CRM, an Accounting Software, or a Chatbot. **WORLD is an AI Business Partner.**

## Repository Purpose
This repository is the **single source of truth** for Project WORLD. All knowledge — governance, architecture, specifications, and implementation — lives here and is documented. Documentation precedes implementation.

## Master Blueprint
Development follows the frozen [Master Blueprint](/docs/blueprint/README.md): 26 volumes across five parts, built one volume at a time in approved order.

- [Volume 01 - Vision & Philosophy](/docs/blueprint/volume-01-vision-and-philosophy/README.md) — Completed

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
All documentation lives under [`docs/`](/docs/README.md) and follows a consistent, scalable framework designed to support thousands of future documents. Every section contains:

- **`README.md`** — purpose, scope, responsibilities, expected documents, and navigation.
- **`index.md`** — a document index table (Document ID, Title, Version, Status, Last Updated).

Every document is authored from the master [document template](/docs/governance/document-template.md) and conforms to the standards defined in [governance](/docs/governance/README.md).

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
