# Machine Learning for HIV/AIDS Prediction using Explainable AI
## 📌 Project Overview

This project presents a comparative analysis of multiple machine learning algorithms for predicting HIV/AIDS status using socio-behavioral data. The study evaluates traditional, ensemble, and stacked models to identify the most effective predictive approach while integrating Explainable AI (SHAP) techniques to enhance model transparency.

This work was authored and presented at the **International Conference on Cybernetics and Intelligent Systems (ICORIS)**.

---

## 🎯 Objectives

- Compare the performance of multiple machine learning models for HIV/AIDS prediction  
- Identify the best-performing model based on classification metrics  
- Improve model interpretability using SHAP (SHapley Additive Explanations)  
- Demonstrate the importance of explainability in healthcare AI systems  

---

## 📊 Dataset

- Source: [Public Kaggle dataset](https://www.kaggle.com/datasets/ishigamisenku10/hiv-prediction)
- Total samples: 698  
- Features: 10 socio-behavioral attributes including:
  - Age  
  - Marital Status  
  - STD history  
  - Educational Background  
  - HIV Test (past year)  
  - AIDS Education
  - Places of seeking sex partners  
  - Sexual Orientation  
  - Drug-taking behavior  
  - Target: HIV Status (Positive / Negative)

---

## ⚙️ Methodology

### 1️⃣ Data Preprocessing

- Data cleaning and categorical standardization  
- Train-test split (80:20)  
- Feature scaling using `StandardScaler`  
- One-hot encoding for categorical variables  
- Label encoding for target variable  
- Pipeline construction using `ColumnTransformer`  

### 2️⃣ Models Evaluated

- Logistic Regression  
- Gaussian Naive Bayes  
- Decision Tree  
- Support Vector Machine (SVM)  
- Random Forest  
- XGBoost  
- Stacked Ensemble (meta-learner: Logistic Regression)  

Hyperparameter tuning was performed using **GridSearchCV with 5-fold cross-validation**.

---

## 🔍 Explainable AI (SHAP)

To improve transparency and interpretability, SHAP was integrated into the best-performing model.

SHAP analysis provided:

- Global feature importance (Beeswarm & Bar plots)
- Individual prediction explanations (Waterfall plot)
- Identification of key predictors such as:
  - Partner-seeking behavior (Internet, Bar)
  - Drug-taking behavior
  - Age
  - Educational background

This enhances trust and supports potential real-world healthcare applications.

---

## 🌐 Interactive Gradio Interface

To demonstrate real-world usability, the trained Random Forest model was deployed using **Gradio**, enabling users to:

- Input socio-behavioral features manually  
- Receive instant HIV risk prediction  
