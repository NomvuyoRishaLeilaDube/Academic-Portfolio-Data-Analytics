# EDA & Model Training — Logistic Regression & Gaussian Naïve Bayes

**Assignment:** PGDip in Data Analytics  
**Author:** NR Dube  
**Notebook:** `NR_DUBE_-_EDA_ANALYSIS___MODEL_TRAINING_USING_LOGISTIC_REGRESSION_AND_NAIVES_BAYES.ipynb`

---

## Overview

This notebook applies **Logistic Regression (LR)** and **Gaussian Naïve Bayes (GNB)** to classify cancer type based on a range of lifestyle, environmental, and genetic risk factors. LR is the primary model; GNB serves as the comparison model.

---

## Dataset

| Detail | Info |
|---|---|
| Source | Kaggle |
| Title | Cancer Risk Factors Dataset |
| Author | Tarek Masryo (2025) |
| Link | https://www.kaggle.com/datasets/tarekmasryo/cancer-risk-factors-dataset |

**Target variable:** `Cancer_Type` — 5 classes: Lung, Breast, Colon, Prostate, Skin  
**Features (19):** demographics (`Age`, `Gender`, `BMI`), lifestyle (`Smoking`, `Alcohol Use`, diet variables), environmental (`Air_Pollution`, `Occupational_Hazards`), genetic (`Family_History`, `BRCA_Mutation`), and risk indicators  
**Note:** Dataset is synthetic (2 000 records); no real patient data

---

## Workflow

1. **Data Loading & Inspection** — shape, data types, first 10 rows
2. **Data Cleaning** — checked for duplicates and missing values; `Patient_ID` dropped
3. **Encoding** — `Cancer_Type` and `Risk_Level` label-encoded; predictor variables were already numerical
4. **EDA** — summary statistics, correlation matrix, histograms, boxplots, count plots
5. **Feature Selection** — based on correlation analysis
6. **Model Training** — 80/20 train-test split; LR and GNB trained separately
7. **Evaluation** — accuracy, macro F1 score, precision, recall, confusion matrix, classification report
8. **Hyperparameter Tuning** — GridSearchCV applied to both LR and GNB (`var_smoothing`)
9. **Validation** — tuned models validated on a synthetic holdout dataset (`synthetic_validation_dataset.csv`)

---

## Files

| File | Description |
|---|---|
| `NR_DUBE_-_EDA_ANALYSIS___MODEL_TRAINING_USING_LOGISTIC_REGRESSION_AND_NAIVES_BAYES.ipynb` | Main notebook |
| `synthetic_validation_dataset.csv` | 300-row synthetic holdout dataset used for final model validation (15 features, same structure as training data) |

---

## Key Libraries

`pandas`, `numpy`, `scikit-learn`, `seaborn`, `matplotlib`, `statsmodels`

---

## Evaluation Metrics

- Accuracy
- Macro F1 Score
- Precision & Recall
- Confusion Matrix
- Classification Report
