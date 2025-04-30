# 📊 Insurance Benefit Prediction Project

## Overview

This project explores customer data to predict whether individuals are likely to receive insurance benefits and to what extent. The work includes similarity analysis, classification, regression modeling, and data obfuscation—all performed with a strong focus on interpretability, performance, and data privacy.

---

## 🧠 Objectives

1. **Customer Similarity Analysis**  
   Group similar customers to support marketing and operational decisions.

2. **Binary Classification (k-Nearest Neighbors vs. Dummy Classifier)**  
   Predict whether a customer will receive any insurance benefit (`insurance_benefits > 0`) using kNN with hyperparameter tuning. Compare it to a chance-based dummy model.

3. **Regression (Linear Regression)**  
   Predict the amount of insurance benefits using a custom Linear Regression model. Evaluate the impact of feature scaling on performance.

4. **Data Obfuscation with Invertible Matrix**  
   Apply matrix transformations to mask sensitive features and demonstrate that the linear model maintains predictive performance with obfuscated data.

---

## 🔑 Key Results

### Task 1: Customer Similarity  
- Built a method to find nearest neighbors based on feature similarity.  
- Helped agents identify customer segments for targeted communication.

---

### Task 2: Binary Classification (Insurance Benefit Eligibility)  
**Model:** k-Nearest Neighbors (kNN)  
**Metric:** F1 Score  

- Scaling had a major impact: F1 scores jumped from 0.02–0.60 (unscaled) to 0.89–0.94 (scaled).
- Best F1: **0.94** with **k=3** on scaled data.
- Dummy classifier maxed out at F1 ≈ 0.20, showing kNN's clear advantage.

---

### Task 3: Regression (Benefit Amount)  
**Model:** Custom Linear Regression  
**Metric:** RMSE, R²  

- **Scaled RMSE:** 0.34  
- **R² Score:** 0.43 (43% of variance explained)  
- Certain features (e.g., the first one) had strong negative influence, others minimal.

---

### Task 4: Data Obfuscation  
- Used matrix multiplication with a random **invertible matrix** to obfuscate feature data.
- After transforming and inverse transforming, the difference from original data was negligible (e.g., 1e-12 scale).
- Model performance **unchanged**:  
  - **Original RMSE:** 0.5461  
  - **Obfuscated RMSE:** 0.5461  
  - **R² scores were identical up to floating-point precision**

---

## ✅ Conclusions

- **kNN is highly effective** when features are scaled, outperforming dummy/random models by a large margin.
- **Linear Regression**, while simple, offers interpretable and fairly accurate predictions of insurance benefits.
- **Feature scaling and data obfuscation** play critical roles in improving model robustness and preserving privacy without sacrificing performance.
- **Custom implementations** reinforced understanding of machine learning mechanics and matrix algebra in practical settings.

---

## ⚙️ Tech Stack

- Python, NumPy, Pandas
- scikit-learn
- Jupyter Notebooks
- Custom ML implementations (kNN, Linear Regression)
- Data visualization and metrics evaluation tools

---

## 🚀 Future Work

- Add cross-validation and feature selection to improve generalizability.
- Explore ensemble classifiers for insurance benefit prediction.
- Implement secure multi-party computation or federated learning for data privacy at scale.

