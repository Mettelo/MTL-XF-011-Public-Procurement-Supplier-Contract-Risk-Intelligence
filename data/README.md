# Data Workspace

## Primary Dataset

**Contracts Finder Notices — June 2026 (Open Contracting Data Standard flattened CSV)**

**Publisher:** Crown Commercial Service / Contracts Finder  
**Format:** CSV (daily OCDS flattened files)  
**Official source:** https://www.data.gov.uk/dataset/c0b71bfc-2f31-4919-b1c5-e43179a104e2/contracts-finder-notices-06-2026

## Mettelo Data Durability Standard

This project uses a frozen cohort dataset/reference so that future teams are not dependent on a changing website or API.

Teams should:

1. preserve the original raw file unchanged;
2. record acquisition date/version;
3. retain official source and methodology links;
4. create processed data separately;
5. make refresh logic optional rather than essential to reproducing the original project.

## Structure

```text
data/
├── README.md
├── SOURCE_REGISTER.md
├── raw/
├── reference/
└── metadata/
```

Large files that are unsuitable for normal Git storage should be stored through the approved Mettelo data location and referenced reproducibly from this folder.
