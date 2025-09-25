# Age-Related Differences in Delay Discounting: Income Matters

This repository contains the analysis scripts, figures, and presentation materials for the peer-reviewed publication:

> Wan, H., Myerson, J., Green, L., Strube, M. J., & Hale, S. (2024). Age-related differences in delay discounting: Income matters. *Psychology and Aging*. Advance online publication. https://doi.org/10.1037/pag0000818

The data for this study are publicly available on the Open Science Framework at: <https://osf.io/um68t/>.

---

## Project Overview

This study investigates the "buffering hypothesis," which posits that older adults may be less susceptible to the effects of financial scarcity on decision-making compared to younger adults. We examined the interaction between age and income on delay discounting—the tendency to devalue rewards that are further in the future.

The analysis employs a series of focused Bayesian multilevel regressions to test for age differences in discounting at both lower and higher income levels. This approach allows for a nuanced examination of the central hypothesis while robustly handling the hierarchical structure of the data.

## Repository Structure

The project materials are organized into the following folders:

* **/Analysis**: Contains the primary analysis scripts that replicate the findings in the paper.
    * `analysis.qmd`: A Quarto document with the complete **R** code for the entire workflow. It demonstrates data processing and the fitting of Bayesian hierarchical models using `brms`.
    * `analysis.ipynb`: A Jupyter Notebook providing a direct **Python** translation of the R analysis, using `pandas` for data manipulation and `pymc` for Bayesian modeling and inference.

* **/Presentation**: Contains a slide deck or poster used to present the findings of this research at an academic conference.

* **/Figure**: Contains the figures as they appear in the final publication.

---

## Methodology Snapshot

This project showcases a modern approach to statistical analysis in psychological science, including:

* **Bayesian Multilevel Modeling**: The core of the hypothesis testing relies on Bayesian binomial and beta regressions to model discounting measures, which are naturally bounded (i.e., proportions and choices). This approach provides robust estimates, particularly for complex interaction effects.
* **Focused Hypothesis Testing**: Instead of an omnibus model, the analysis uses a series of planned contrasts to directly test the effect of age within each income group, and vice versa.
* **Composite Measure Creation**: A composite z-score for discounting is calculated by combining measures from two different procedures (Adjusting-Amount and Monetary Choice Questionnaire) to provide a more reliable estimate of the underlying construct.
* **Data Quality and Reliability**: The analysis begins with data quality checks, including fitting nonlinear models to group-level data and calculating within-procedure reliability correlations.

---

## Software and Execution

To run the analyses, you will need the appropriate software environment and the raw data from the OSF repository linked above.

### R Environment (`/Analysis/analysis.qmd`)

* **Required Packages**: `readxl`, `minpack.lm`, `brms`, `tidybayes`, `bayestestR`, `dplyr`, `tidyr`, and others.
* **Installation**:
    ```R
    install.packages(c("readxl", "minpack.lm", "lme4", "glmmTMB", "multcomp", "brms", "tidybayes", "bayestestR", "psych", "dplyr", "tidyr", "stringr"))
    ```

### Python Environment (`/Analysis/analysis.ipynb`)

* **Required Packages**: `pandas`, `numpy`, `openpyxl`, `scipy`, `statsmodels`, `pymc`, `arviz`, `scikit-learn`.
* **Installation**:
    ```bash
    pip install pandas numpy openpyxl scipy statsmodels pymc arviz scikit-learn
    ```