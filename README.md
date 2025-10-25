# Modeling Interaction Effects in Behavioral Science
### A Reproducible Analysis of Wan et al. (2024), *Psychology and Aging*

This repository contains the complete analysis scripts and materials for the peer-reviewed publication:

> Wan, H., Myerson, J., Green, L., Strube, M. J., & Hale, S. (2024). Age-related differences in delay discounting: Income matters. *Psychology and Aging*. Advance online publication. https://doi.org/10.1037/pag0000818

The data for this study are publicly available on the Open Science Framework at: **[https://osf.io/um68t/](https://osf.io/um68t/)**.

---

## Project Objective

The goal of this project is to investigate how age moderates the relationship between socioeconomic status and intertemporal decision-making. We test the **"buffering hypothesis,"** which predicts that the effect of income on choice behavior is attenuated in older adults.

The analysis employs a series of focused Bayesian hierarchical models to provide a robust and nuanced test of this interaction, demonstrating a complete and reproducible workflow from data processing to statistical inference and reporting.

## Repository Contents

| File / Folder | Description |
| :--- | :--- |
| **`/Analysis/`** | Contains the primary scripts that replicate all findings in the paper. |
| `analysis.qmd` | A Quarto document with the complete **R** workflow, using `brms` for Bayesian modeling. |
| `analysis.ipynb` | A Jupyter Notebook providing a **Python** translation of the analysis, using `pymc` for modeling. |
| **`/Presentation/`** | A slide deck used to present the research findings at an academic conference. |
| **`/Figure/`** | All figures as they appear in the final publication. |

---

## Methodological Approach

This project showcases a modern, rigorous approach to quantitative analysis, highlighting the following skills:

* **Bayesian Hierarchical Modeling**: Implemented Bayesian generalized linear mixed-effects models (binomial and beta regressions) to accurately model the bounded nature of the outcome variables (choices and proportions) while accounting for the nested data structure (multiple observations per participant).
* **Focused Hypothesis Testing**: Used a series of planned contrasts to directly test the theoretically-driven hypotheses, examining the effect of age within each income group and vice-versa.
* **Latent Construct Estimation**: Created a composite z-score by standardizing and averaging measures from two distinct behavioral tasks, providing a more reliable and robust estimate of the underlying construct of delay discounting.
* **Data Validation and Reliability**: The workflow begins with essential data quality checks, including assessing the fit of nonlinear models to group-level data and calculating within-procedure (alternate-forms) reliability.

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