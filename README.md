# Divorce Prediction with Machine Learning

A binary-classification project using the **Divorce Predictors** dataset to distinguish between married and divorced participants from questionnaire responses.

## Project overview

The analysis is implemented in R Markdown and explores a supervised machine-learning workflow on a small structured dataset. The original project reports that the models evaluated achieved 100% accuracy on its held-out test split; because the dataset is small, that result should be interpreted in the context of the specific split and validation design used in the analysis.

## Repository contents

- [`ADM_Project.Rmd`](ADM_Project.Rmd) — complete source analysis.
- [`README.md`](README.md) — project documentation.

## Data source

The project uses the UCI Divorce Predictors dataset. The dataset contains questionnaire-derived features from 170 participants: 84 divorced and 86 married.

## Objective

Build and compare classification models that predict marital-status class from the available predictor variables.

## Reproducing the analysis

1. Download the Divorce Predictors dataset referenced in `ADM_Project.Rmd`.
2. Open the R Markdown file in RStudio.
3. Install any required packages listed in the analysis.
4. Update the local data path if necessary and knit/run the document.

## Notes

This repository preserves the original academic analysis while documenting its scope and limitations more clearly for portfolio review.
