# messy-to-clean

A structured workspace for turning raw, messy data into clean, validated, analysis-ready datasets.

This repository uses a **Cookiecutter Data Science–style** layout. Each directory contains a short README describing its purpose.

## Project structure

```text
messy-to-clean/
├── data/
│   ├── raw/          # Immutable source data
│   ├── interim/      # Intermediate transformed data
│   ├── processed/    # Clean, analysis-ready data
│   └── external/     # Third-party data sources
├── docs/             # Project documentation
├── models/           # Trained model artifacts
├── notebooks/        # Exploration and experiments
├── references/       # Papers, manuals, and source material
├── reports/
│   └── figures/      # Generated plots and figures
└── src/
    ├── data/         # Data ingestion and cleaning
    ├── features/     # Feature engineering
    ├── models/       # Training and inference code
    └── visualization/ # Plotting utilities
```

## Recommended workflow

1. Store original datasets in `data/raw/` and keep them unchanged.
2. Put temporary cleaning outputs in `data/interim/`.
3. Save validated, analysis-ready datasets in `data/processed/`.
4. Keep reusable pipeline code in `src/`; use notebooks for exploration.
5. Save model artifacts in `models/` and generated reports/figures in `reports/`.

## Data handling

Do not commit secrets, credentials, or sensitive data. For large datasets and model artifacts, consider Git LFS or external object storage. Document dataset sources, licenses, and transformation steps.
