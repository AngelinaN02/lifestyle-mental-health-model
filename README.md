# Mental Health Lifestyle Predicition

## Overview
This project uses ML to predict whether an individual is at risk for a mental health condition based on their lifestyle behaviors. By analyzing factors like stress, diet, and physical activity, we aim to uncover patterns that contribute to mental health outcomes.
Models are tained using Logisitic Regression and Random Forest, and SHAP is used to interpret model predictions.

---

## Objectives 
- Predict mental health conditions from lifestyle and demographic data
- Identify which features most influence model decisions
- Visualize results and explain the model using SHAP

---

## Dataset
- **Type**: Tabular (CSV)
- **Size**: ~50,000 rows, 17 columns 
- **Target**: `Mental_Health_Condition` (Yes/No)
- **Features**:
    - Age, Gender, Sleep Hours, Stress Level, Physical Activity
    - Work Hours, Diet Quality, Social Media Use, and more

---

## Tools & Technologies
- Python
- Pandas, NumPy
- Scikit-learn
- SHAP (SHapley Additive Explanations)
- Jupyter Notebook

---

## Model Summary
| Model              | Accuracy | Key Insight |
|-------------------|----------|-------------|
| Logistic Regression | ~50%     | Baseline model, evenly split predictions |
| Random Forest       | ~50%     | Slight improvement in class separation |
| SHAP                | —        | Provided interpretability and key feature insights |

> Note: Despite the balanced dataset, results indicate mental health is influenced by subtle, nonlinear interactions-making predicition a challenging task.

---

## SHAP Explanation

SHAP was used to interpret the model and understand how individual features contribute to predicitions.

### Global Insights (Beeswarm Plot)
- SHAP values were calculated for the first 1,000 individuals.
- Top predicitive features included:
    - **Age**
    - **Social Media Usage**
    - **Sleep Hours**
    - **Physical Activity Hours**
    - **Work Hours**
 - Bright pink -> features value, Blue -> low value
 - For example: High **Social Media USiage** and fewer **Sleep Hours** were associated with increaded mental health risk

### Individual Prediction (Waterfall Plot)
- A detailed explanation for one individual (age 48, sleep 6.9 hrs):
      - **Age** contributed slightly toward lower risk.
      - **Sleep Hours** slightly increaded predicted risk.
- The model output was near 0.497 - showing low conidence in predicition for this case.

Plots are included in the `visuals/` folfer.
