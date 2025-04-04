# Bank Marketing Term Deposit Prediction

## Project Overview

This project analyzes a direct marketing campaign dataset from a Portuguese bank to predict whether a client will subscribe to a term deposit. The dataset includes client demographics, contact details, campaign-related variables, and socio-economic indicators.

The goal is to build and compare machine learning models to identify clients most likely to respond positively to future marketing efforts.

---

## Business Objective

To improve the efficiency and effectiveness of the bank's telemarketing campaigns by predicting which customers are likely to subscribe to a term deposit. Accurate predictions can help the bank:

- Focus efforts on high-potential clients
- Reduce the number of unnecessary contact attempts
- Improve campaign ROI

---

## Dataset

**Source**: UCI Machine Learning Repository  
**File Used**: `bank-additional-full.csv`  
**Target Variable**: `y` — whether the client subscribed to a term deposit (`yes` or `no`)

**Selected Features for Modeling**:
- Demographic: `age`, `job`, `marital`, `education`
- Financial: `housing`, `loan`
- Campaign: `campaign`, `pdays`, `previous`, `poutcome`
- Economic: `euribor3m`

---

## Workflow Summary

### 🔹 Data Preparation
- Converted target labels to binary format
- One-hot encoded categorical features
- Standardized numeric features
- Split dataset into training and test sets using stratified sampling

### 🔹 Baseline Model
- Dummy classifier using the most frequent class
- Metrics: High accuracy due to class imbalance, but poor recall and F1-score

### 🔹 Models Compared
- Logistic Regression
- K-Nearest Neighbors
- Decision Tree
- Support Vector Machine

### 🔹 Model Evaluation Metrics
- Accuracy
- Precision
- Recall
- F1 Score

### 🔹 Model Tuning
- Performed hyperparameter tuning using GridSearchCV on Decision Tree
- Improved recall and F1-score through feature expansion and optimization

---

## Key Findings

- Most clients did not subscribe to a term deposit, creating a class imbalance.
- Logistic Regression and SVM had competitive accuracy but low recall by default.
- The Decision Tree model, after tuning, offered the best balance between precision and recall.
- Including additional features like `euribor3m` and `poutcome` improved model performance.

