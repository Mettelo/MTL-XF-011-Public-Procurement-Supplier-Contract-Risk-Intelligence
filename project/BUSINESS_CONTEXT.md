# Business Context

## Business Problem

The commercial directorate manages a large volume of procurement activity across multiple buyers, categories and suppliers, but current reporting is fragmented across individual notices and spreadsheets. Leadership cannot easily see where public spend is concentrated, where the same supplier is repeatedly winning work, where low-value purchasing is fragmented across multiple awards, or where contracts may create upcoming re-procurement pressure.

This creates three practical risks. First, commercial teams may become overly dependent on a small number of suppliers without recognising the concentration early enough. Second, fragmented purchasing may prevent the organisation from identifying opportunities to consolidate demand or negotiate more effectively. Third, upcoming contract end dates and award timing may not be visible in one place, making forward procurement planning reactive rather than planned.

The problem is therefore not “analyse procurement data”. The problem is that commercial leaders currently lack one governed, reproducible view that turns procurement notices into an evidence base for supplier review, category planning and future procurement workload.

## Required Delivery Response

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

## How the Client Will Use the Output

The finished product should support a monthly or quarterly commercial portfolio review. A Commercial Director should be able to open the dashboard and ask, for example: “Which category is becoming too concentrated around a small number of suppliers?”, “Which buyers appear to be repeatedly purchasing similar services in separate awards?”, or “Which contracts should procurement teams begin planning to re-compete soon?”

The output is not intended to automatically label suppliers as risky. It is intended to identify where commercial managers should investigate, challenge or plan earlier.

## Client
**Confidential Public Sector Commercial & Procurement Directorate**

## Current Problem
The directorate publishes and manages a large volume of procurement activity, but commercial leaders do not have one governed view of supplier concentration, repeated awards, fragmented buying, contract timing and SME participation. Existing reports are notice-centric rather than decision-centric, so teams cannot consistently distinguish genuine commercial exposure from simple high-volume activity.

## Decision Owner
**Commercial Director**

## Senior Stakeholders
Head of Procurement, Category Management Lead, Commercial Finance Lead, Supplier Management Lead, Data Governance Lead, Data & Analytics Lead

## Decision to Support
**Which suppliers, categories and contract groups should commercial leadership investigate first for concentration exposure, upcoming re-procurement pressure, fragmented demand or weak SME participation?**

## Role Responsibilities
| Role | Required contribution |
|---|---|
| Business Analyst | Produce stakeholder map, as-is/to-be decision process, requirements catalogue, user stories and acceptance criteria. |
| Data Governance Analyst | Produce procurement glossary, critical data-element register, ownership/stewardship matrix, DQ rules and lineage. |
| Data Engineer | Build repeatable ingestion/standardisation of daily OCDS CSVs and an auditable supplier-award analytical model. |
| Commercial/Data Analyst | Own concentration, fragmentation, SME and timing analysis plus interpretation. |
| BI Developer | Build governed semantic measures and the commercial portfolio dashboard. |
| Data Quality / Assurance Analyst | Own reconciliation, duplicate/amendment tests, UAT evidence and release QA. |

## Expected Organisational Outcome

The intended result is a governed, repeatable decision process. The BI product is one delivery component; it is not the project outcome by itself.

## Evidence Chain

**Requirement → governed field/definition → transformation → quality control → metric/analysis → decision insight → recommendation → UAT/acceptance**

Every major recommendation should be traceable through this chain.
