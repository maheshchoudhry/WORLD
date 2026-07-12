# Contributing to Project WORLD

| Field | Value |
|---|---|
| Document ID | WORLD-CONTRIB |
| Title | Contribution Guidelines & Documentation Standards |
| Version | 0.1.0 |
| Status | Draft |
| Owner | Mahesh Choudhary (Founder) |
| Author | Lead Software Engineer |
| Last Updated | 2026-07-12 |

## Purpose
Define how contributions are made to WORLD and the mandatory documentation standards that govern the repository.

## Scope
All contributors, all directories, all documents and code.

## Source of Truth
The repository is the single source of truth. Every change must exist in the repository and be documented. Never rely on conversation history.

## Documentation Standards (Mandatory)
Every document is professional Markdown and MUST include the metadata block:

- Document ID
- Title
- Version
- Status
- Owner
- Author
- Last Updated
- Purpose
- Scope
- References
- Change Log

Documentation is mandatory **before** implementation. Every implementation references its specification.

## Engineering Principles
Clean, modular, documented, testable code. Follow SOLID. Never duplicate logic. Never hardcode secrets. Never bypass security or documentation.

## Commit & PR Workflow
1. Document the change (spec/ADR) before coding.
2. Use clear, conventional commit messages.
3. Open a Pull Request using [`.github/pull_request_template.md`](/.github/pull_request_template.md).
4. Update `CHANGELOG.md`, indexes, and cross-references.

## Pre-Commit Quality Checklist
Folder structure · Naming consistency · Broken links · Document references · Architecture consistency · Code quality · Security · Testing · Version numbers.

## References
- [README.md](/README.md)
- [CHANGELOG.md](/CHANGELOG.md)

## Change Log
| Version | Date | Author | Change |
|---|---|---|---|
| 0.1.0 | 2026-07-12 | Lead Software Engineer | Initial contribution guidelines and documentation standards. |
