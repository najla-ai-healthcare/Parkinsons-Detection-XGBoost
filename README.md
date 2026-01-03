#  Parkinson’s Disease Detection using XGBoost

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1zkaUpPsqN44HNqBRSiZ72cTiR1g0F0RP?usp=sharing)

## Project Overview
This project aims to accurately detect Parkinson's Disease using vocal feature measurements. By leveraging the **XGBoost Classifier** and optimizing it through **GridSearchCV**, the model achieves high diagnostic accuracy, which is crucial for early clinical intervention.

---

## Technical Workflow

### 1. Data Preprocessing
- **Feature Scaling:** Applied `StandardScaler` to normalize vocal features, ensuring optimal performance for the gradient boosting algorithm.

### 2. Modeling & Optimization
- **Baseline Model:** Initialized an `XGBClassifier` with tuned hyperparameters (learning rate, max depth, etc.).
- **Hyperparameter Tuning:** Conducted a comprehensive **GridSearchCV** over a multi-dimensional parameter grid (n_estimators, max_depth, subsample) using 5-fold cross-validation.
- **Evaluation:** Focused on **ROC-AUC** and **Accuracy** to ensure a robust balance between sensitivity and specificity.

### 3. Model Explainability & Interpretability
To move beyond "black-box" modeling, I implemented two layers of interpretation:
- **XGBoost Feature Importance:** Visualized feature gains to identify which vocal markers contribute most to the prediction.
- **SHAP (Shapely Additive explanations):** Utilized **SHAP beeswarm plots** to understand the impact of each feature on individual predictions, providing clinical transparency.

---

## Key Visualizations
The repository includes:
* **ROC Curve:** Demonstrating the trade-off between True Positive and False Positive rates.
* **Feature Importance (Gain):** Ranking the top 10 vocal features.
* **SHAP Beeswarm Plot:** Showing the distribution and impact of features on the model output.

---

##  Results
- **Optimized Performance:** Achieved peak test accuracy and ROC-AUC through systematic grid search.
- **Explainable AI:** Successfully identified key biomarkers for Parkinson's detection using SHAP values.

---

## 💻 Tech Stack
- **Language:** Python
- **Core Libraries:** XGBoost, Scikit-Learn, SHAP
- **Visualization:** Matplotlib, Seaborn# Parkinsons-Detection-XGBoost
Parkinson's detection using XGBoost and SHAP for model interpretability
