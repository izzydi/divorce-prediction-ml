# Divorce Prediction with Machine Learning

A binary-classification project using the **UCI Divorce Predictors** questionnaire dataset.

## Primary workflow

[`divorce_prediction.Rmd`](divorce_prediction.Rmd) is the audited source. It uses a stratified hold-out split, computes correlation and PCA from training data only, performs repeated cross-validation only inside the training partition, and compares logistic regression with a 500-tree Ranger Random Forest before a final held-out evaluation.

## Repository contents

- [`divorce_prediction.Rmd`](divorce_prediction.Rmd) — audited R Markdown workflow.
- [`archive/legacy_course_analysis.Rmd`](archive/legacy_course_analysis.Rmd) — original coursework retained for provenance.
- [`data/README.md`](data/README.md) — expected dataset layout.
- [`R-packages.txt`](R-packages.txt) — direct R dependencies.

## Audit improvements

The original analysis calculated one correlation matrix using the complete dataset after splitting, allowing held-out information into that transformation. The current workflow keeps exploratory transforms and model selection inside training data. It also avoids presenting the original 100% split-specific accuracy as a generalizable performance claim.

## Data

The dataset contains 170 observations and 54 questionnaire predictors. Because it is small, model performance can vary materially across samples; results should be interpreted as an educational modelling exercise rather than a real-world assessment tool.

## Reproducing the analysis

1. Place `divorce.csv` under `data/` as described in [`data/README.md`](data/README.md).
2. Install packages in [`R-packages.txt`](R-packages.txt).
3. Run or knit `divorce_prediction.Rmd` from top to bottom.

## Scope

This is an academic machine-learning portfolio project. It is not intended for relationship, legal, psychological or clinical decision-making.
