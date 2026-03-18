 # Credit Risk Prediction using Machine Learning

## Overview

This project builds a machine learning pipeline to predict whether a borrower will default on a loan. Using a credit risk dataset, multiple machine learning models were trained and evaluated to identify high-risk borrowers.

The goal is to assist financial institutions in making better lending decisions by estimating the risk associated with each borrower.

---

## Dataset

The dataset used is the **Credit Risk Dataset**, which contains borrower information such as:

* Age
* Income
* Employment length
* Loan amount
* Loan intent
* Home ownership
* Previous default history
* Loan-to-income ratio

### Target Variable

**loan_status** indicates the repayment outcome:

* **0 → Loan repaid (No Default)**
* **1 → Loan defaulted**

---

## Project Pipeline

The project follows a complete end-to-end machine learning workflow:

### 1. Data Cleaning

* Handled missing values
* Created missing indicators

### 2. Feature Engineering

* Created `loan_percent_income` feature
* Encoded categorical variables
* Removed leakage features

### 3. Exploratory Data Analysis

* Univariate analysis
* Bivariate analysis
* Correlation analysis

### 4. Feature Selection

* Removed redundant features
* Analyzed feature importance

### 5. Model Training

* Logistic Regression (baseline)
* Random Forest
* XGBoost

### 6. Model Evaluation

* Accuracy
* Precision
* Recall
* F1 Score
* ROC-AUC
* Precision-Recall Curve

### 7. Hyperparameter Tuning

* Optimized Random Forest parameters

### 8. Threshold Optimization

* Tuned classification threshold to balance precision and recall

### 9. Model Comparison

* Compared all models using metrics and visualizations

## Model Performance

| Model               | Accuracy | Recall | Precision | F1 Score | ROC-AUC   |
| ------------------- | -------- | ------ | --------- | -------- | --------- |
| Logistic Regression | ~0.67    | ~0.81  | ~0.38     | ~0.52    | ~0.82     |
| Random Forest       | ~0.88    | ~0.53  | ~0.91     | ~0.68    | ~0.88     |
| XGBoost             | ~0.86    | ~0.71  | ~0.68     | ~0.69    | **~0.90** |

**XGBoost achieved the best overall performance**, providing strong discrimination and balanced precision-recall tradeoff.

---

## Key Insights

Important factors influencing loan default risk:

* Home ownership status
* Previous default history
* Loan-to-income ratio
* Loan purpose
* Borrower income

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* XGBoost

---

## Conclusion

This project demonstrates a complete machine learning workflow for credit risk prediction. The final XGBoost model effectively identifies high-risk borrowers and can help financial institutions reduce default risk and improve lending decisions.
