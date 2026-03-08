# Training Module

## Current Status

The training module is currently focused on baseline experiments for UCI dataset `336` only.

At this stage:

- dataset `336` is the primary training and development dataset
- dataset `857` is not used for baseline experiments in this module
- AutoPrognosis training has not started yet
- AWS deployment work is out of scope here

## What This Round Covers

This round implements a reproducible baseline experiment package for `336`:

- baseline setup and reproducible split artifacts
- Logistic Regression
- Random Forest
- XGBoost if available, otherwise `HistGradientBoostingClassifier`
- CV evaluation on the training split
- held-out test evaluation
- plots and markdown summary outputs

## Baseline Versus AutoPrognosis

Baseline models are used here to establish a defensible reference point before AutoPrognosis training begins.

They answer a different question from AutoPrognosis:

- baseline models: "What performance can standard models achieve under a reproducible sklearn pipeline?"
- AutoPrognosis: "Can a more automated clinical modeling workflow improve or match that baseline under the thesis setting?"

## Why Imputation Is Allowed Here

The raw aligned dataset is not modified in place.

For baseline models only, imputation is allowed inside sklearn Pipelines and ColumnTransformers because:

- sklearn estimators generally require complete numeric inputs
- the preprocessing stays fully reproducible
- the imputation choice remains local to each model pipeline
- the raw aligned CSV remains unchanged outside the pipeline

This does not mean the repository has permanently imputed the dataset.

## Expected Outputs

Artifacts are written to `artifacts/baselines_336/`, including:

- setup metadata
- split indices
- CV results
- held-out test results
- per-model prediction files
- best-model artifact and metadata
- ROC / PR / calibration plots
- confusion matrix for the best model
- markdown summary for thesis writing support
