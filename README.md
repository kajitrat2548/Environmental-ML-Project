# Environmental-ML-Project
# Environmental Machine Learning Project: Water Quality Potability Prediction

## 🌍 Environmental Problem
Access to safe drinking water is vital for public health and environmental sustainability. Monitoring water safety manually is time-consuming and costly. This project aims to predict whether water is safe for human consumption based on various chemical and physical water quality parameters.

## 📊 Dataset Source
* **Dataset Name:** Water Quality Potability Dataset
* **Source:** Kaggle (Water Quality / Potability Data)
* **Description:** Contains water quality metrics for 3,276 water bodies, including pH, Hardness, Solids, Chloramines, Sulfate, Conductivity, Organic Carbon, Trihalomethanes, and Turbidity.

## ❓ Research Questions
1. Can we accurately predict water potability using machine learning classification models based on physicochemical water parameters?
2. Which water quality parameters (e.g., pH, Sulfate, Chloramines) are the most critical indicators for determining water safety?

## ⚙️ Methods
1. **Data Preprocessing:** Handled missing values using median imputation and standardized features using `StandardScaler`.
2. **Model Training:** Developed and trained 5 different machine learning models:
   * Logistic Regression
   * Random Forest Classifier
   * Gradient Boosting Classifier
   * Support Vector Machine (SVM)
   * XGBoost Classifier
3. **Hyperparameter Tuning:** Optimized the best-performing model (Random Forest) using `GridSearchCV`.

## 📈 Main Results & Best Model
* **Best Model:** Random Forest Classifier (optimized via hyperparameter tuning)
* **Test Accuracy:** ~82%
* **ROC-AUC Score:** ~0.85
* The ensemble tree-based models significantly outperformed linear models due to non-linear relationships between water parameters and safety thresholds.

## 🔍 Feature Importance (Explainable ML)
Based on feature importance analysis from the Random Forest model:
1. **pH Level:** The most influential factor, reflecting acidity/alkalinity limits set by environmental health standards.
2. **Sulfate & Chloramines:** High contributors, indicating chemical treatment efficiency and mineral content.
*(Saved visualization figure can be found in `figures/feature_importance.png`)*

## 🌱 Environmental Interpretation
The machine learning model successfully highlights that maintaining strict controls over chemical additives (like chloramines and sulfates) and balancing water pH are paramount for ensuring safe drinking water. Environmental agencies can leverage this predictive workflow to automate preliminary water quality screenings before deploying expensive lab testing.