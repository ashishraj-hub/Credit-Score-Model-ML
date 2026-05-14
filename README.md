# 💳 Credit Scoring Model using Machine Learning

## 📌 Project Overview
This project focuses on building a **Credit Scoring Model** to predict an individual's **creditworthiness** using historical financial data.  
The goal is to help financial institutions identify **high-risk borrowers** and reduce potential loan defaults.

The project uses the **"Give Me Some Credit"** dataset from Kaggle and applies multiple machine learning classification algorithms to evaluate and compare performance.

---

## 🎯 Problem Statement
Financial institutions face significant losses due to loan defaults.  
The objective of this project is to build a machine learning model that can:

- Predict whether a customer is likely to default on a loan
- Identify risky customers early
- Support better credit decision-making

This is formulated as a **binary classification problem**.

---

## 📊 Dataset Information

- **Dataset Name:** Give Me Some Credit  
- **Source:** Kaggle  
- **Target Variable:** `SeriousDlqin2yrs`  
  - `1` → Customer defaulted (Bad Credit)
  - `0` → Customer did not default (Good Credit)

### Key Features:
- MonthlyIncome
- DebtRatio
- Age
- Credit utilization ratio
- Number of late payments
- Number of active loans
- Number of dependents
- Engineered feature: `LatePaymentRatio`

---

## 🛠️ Technologies & Tools Used

- **Programming Language:** Python
- **Libraries:**
  - NumPy
  - Pandas
  - Scikit-learn
  - Matplotlib
  - Seaborn
  - Joblib
- **Modeling Techniques:**
  - Logistic Regression
  - Decision Tree
  - Random Forest
- **Evaluation Metrics:**
  - ROC-AUC
  - Precision
  - Recall
  - F1-Score

---

## ⚙️ Project Workflow

1. Data Loading and Exploration
2. Data Cleaning and Missing Value Handling
3. Feature Engineering
4. Train-Test Split with Stratification
5. Model Training
6. Model Evaluation and Comparison
7. Pipeline Creation
8. Model Saving and Loading
9. Testing with New Customer Data

---

## 🤖 Models Implemented

### 1️⃣ Logistic Regression
- Used as a baseline model
- Simple and interpretable
- Poor recall for defaulters due to class imbalance

### 2️⃣ Decision Tree
- Captures non-linear relationships
- Better recall and ROC-AUC than Logistic Regression
- Easy to explain

### 3️⃣ Random Forest (Final Model)
- Best balance between Precision and Recall
- High ROC-AUC score
- Handles class imbalance effectively
- Selected as the final production model

---

## 📈 Model Performance Summary

| Model | ROC-AUC | Precision | Recall | F1-Score |
|-----|--------|----------|-------|---------|
| Logistic Regression | ~0.71 | 0.58 | 0.04 | 0.08 |
| Decision Tree | ~0.85 | 0.60 | 0.15 | 0.24 |
| Random Forest | ~0.84 | 0.57 | 0.19 | 0.28 |

> **Note:** Accuracy was not considered the primary metric due to class imbalance.  
> Recall and ROC-AUC were prioritized to minimize financial risk.

---

## 🧠 Why Random Forest Was Chosen
- Identifies more defaulters compared to other models
- Reduces overfitting by combining multiple decision trees
- Performs well on tabular financial data
- Commonly used in real-world credit risk systems

---

## 🔗 Pipeline & Model Deployment

A **Scikit-learn Pipeline** was created to ensure consistent preprocessing and prediction:

- StandardScaler for feature scaling
- RandomForestClassifier as the final estimator

The trained pipeline was saved using **Joblib** for reuse and deployment.

```python
joblib.dump(pipeline, "credit_scoring_pipeline.joblib")
```

---

## 📂 Repository Structure
```
Credit-Score-Model-ML/
│── Credit Scoring Model.ipynb      # Main Jupyter Notebook
│── data(cs-training.csv)           # Dataset files
│── README.md                       # Project documentation
│── LICENSE                         # License file
```
---

## ⭐ Acknowledgements

- Kaggle for providing the dataset

- Scikit-learn documentation

- Open-source ML community

---

## 📜 License
This project is licensed under the MIT License - see the [License] file for details.

---

## 👤 Author

**Ashish Raj**

📌 LinkedIn: [LINKEDIN-ID](https://www.linkedin.com/in/ashish-raj-ashishraj/)

📌 GitHub: [GITHUB-ID](https://github.com/ashishraj-hub)

---

## ⭐ Support This Project

If this README or project helped you:
- **Star** ⭐ this repository
- **Fork** 🍴 it and build your own version
- **Share** it with someone who is learning Data Science or AI/ML

---
