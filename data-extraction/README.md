# Data extraction and audit

This directory contains the prompts used for data extraction and the subsequent audit for the systematic review *Artificial Intelligence for Biosound-Based Healthcare: A Systematic Review of Machine Learning, Deployment Architectures, and Technological Maturity*.

## Workflow

1. **Full-text reading and annotation.** Reviewer AT read each included article in full and highlighted passages relevant to the extraction fields in Zotero.
2. **ChatGPT-assisted extraction.** The reviewer used the resulting excerpts and notes as input to ChatGPT. The extraction instructions were organised into five modules, each used in a dedicated conversation. The reviewer supervised the extraction, checked the suggested values against the source evidence and recorded the final values in the extraction matrix.
3. **Post-extraction audit.** After completing the matrix, the reviewer used the audit prompt to check existing entries against the applicable extraction rules and the supplied excerpts or annotations. The audit focused on identifying substantive extraction errors and cases requiring further verification.

## Extraction modules

| Module | Fields covered |
| --- | --- |
| [Module 01](modules/module-01.md) | Study aim, targeted disorder or application domain, clinical or functional purpose, study type, and database |
| [Module 02](modules/module-02.md) | Origin of data, sample size, biosound modality, feature sets, additional data, and feature engineering strategy |
| [Module 03](modules/module-03.md) | ML paradigm and proposed ML algorithm, including algorithmic family and architecture |
| [Module 04](modules/module-04.md) | Computational workflow architecture, computational infrastructure, architectural deployment strategy, deployment maturity, and deployment level |
| [Module 05](modules/module-05.md) | Clinical setting, real-time capability, privacy and confidentiality mechanisms, and explainability |

## Audit prompt

The [audit prompt](audit/extraction-audit-prompt.md) takes three inputs:

1. The extraction rules relevant to the review.
2. The existing row from the completed data-extraction matrix.
3. Excerpts or annotations from the original article.

The reviewer retains defensible entries, checks the source further when the supplied evidence is insufficient, and corrects entries when the evidence establishes a substantive error.

## AI tool

- **Tool:** ChatGPT Plus (OpenAI).
- **Model:** [GPT-6]
- **Training setting:** The “Improve the model for everyone” setting was turned off during data extraction and the subsequent audit.
