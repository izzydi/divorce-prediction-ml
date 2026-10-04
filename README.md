# Divorce Prediction with Machine Learning

A binary-classification project using the **UCI Divorce Predictors** questionnaire dataset.

## Primary workflow

[`divorce_prediction.Rmd`](divorce_prediction.Rmd) is the audited source. It uses a stratified hold-out split, computes correlation and PCA from training data only, performs repeated cross-validation only inside the training partition, and compares logistic regression with a 500-tree Ranger Random Forest before a final held-out evaluation.

## Repository contents

- [`divorce_prediction.Rmd`](divorce_prediction.Rmd) — audited R Markdown workflow.
- [`archive/legacy_course_analysis.Rmd`](archive/legacy_course_analysis.Rmd) — original coursework retained for provenance.
- [`data/README.md`](data/README.md) — authoritative UCI source, license and expected dataset layout.
- [`R-packages.txt`](R-packages.txt) — version-pinned direct R dependencies.
- [`.github/workflows/r-ci.yml`](.github/workflows/r-ci.yml) — R 4.6.1 dependency and syntax CI.

## Audit improvements

The original analysis calculated one correlation matrix using the complete dataset after splitting, allowing held-out information into that transformation. The current workflow keeps exploratory transforms and model selection inside training data. It also avoids presenting the original 100% split-specific accuracy as a generalizable performance claim.

## Data

The dataset contains 170 observations and 54 questionnaire predictors. [`data/README.md`](data/README.md) records the authoritative UCI dataset page, DOI and license. Because the dataset is small, model performance can vary materially across samples; results should be interpreted as an educational modelling exercise rather than a real-world assessment tool.

## Reproducing the analysis

1. Install R 4.6.1.
2. Place `divorce.csv` under `data/` as described in [`data/README.md`](data/README.md).
3. Install `pak` and the pinned direct dependencies:

```r
install.packages("pak")
pak::pkg_install(readLines("R-packages.txt"), upgrade = FALSE)
```

4. Run or knit `divorce_prediction.Rmd` from top to bottom.

GitHub Actions performs the same direct-dependency installation and parses the canonical R Markdown source on every push and pull request. `R-packages.txt` is a direct-dependency manifest, not a complete `renv.lock` snapshot.

## Scope

This is an academic machine-learning portfolio project. It is not intended for relationship, legal, psychological or clinical decision-making.
