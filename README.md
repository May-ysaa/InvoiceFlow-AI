# InvoiceFlow AI

InvoiceFlow AI is a Python-based research and development project for bulk invoice understanding, document extraction, validation, and structured export.

> **Current stage:** Synthetic dataset v1.0.0 is complete. The invoice extraction baseline is the next development stage.

## Project objectives

InvoiceFlow AI is being developed to:

- process invoice documents in batches;
- extract important invoice fields;
- normalize extracted values;
- validate financial and document information;
- export structured results for downstream systems;
- provide measurable extraction quality.

## Current dataset milestone

- 200 fully synthetic invoice documents
- 10 distinct invoice templates
- Indonesian and English language coverage
- IDR, USD, EUR, and GBP currency coverage
- 120 development documents
- 40 validation documents
- 40 test documents
- 200/200 documents passed automated technical QA
- 30 stratified visual samples covered all 10 templates
- Final dataset integrity status: `PASSED`
- Release metadata status: `FROZEN`

The dataset is entirely synthetic and contains no real customer invoices. Generated PDF, preview, ground-truth, and QA artifacts are retained outside this public repository.

## Repository structure

```text
InvoiceFlow-AI/
├── notebooks/
│   ├── 00_environment_setup.ipynb
│   └── 01_data_collection_and_audit.ipynb
├── .gitignore
├── LICENSE
├── README.md
└── requirements.txt
```

## Notebooks

### 00 — Environment setup

[Open 00_environment_setup.ipynb in Google Colab](https://colab.research.google.com/github/May-ysaa/InvoiceFlow-AI/blob/main/notebooks/00_environment_setup.ipynb)

Prepares the Google Colab runtime, connects Google Drive, installs dependencies, separates source code from data, and performs environment readiness checks.

### 01 — Synthetic data collection and audit

[Open 01_data_collection_and_audit.ipynb in Google Colab](https://colab.research.google.com/github/May-ysaa/InvoiceFlow-AI/blob/main/notebooks/01_data_collection_and_audit.ipynb)

Builds the synthetic invoice dataset and performs template rendering, annotation generation, technical QA, stratified visual review, integrity verification, and release metadata preparation.

## Getting started

Clone the repository:

```bash
git clone https://github.com/May-ysaa/InvoiceFlow-AI.git
cd InvoiceFlow-AI
```

Install the Python dependencies:

```bash
python -m pip install -r requirements.txt
```

Google Colab is the primary environment for the current notebook workflow. Start with `notebooks/00_environment_setup.ipynb`.

## Data and security policy

- Real invoices and private documents must not be committed to GitHub.
- Generated dataset artifacts are stored separately in Google Drive.
- Credentials must use environment variables or Colab Secrets.
- Repository commits contain source code and documentation only.

## Quality scope

Automated technical QA was performed on all 200 synthetic documents. Manual visual review used a stratified sample of 30 documents covering all 10 templates and both supported languages.

The manual review result therefore represents the selected sample and is not a claim that every generated page was manually inspected.

## Development roadmap

- [x] Environment initialization
- [x] Synthetic dataset generation
- [x] Annotation and ground-truth generation
- [x] Technical QA and integrity verification
- [x] Synthetic dataset v1.0.0 release metadata
- [ ] Invoice extraction baseline
- [ ] Field normalization and validation
- [ ] Evaluation on development and validation splits
- [ ] Batch processing application

## Licensing

The source code in this repository is licensed under the [MIT License](LICENSE).

A separate public-distribution license has not yet been assigned to the generated synthetic dataset. Dataset distribution remains disabled until that decision is documented.

## Author

**Muhammad Mayyosa**

GitHub: [May-ysaa](https://github.com/May-ysaa)
