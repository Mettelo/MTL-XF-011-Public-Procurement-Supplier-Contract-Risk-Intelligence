# Project Brief

## 1. Business Problem

The commercial directorate manages a large volume of procurement activity across multiple buyers, categories and suppliers, but current reporting is fragmented across individual notices and spreadsheets. Leadership cannot easily see where public spend is concentrated, where the same supplier is repeatedly winning work, where low-value purchasing is fragmented across multiple awards, or where contracts may create upcoming re-procurement pressure.

This creates three practical risks. First, commercial teams may become overly dependent on a small number of suppliers without recognising the concentration early enough. Second, fragmented purchasing may prevent the organisation from identifying opportunities to consolidate demand or negotiate more effectively. Third, upcoming contract end dates and award timing may not be visible in one place, making forward procurement planning reactive rather than planned.

The problem is therefore not “analyse procurement data”. The problem is that commercial leaders currently lack one governed, reproducible view that turns procurement notices into an evidence base for supplier review, category planning and future procurement workload.

## What the Team Needs to Do

The team is expected to build a governed procurement-intelligence solution that converts the raw Contracts Finder notice files into a decision-ready supplier, buyer, category and contract view.

The work should include:
- defining the commercial questions and stakeholder requirements before building;
- documenting which notice, award, buyer, supplier, value, date and SME fields are trustworthy enough for analysis;
- creating reproducible ingestion and transformation logic;
- identifying amended, duplicated or incomplete notices before aggregation;
- standardising supplier/buyer fields without creating false matches;
- calculating supplier concentration, repeat-award and fragmented-purchasing measures;
- identifying upcoming procurement/re-procurement workload from available dates;
- analysing SME participation where the source supports it;
- creating a transparent commercial-review prioritisation framework;
- building a BI product that allows leaders to move from portfolio-level risk indicators to the underlying notices;
- reconciling headline measures back to the source and completing UAT/handover.

## Practical Use Case

The finished product should support a monthly or quarterly commercial portfolio review. A Commercial Director should be able to open the dashboard and ask, for example: “Which category is becoming too concentrated around a small number of suppliers?”, “Which buyers appear to be repeatedly purchasing similar services in separate awards?”, or “Which contracts should procurement teams begin planning to re-compete soon?”

The output is not intended to automatically label suppliers as risky. It is intended to identify where commercial managers should investigate, challenge or plan earlier.

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
