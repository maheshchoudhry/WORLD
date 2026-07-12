# 🌍 Project WORLD

> **WORLD** is an **AI-Native Business Operating System** — an intelligent **AI Business Partner** built to help founders think better, decide better, execute faster, and continuously improve their businesses.

**WORLD is NOT** an ERP. **WORLD is NOT** a CRM. **WORLD is NOT** an Accounting Software. **WORLD is NOT** a Chatbot. **WORLD is an AI Business Partner.**

| Field | Value |
|---|---|
| Document ID | WORLD-README |
| Title | Project WORLD — Repository Overview |
| Version | 0.1.0 |
| Status | Draft |
| Owner | Mahesh Choudhary (Founder) |
| Author | Lead Software Engineer |
| Last Updated | 2026-07-12 |

## Purpose
This document is the single entry point and navigation index for the WORLD repository. The repository is the **single source of truth** for the project; all knowledge, architecture, and implementation live here and are documented.

## Scope
Repository-wide overview, structure, and navigation. Domain-specific details live in the linked directories.

## Repository Structure
```
WORLD/
├── docs/            # Documentation hub (source of truth)
│   ├── governance/  # Decision records, policies, standards
│   ├── business/    # Vision, business model, product definition
│   ├── ai/          # AI product & behavior specifications
│   ├── architecture/# System architecture & ADRs
│   ├── security/    # Security architecture & policy docs
│   ├── engineering/ # Engineering standards & practices
│   ├── database/    # Data models, schemas, migrations
│   ├── api/         # API specifications & contracts
│   ├── ui-ux/       # UI/UX design specs & flows
│   ├── roadmap/     # Product & engineering roadmap
│   └── research/    # Research notes & experiments
├── platform/        # Application platform code
│   ├── backend/
│   ├── frontend/
│   ├── mobile/
│   └── shared/
├── ai/              # AI system implementation
│   ├── agents/
│   ├── memory/
│   ├── reasoning/
│   ├── planning/
│   └── knowledge/
├── security/        # Security tooling & policy-as-code
├── infrastructure/  # IaC, environments, deployment
├── scripts/         # Automation scripts
├── tools/           # Developer tooling
├── tests/           # Cross-cutting test suites
├── .github/         # GitHub configuration & templates
├── README.md
├── CHANGELOG.md
└── CONTRIBUTING.md
```

## Navigation
- **Documentation Hub** → [`docs/`](/docs/README.md)
- **Platform Code** → [`platform/`](/platform/README.md)
- **AI System** → [`ai/`](/ai/README.md)
- **Security** → [`security/`](/security/README.md)
- **Infrastructure** → [`infrastructure/`](/infrastructure/README.md)
- **Contributing & Standards** → [`CONTRIBUTING.md`](/CONTRIBUTING.md)
- **Change History** → [`CHANGELOG.md`](/CHANGELOG.md)

## Engineering Principles
Clean, modular, documented, testable code. SOLID by default. No duplicated logic. No hardcoded secrets. No bypassing security or documentation. Documentation precedes implementation.

## Source of Truth
The GitHub repository is the single source of truth. Every change exists in the repository, is documented, and never relies on conversation history.

## References
- [CONTRIBUTING.md](/CONTRIBUTING.md)
- [CHANGELOG.md](/CHANGELOG.md)

## Change Log
| Version | Date | Author | Change |
|---|---|---|---|
| 0.1.0 | 2026-07-12 | Lead Software Engineer | Initial repository scaffold and overview. |
