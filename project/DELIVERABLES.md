# Required Deliverables

Every team repository must contain evidence for all deliverables below. A deliverable is complete only when its minimum contents and acceptance checks are satisfied.

## D1 — Discovery, Decision & Requirements Pack
**Due:** End of Week 1  
**Location:** `docs/01-discovery/`

Required:
- agreed problem statement and decision statement;
- stakeholder map and RACI/ownership view;
- as-is decision/reporting process;
- to-be decision process;
- at least 8 prioritised functional/user requirements;
- non-functional requirements covering reproducibility, usability and data quality;
- assumptions, dependencies and out-of-scope list;
- acceptance criteria mapped to requirements.

**Acceptance:** every dashboard/analytical feature planned for delivery must map to at least one approved requirement.

## D2 — Data Governance & Source Control Pack
**Due:** End of Week 2  
**Location:** `docs/02-data-governance/`, `data/SOURCE_REGISTER.md`

Required:
- source inventory and frozen-version details;
- business glossary;
- critical data-element register;
- owner/steward assumption for each critical element;
- source-to-target lineage;
- data-quality rule catalogue;
- access/reuse/licensing notes;
- known governance risks.

**Acceptance:** each headline KPI must trace to governed source fields and an approved definition.

## D3 — Reproducible Ingestion & Analytical Model
**Due:** End of Week 3  
**Location:** `src/`, `sql/`, `docs/03-data-model/`

Required:
- documented acquisition/load process;
- raw-data preservation;
- schema/type validation;
- standardisation logic;
- documented grain and keys;
- curated analytical table(s);
- rerunnable execution instructions;
- error/exception handling.

**Acceptance:** a clean rerun produces the same record-level/aggregate outputs from the same frozen input.

## D4 — Data Quality, Reconciliation & Exceptions
**Due:** End of Week 3  
**Location:** `docs/04-data-quality/`, `tests/` where used

Required:
- row-count reconciliation;
- duplicate assessment;
- key uniqueness/referential checks where applicable;
- missingness profile for critical fields;
- accepted-value/range checks;
- exception log;
- documented inclusion/exclusion rules.

**Acceptance:** every material record loss or exclusion is quantified and explained.

## D5 — KPI & Metric Catalogue
**Due:** End of Week 4  
**Location:** `docs/05-kpi-catalogue/`

Minimum metric set:
- total awarded value with documented value rule;
- award/notices count;
- unique suppliers;
- supplier share of awarded value;
- top-5/top-10 supplier concentration;
- buyer/category concentration;
- SME award share where supported;
- awards/notices with missing/invalid value;
- contracts/notices approaching selected review horizon;
- repeat supplier/buyer/category activity;

Each metric must contain: business purpose, definition, formula, grain, source fields, filters/exclusions, owner, refresh expectation and limitation.

## D6 — Core Analytical Assessment I
**Due:** End of Week 5  
**Location:** `analysis/`, `docs/06-analysis/`

Required:
- supplier concentration by value and count;
- top supplier dependence by buyer/category;
- sensitivity of concentration to missing/invalid values;
- supplier-name standardisation exceptions;

For every major finding include the supporting measure, comparison basis, materiality and limitation.

## D7 — Core Analytical Assessment II & Decision Framework
**Due:** End of Week 6  
**Location:** `docs/07-decision-framework/`

Required:
- fragmented purchasing patterns;
- contract/re-procurement timing profile;
- SME participation patterns;
- priority-review segmentation with explicit rationale;

Also provide:
- explicit prioritisation factors;
- threshold/rule rationale;
- sensitivity test for at least one important threshold or assumption;
- evidence that should trigger manual review;
- evidence that is insufficient for action.

## D8 — BI / Decision-Support Product
**Due:** Draft Week 6; final Week 7  
**Location:** `dashboard/`

Required:
- executive summary view;
- diagnostic/drill-down view;
- data-quality/definition information accessible to users;
- governed measures only;
- clear filter/reset behaviour;
- visible reporting period/source version;
- accessibility/readability considerations;
- link or reproducible build instructions.

**Acceptance:** at least five agreed headline measures reconcile to the curated analytical model.

## D9 — Assurance & User Acceptance Testing
**Due:** Week 7  
**Location:** `docs/08-assurance-uat/`

Required:
- minimum 10 test scenarios covering calculations, filters, edge cases and user journeys;
- reconciliation evidence;
- defect/issue log;
- requirement-to-test traceability;
- UAT feedback and disposition;
- final acceptance status.

## D10 — Technical & Operational Handover
**Due:** Week 8  
**Location:** `docs/09-technical-handover/`

Required:
- prerequisites/setup;
- end-to-end run instructions;
- data refresh/update process;
- architecture/data-flow diagram;
- transformation and metric logic;
- test commands/checks;
- troubleshooting;
- known limitations;
- maintenance/change recommendations.

## D11 — Executive Briefing & Demo-Day Presentation
**Due:** Week 8  
**Location:** `deliverables/executive-briefing/`, `deliverables/presentation/`

Executive briefing: maximum two pages or equivalent.  
Presentation: 15–20 minutes plus Q&A.

Both must state:
- commissioned decision;
- strongest evidence;
- recommended action/investigation;
- material limitations;
- next steps.

## D12 — Contribution & Delivery Evidence
**Due:** Final submission  
**Location:** `CONTRIBUTIONS.md` and GitHub history

For each member:
- role;
- owned work packages;
- principal artefacts;
- linked issues/PRs/commits;
- review/assurance contribution;
- presentation contribution.

Commit count alone is not evidence of capability.
