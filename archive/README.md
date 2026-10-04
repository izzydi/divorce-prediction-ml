# Legacy course analysis

`legacy_course_analysis.Rmd` preserves the original coursework.

The audited source is [`../divorce_prediction.Rmd`](../divorce_prediction.Rmd). The legacy analysis included a correlation calculation on the full dataset after a train/test split, which allowed held-out information into an exploratory transformation. The audited workflow keeps correlation, PCA, cross-validation and model selection inside the training partition and evaluates only once on a stratified hold-out set.
