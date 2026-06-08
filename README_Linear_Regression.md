# EDA & Model Training — Linear Regression

**Assignment:** PGDip in Data Analytics  
**Author:** NR Dube  
**Notebook:** `NR_DUBE_-_EDA_ANALYSIS___MODEL_TRAINING_USING_LINEAR_REGRESSION.ipynb`

---

## Overview

This notebook applies **Multiple Linear Regression** to predict individual medical insurance charges based on a set of demographic and lifestyle variables.

---

## Dataset

| Detail | Info |
|---|---|
| Source | Kaggle |
| Title | Medical Cost Personal Datasets |
| Author | Miri Choi (2018) |
| Link | https://www.kaggle.com/datasets/mirichoi0218/insurance |

**Target variable:** `charges` (continuous — insurance costs in USD)  
**Predictor variables:** `age`, `bmi`, `children`, `sex`, `smoker`, `region`

---

## Workflow

1. **Data Loading & Inspection** — shape, data types, first 10 rows
2. **Data Cleaning** — checked for duplicates and missing values; mean imputation applied
3. **Encoding** — `sex`, `smoker`, and `region` label-encoded to numerical values
4. **EDA** — summary statistics, correlation matrix, histograms, scatter plots, boxplots
5. **Feature Selection** — based on correlation with `charges`
6. **Model Training** — 80/20 train-test split; Multiple Linear Regression fitted
7. **Evaluation** — R², MAE, MSE, RMSE; train vs test score comparison to check for overfitting
8. **Hyperparameter Tuning** — RandomizedSearchCV applied

---

## Key Libraries

`pandas`, `numpy`, `scikit-learn`, `seaborn`, `matplotlib`, `statsmodels`

---

## Evaluation Metrics

- R² (coefficient of determination)
- MAE (Mean Absolute Error)
- MSE (Mean Squared Error)
- RMSE (Root Mean Squared Error)
