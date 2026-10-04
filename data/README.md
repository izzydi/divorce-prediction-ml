# Data

This project uses the **UCI Divorce Predictors data set** (UCI dataset ID 539).

Authoritative source:

- UCI dataset page: https://archive.ics.uci.edu/dataset/539/divorce%2Bpredictors%2Bdata%2Bset
- DOI: https://doi.org/10.24432/C53W5P
- License: CC BY 4.0

The UCI dataset contains 170 observations and 54 predictor features. The audited workflow expects the semicolon-delimited source file to be extracted/renamed as:

```text
data/divorce.csv
```

and expects the binary target column to be named `Class`.

For exact reproduction, keep an unmodified copy of the downloaded source archive/file and record its checksum alongside the analysis environment.
