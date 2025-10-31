# Modeling Interaction Effects in Behavioral Science
### A Reproducible Analysis of Wan et al. (2024), *Psychology and Aging*

This repository contains the complete analysis scripts and materials for the peer-reviewed publication:

> Wan, H., Myerson, J., Green, L., Strube, M. J., & Hale, S. (2024). Age-related differences in delay discounting: Income matters. *Psychology and Aging*. Advance online publication. https://doi.org/10.1037/pag0000818

The data for this study are publicly available on the Open Science Framework at: **[https://osf.io/um68t/](https://osf.io/um68t/)**.

---

## Project Objective

The goal of this project is to investigate how age moderates the relation between socioeconomic status and intertemporal decision-making. We test the **"buffering hypothesis,"** which predicts that the effect of income on choice behavior is attenuated in older adults.

The analysis employs a series of focused Bayesian hierarchical models to provide a robust and nuanced test of this interaction, demonstrating a complete and reproducible workflow from data processing to statistical inference and reporting.

## Repository Contents

| File / Folder | Description |
| :--- | :--- |
| **`/Analysis/`** | Contains the primary scripts that replicate all findings in the paper. |
| `analysis.qmd` | A Quarto document with the complete **R** workflow, using `brms` for Bayesian modeling. |
| `analysis.ipynb` | A Jupyter Notebook providing a **Python** translation of the analysis, using `pymc` for modeling. |
| **`/Presentation/`** | Contains the poster that was presented at DACC. |
| **`/Figure/`** | All figures as they appear in the final publication. |

---

## Methodological Approach

The analysis uses a multi-step workflow to test the study's primary hypotheses while ensuring the validity of the data and measures.

* **Data Validation and Reliability**: The workflow begins with essential data quality checks, including fitting nonlinear models to group-level data to confirm systematic behavioral patterns and calculating within-procedure (alternate-forms) reliability correlations to ensure the measures are internally consistent.
* **Bayesian Hierarchical Modeling**: The core of the analysis relies on Bayesian generalized linear mixed-effects models (binomial and beta regressions) to accurately model the bounded nature of the outcome variables (choices and proportions) while accounting for the nested data structure (multiple observations per participant).
* **Focused Hypothesis Testing**: Instead of a single omnibus model, hypotheses were tested using a series of planned contrasts to directly assess the theoretically-driven predictions, such as the effect of age within each income group.
* **Composite Score Analysis**: A composite z-score was created by standardizing and averaging measures from two distinct behavioral tasks. This provides a single, robust estimate of the underlying construct for final correlational and regression analyses.

---

## How to Reproduce This Analysis

To run these analyses, first download the raw data from the OSF repository linked above and place it in the `/Analysis/` directory. Then, set up the appropriate software environment as described below.

### R Environment (`/Analysis/analysis.qmd`)

* **Required Packages**: `brms`, `dplyr`, `tidybayes`, `readxl`, `minpack.lm`, and others listed in the script.
* **Installation**:
    ```R
    install.packages(c("brms", "tidybayes", "bayestestR", "dplyr", "tidyr", "readxl", "minpack.lm"))
    ```

### Python Environment (`/Analysis/analysis.ipynb`)

* **Required Packages**: `pymc`, `pandas`, `arviz`, `statsmodels`, `scipy`, `numpy`, `openpyxl`, `scikit-learn`.
* **Installation**:
    ```bash
    pip install pymc pandas arviz statsmodels scipy numpy openpyxl scikit-learn
    ```