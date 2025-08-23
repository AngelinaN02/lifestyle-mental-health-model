# Mental Health & Lifestyle Classifier

This project explores the use of machine learning to predict self-reported mental health conditions from lifestyle and demographic survey data.

Dataset: [Zenodo DOI: 10.5281/zenodo.14838680](https://doi.org/10.5281/zenodo.14838680) (~50,000 rows x 17 columns).

---

## Overview
- **Task:** Binary classification (Yes/No for mental health condition).
- **Inputs:** Sleep hours, stress level, physical activity, work hours, diet, substance use, demographics.
- **Output:** Predicted mental health condition.
- **Model:** Random Forest Classifier (scikit-learn)

---

## Approach
- Cleaned and encoded categorical + numerical survey data.
- Performed EDA with visualizations of lifestyle trends vs conditions.
- Trained Random Forest with 80//20 train-test split.
- Evaluated using accuracy, precision, recall, F1, and confusion matrix

---

## Results
- **Accuracy:** ~50% (baseline-level).
- **Precision / Recall / F1:** ~0.50 each.
- **Top Features:** Sleep Hours, Social Media Use, Work Hours, Physical Activity, Age.
- Despite weak predicitve performance, feature importance aligned with known mental health indicators.

---

## Visualizations
- Sleep hours vs. reported condition
- Stress levels vs. reported condition
- Medication usage by condition
- Feature importance from Random Forest

---

## Lesson Learned
- The dataset contained relevant features, but overall predictive signal was weak.
- Random Forest failed to generalize well, despite no signs of overfitting.
- Survey-based lifestyle data may not be sufficient for accurate prediction alone.

---

## Future Work
- Test advanced models (XGBoost, LightGBM).
- One-hot encode nominal features (e.g., Occupation).
- Engineer interaction features (e.g., stress x sleep).
- Add SHAP values for explainability.
- Supplement lifestyle data with structured/clinical features.

---

## Tech Stack
`Python` · `pandas` · `numpy` · `matplotlib` · `scikit-learn` · `seaborn`
