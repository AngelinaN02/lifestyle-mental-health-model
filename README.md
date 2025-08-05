# Mental Health & Lifestyle Classifier

This repository contains a machine learning model trained to predict mental health conditions based on lifestyle and demographic data, using survey responses from a publicy available dataset on Zenodo.

---

## Overview

**Task Definition**
The task is to classift whether an individual reports a mental health condition (`Yes` or `No`) based on lifestyle habits such as sleep, stress level, physical activity, work hours, diet, and substance use.

**Approach**
The problem is treated as a binary classification task. A Random Forest classifier was trained using encoded categorical and numerical features. Exploratory Data Analysis (EDA) was performed to understand key trends, and feature importance was used to interpret the model.

**Performance Summary**
The model achieved an accuracy of approximately **50%**. Although predictive performce was low, the model's most important features aligned with real-world indicators of mental health.

---

## Summary of Work Done

- Cleaned and encoded categorical and numerical survey data
- Explored key distributions through visualizations
- Trained a Random Forest classifier with 80/20 train-test split
- Evaluated model performance using accuracy, precision, recall and confusion matrix

---

## Data

**Type**
Tabular CSV file

**Source**
[Zenodo DOI: 10.5281/zenodo.14838680](https://doi.org/10.5281/zenodo.14838680)

**Size**
~50,000 rows x 17 columns

**Split**
- 80% training (40,000)
- 20% testing (10,000)

**Preprocessing Steps**
- Dropped irrelevent or identifier columns
- Encoded categorical features with `LabelEncoder`
- Handled missing values in severity and lifestyle columns
- Converted target to binary encoding

--- 

## Data Visualization

Visualizations include:

- Sleep Hours Distribution by Mental Health Condition
- Stress Level by Mental Health Condition
- Medication Usage by Condition
- Feature Importance from the Random Forest Model

These visuals helped confirm feature relevance and guided model interpretation.

---

## Problem Formulation

- **Input:** Lifestyle and demographic survey responses
- **Output:** Mental health condition (Yes/No)
- **Model:** Random Forest (Scikit-learn)
- **Loss/Optimizer:** Not applicable for RF; uses Gini-based impurity split
- **Hyperparameters:** Used default 100 estimators; `random_state=42`

---

## Training

- Trained using `scikit-learn` on Google Colab
- Runtime: ~5 seconds for training on ~40k rows
- Model trained in a single session; no early stopping or tuning
- No overfitting observed; model generalized poorly, suggesting limited predictive signal
- Key difficulty: weak correlations between features and target

--- 

## Performance Comparison

| Metric     | Value  |
|------------|--------|
| Accuracy   | 50%    |
| Precision  | ~0.50  |
| Recall     | ~0.50  |
| F1-Score   | ~0.50  |

**Top Features by Importance:**
- Sleep_Hours
- Social_Media_Usage
- Work_Hours
- Physical_Activity_Hours
- Age

No ROC curve included due to baseline-level performance.

---

## Conclusions

The model identified relevant health-related features, but the signal was not strong enough to enable useful predictions. Additional feature engineering and more sophisticated models could improve outcomes.

---

## Future Work

- Try XGBoost or LightGBM for improved performance
- Apply one-hot encoding to nominal features (e.g., Occupation)
- Use interaction terms or domain knowledge to build composite features
- Integrate SHAP values for deeper model explainability
- Collect more structured or clinical data to supplement lifestyle inputs

---

## Software Setup
`pandas`
`numpy`
`matplotlib`
`seaborn`
`scikit-learn`

---

## Citations
Pandey, B. (2024). *Mental Health and Lifestyle Dataset for Sentiment Analysis*. Zenodo. https://doi.org/10.5281/zenodo.14838680
