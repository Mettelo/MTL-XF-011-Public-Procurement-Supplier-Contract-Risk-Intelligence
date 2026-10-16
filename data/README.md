# Data Guidance

## Approved Core Scope

Use the **June 2026 Contracts Finder OCDS flattened CSV releases** as the frozen project cohort.

Official source:
https://www.data.gov.uk/dataset/c0b71bfc-2f31-4919-b1c5-e43179a104e2/contracts-finder-notices-06-2026

The source is published as **one CSV per calendar day**, not as one monthly file.

## What to Download

Download all June 2026 daily CSV files listed on the official dataset page.

Do not mix June 2026 with later months for the core submission unless your team documents an optional extension separately.

## Recommended Raw-Data Strategy

1. Keep the original daily CSV files unchanged in `data/raw/` where practical.
2. If storing all daily files makes the team repository unnecessarily heavy, preserve the originals in approved shared storage and keep a manifest in the repository containing:
   - exact source URL;
   - acquisition date;
   - file name;
   - file size;
   - checksum where practical.
3. Build one reproducible combined staging table from the daily files.
4. Do **not** manually copy/paste daily files together.

## Required Cohort

Core project period: **1 June 2026 to 30 June 2026**.

The full June cohort should be analysed before any optional extension.

## Important Source Handling

Contracts Finder may contain:
- multiple releases relating to the same contracting process;
- amended or replacement notices;
- incomplete value/date fields;
- inconsistent supplier names.

Do not assume one row equals one unique contract.

Before creating supplier or award metrics, document:
- analytical grain;
- duplicate/amendment handling;
- award/value inclusion rules;
- supplier-name standardisation rules.

## Recommended Raw Folder

```text
data/raw/
├── contracts-finder-2026-06-01.csv
├── contracts-finder-2026-06-02.csv
├── ...
└── contracts-finder-2026-06-30.csv
```

If all daily files are not committed, keep a `MANIFEST.csv` or equivalent listing every expected source file.

## Optional Extension

After the June solution passes acceptance criteria, the team may add July 2026 or another month to demonstrate refreshability. The June 2026 cohort remains the assessment baseline.
