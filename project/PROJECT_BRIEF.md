# Project Brief

## Engagement Details

| Field | Detail |
|---|---|
| Project ID | MTL-XF-011 |
| Project Title | Public Procurement Spend, Supplier Concentration & Contract Risk Intelligence |
| Client | Confidential Public Sector Commercial & Procurement Directorate |
| Sector | Public Sector / Commercial / Procurement |
| Duration | 8 weeks |
| Recommended Team Size | 6–8 |
| Primary Sponsor | Commercial Director |
| Senior Stakeholders | Head of Procurement, Category Management Lead, Commercial Finance Lead, Supplier Management Lead, Data Governance Lead, Data & Analytics Lead |
| Primary Dataset | Contracts Finder notices — June 2026 flattened OCDS CSV releases |

## 1. Client Situation

The directorate publishes and manages a large volume of procurement activity, but commercial leaders do not have one governed view of supplier concentration, repeated awards, fragmented buying, contract timing and SME participation. Existing reports are notice-centric rather than decision-centric, so teams cannot consistently distinguish genuine commercial exposure from simple high-volume activity.

## 2. Business Decision

The team has been commissioned to provide evidence for this decision:

> **Which suppliers, categories and contract groups should commercial leadership investigate first for concentration exposure, upcoming re-procurement pressure, fragmented demand or weak SME participation?**

The project succeeds only if the final solution helps stakeholders make or structure this decision; producing charts without a decision framework is insufficient.

## 3. Agreed Objectives

1. Create a trusted procurement analytical layer from the daily flattened OCDS files.
2. Define governed supplier, buyer, value, date, procedure and SME fields and document data-quality limitations.
3. Measure supplier concentration, repeated awards, category/buyer fragmentation and contract timing without double counting notices.
4. Build an interpretable commercial-prioritisation framework that distinguishes analytical flags from supplier-risk conclusions.
5. Provide a decision-support product that allows commercial leaders to drill from portfolio indicators to the underlying notices.

## 4. Key Business Questions

1. Which suppliers account for the greatest share of awarded value and award count within the selected cohort?
2. Which buyers/categories show repeated low-value or fragmented purchasing that may warrant consolidation review?
3. Which awards/notices create the greatest upcoming expiry or re-procurement workload based on available dates?
4. How does SME participation vary by value band, buyer and category where the source supports it?
5. Which duplicate, amended or incomplete notices could distort supplier/value measures?
6. Which commercial indicators are sufficiently reliable for routine monitoring and which require manual investigation?

## 5. Cross-Functional Delivery Model

| Role | Minimum expected output |
|---|---|
| Business Analyst | Produce stakeholder map, as-is/to-be decision process, requirements catalogue, user stories and acceptance criteria. |
| Data Governance Analyst | Produce procurement glossary, critical data-element register, ownership/stewardship matrix, DQ rules and lineage. |
| Data Engineer | Build repeatable ingestion/standardisation of daily OCDS CSVs and an auditable supplier-award analytical model. |
| Commercial/Data Analyst | Own concentration, fragmentation, SME and timing analysis plus interpretation. |
| BI Developer | Build governed semantic measures and the commercial portfolio dashboard. |
| Data Quality / Assurance Analyst | Own reconciliation, duplicate/amendment tests, UAT evidence and release QA. |

Responsibilities may be combined in a smaller team, but ownership and evidence must remain explicit.

## 6. Minimum Delivery Standard

The team must demonstrate:

- traceable requirements from stakeholder need to delivered feature/KPI;
- documented governance for critical fields and measures;
- preserved raw source data and reproducible transformations;
- explicit data-quality tests and reconciliation;
- analytical outputs that answer the commissioned questions;
- transparent decision/prioritisation logic;
- a stakeholder-facing product built from approved metrics;
- assurance/UAT evidence;
- technical and operational handover;
- GitHub evidence of genuine multidisciplinary collaboration.

## 7. Constraints and Interpretation Rules

- Contracts Finder notices are administrative procurement records and do not prove supplier financial distress, delivery failure or poor value for money.
- Notice status, amendment history and duplicate/replacement records must be assessed before aggregation.
- Contract values may contain ranges, missing values or inconsistent units/structures that require documented rules.
- Supplier names may require standardisation; entity resolution must not silently merge distinct suppliers.
- Recommendations must be framed as commercial review priorities, not allegations of supplier risk.

## 8. Agreed Success Criteria

The detailed acceptance tests are in `ACCEPTANCE_CRITERIA.md`. At minimum:

- All June 2026 source files used are listed with filename, source URL, acquisition date and record count.
- A documented rule prevents duplicate/amended notices from being double counted in core metrics.
- At least 95% of records entering the curated award/notices table reconcile to an explicit included/excluded/error category.
- Supplier concentration metrics can be reproduced from code and trace back to source fields.
- Every executive KPI has definition, grain, owner, calculation, exclusions and limitation in the KPI catalogue.
- The prioritisation framework uses documented factors and does not label suppliers as financially or operationally risky without evidence.

## 9. Out of Scope

Unless explicitly justified as an extension, the core engagement does not require:

- paid production infrastructure;
- confidential client data;
- automated operational decisions;
- unsupported causal inference;
- a production-grade public application.

## 10. Final Review

The Mettelo review panel may challenge source handling, definitions, reconciliation, analytical methods, thresholds, usability, governance, recommendations and whether the evidence actually supports the commissioned decision.

### Reproducibility definition

A reviewer should be able to clone the team repository, obtain the documented approved source data, execute the documented workflow and reproduce the curated analytical outputs and validation evidence without undocumented manual changes.
