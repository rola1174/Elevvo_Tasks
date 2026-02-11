# Loan Approval Prediction using Machine Learning

## Project Overview
This project builds a **Loan Approval Prediction** system using supervised machine learning techniques.  
The goal is to predict whether a loan application will be **approved or rejected** based on applicant financial and personal information.

The project focuses on handling **imbalanced data**, preprocessing categorical variables, and evaluating models using **Precision, Recall, and F1-score**.

---

## Dataset
Dataset used: **Loan Approval Prediction Dataset (Kaggle)**  
Link: https://www.kaggle.com/datasets/architsharma01/loan-approval-prediction-dataset

The dataset contains features such as:
- Number of Dependents
- Education
- Self Employment Status
- Annual Income
- Loan Amount
- Loan Term
- CIBIL Score
- Asset Values
- Loan Status (Target Variable)

---

## Objectives
- Handle missing values
- Encode categorical variables
- Address class imbalance using **SMOTE**
- Train classification models
- Compare **Logistic Regression** and **Decision Tree**
- Evaluate performance using **Precision, Recall, and F1-score**

---

## Tools & Libraries
- Python
- Pandas
- Scikit-learn
- Imbalanced-learn (SMOTE)

---

## Methodology
1. Load and explore dataset
2. Handle missing values using median and mode
3. Encode categorical variables using Label Encoding
4. Split dataset into training and testing sets
5. Apply **SMOTE** to handle class imbalance
6. Train Logistic Regression model
7. Train Decision Tree model
8. Evaluate models using classification metrics

---

## Results
Both models were evaluated using Precision, Recall, and F1-score to properly measure performance on imbalanced data.  
SMOTE improved the model's ability to correctly classify minority loan approval cases.

---

## Conclusion
Machine learning models can effectively predict loan approval decisions when proper preprocessing and imbalance handling techniques are applied.  
Evaluation using F1-score provides a more reliable performance measure compared to accuracy alone.

---
