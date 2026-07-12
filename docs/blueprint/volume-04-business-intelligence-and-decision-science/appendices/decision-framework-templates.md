# Volume 04 - Decision Framework Templates

| Field | Value |
|---|---|
| Document ID | WORLD-VOL04-A1 |
| Title | Decision Framework Templates |
| Version | 1.0 |
| Status | Approved |
| Classification | Internal |
| Founder | Mahesh Choudhary |

## Purpose

This appendix provides reusable, ready-to-use decision framework templates for the WORLD AI Business Operating System. These templates standardize how the AI Business Partner and human operators frame, structure, and record decisions so that reasoning is transparent, comparable, and auditable across the organization.

## Scope

The templates apply to any material business decision surfaced within Volume 04 workflows: capital allocation, hiring, vendor selection, product prioritization, market entry, and operational trade-offs. Each template is fill-in-ready. Placeholders in angle brackets `<...>` are meant to be replaced with real values at use time.

## 1. Decision Brief

A one-page structured framing document that must accompany any decision above the materiality threshold.

| Section | Content |
|---|---|
| Decision ID | `<VOL04-DEC-YYYYMMDD-NN>` |
| Decision statement | A single sentence: "We must decide whether to `<action>` by `<date>`." |
| Decision owner | `<name / role>` |
| Decision type | Reversible (Type 2) / Irreversible (Type 1) |
| Context & trigger | Why this decision is needed now. |
| Objectives | What a good outcome achieves (linked to OKRs). |
| Options considered | Option A, Option B, Option C, Do-nothing baseline. |
| Key assumptions | Explicit assumptions with confidence level. |
| Constraints | Budget, time, regulatory, capacity. |
| Recommendation | Preferred option and rationale. |
| Decision deadline | `<date>` |
| Approvers | `<names / roles>` |

## 2. Weighted-Scoring / MCDA Matrix

Multi-Criteria Decision Analysis. Assign each criterion a weight (weights sum to 100%). Score each option 1-5 against each criterion. Weighted score = weight x raw score. The option with the highest total weighted score is favored.

| Criterion | Weight (%) | Option A (raw) | Option A (wtd) | Option B (raw) | Option B (wtd) | Option C (raw) | Option C (wtd) |
|---|---|---|---|---|---|---|---|
| Strategic fit | 25 | 4 | 1.00 | 3 | 0.75 | 5 | 1.25 |
| Financial return | 25 | 3 | 0.75 | 5 | 1.25 | 3 | 0.75 |
| Time to value | 15 | 5 | 0.75 | 3 | 0.45 | 2 | 0.30 |
| Risk / feasibility | 20 | 4 | 0.80 | 2 | 0.40 | 3 | 0.60 |
| Customer impact | 15 | 3 | 0.45 | 4 | 0.60 | 5 | 0.75 |
| **Total** | **100** | | **3.75** | | **3.45** | | **3.65** |

Scoring guide: 1 = poor, 2 = below average, 3 = adequate, 4 = strong, 5 = excellent.

## 3. Cost-Benefit Table

Quantify benefits and costs over a defined horizon. Express in a single currency and net them.

| Item | Type | Year 0 | Year 1 | Year 2 | Year 3 | Total |
|---|---|---|---|---|---|---|
| Implementation cost | Cost | (100,000) | 0 | 0 | 0 | (100,000) |
| Operating cost | Cost | 0 | (20,000) | (20,000) | (20,000) | (60,000) |
| Revenue uplift | Benefit | 0 | 60,000 | 90,000 | 110,000 | 260,000 |
| Cost savings | Benefit | 0 | 15,000 | 20,000 | 25,000 | 60,000 |
| **Net cash flow** | | **(100,000)** | **55,000** | **90,000** | **115,000** | **160,000** |

Complete with: payback period, NPV (see A3), and benefit-cost ratio (total benefits / total costs).

## 4. Risk-Reward Grid

Plot each option on a 2x2 by expected reward (value if successful) and risk (probability x impact of failure).

| | Low Risk | High Risk |
|---|---|---|
| **High Reward** | Prioritize (quick wins, strategic bets) | Evaluate carefully (big bets - stage-gate, pilot) |
| **Low Reward** | Fill-in / delegate | Avoid / reject |

Usage: place each option in a quadrant, then record the mitigation required to move a High-Risk/High-Reward option toward acceptability.

## 5. Go / No-Go Decision Template

A gate checklist. All "must" criteria must be met to proceed.

| # | Gate criterion | Type | Met? (Y/N) | Evidence / Note |
|---|---|---|---|---|
| 1 | Strategic alignment confirmed | Must | | |
| 2 | Positive NPV / acceptable ROI | Must | | |
| 3 | Funding available and approved | Must | | |
| 4 | Key risks identified and mitigated | Must | | |
| 5 | Capacity / resources secured | Should | | |
| 6 | Compliance / legal cleared | Must | | |
| 7 | Success metrics defined | Should | | |

**Decision:** GO / NO-GO / CONDITIONAL GO (conditions: `<...>`) - Owner: `<name>` - Date: `<date>`.

## Cross-References

- [Decision-Making Frameworks](/docs/blueprint/volume-04-business-intelligence-and-decision-science/README.md)
- [Analytical Models](/docs/blueprint/volume-04-business-intelligence-and-decision-science/appendices/analytical-models.md)
- [Executive Review Templates](/docs/blueprint/volume-04-business-intelligence-and-decision-science/appendices/executive-review-templates.md)

## References

- [Volume 01 - Vision and Philosophy](/docs/blueprint/volume-01-vision-and-philosophy/README.md)
- [Document Standards](/docs/governance/document-standards.md)

## Change Log

| Version | Date | Author | Notes |
|---|---|---|---|
| 1.0 | 2026-07-12 | Lead Software Engineer | Initial approved version. |
