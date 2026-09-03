# Loan Approval Prediction using Machine Learning

##  Overview

This project uses Machine Learning to predict whether a loan application will be approved or rejected based on an applicant's financial, personal, employment, and credit-related information.

The project follows a basic end-to-end Machine Learning workflow, including data exploration, preprocessing, feature engineering, model training, and evaluation.

---

##  Objective

The objective of this project is to build and compare Machine Learning classification models for predicting loan approval.

The target variable is:

- `1` → Loan Approved
- `0` → Loan Rejected

---

##  Dataset

The dataset contains **1,000 loan application records** with information related to applicants and their loan applications.

Some of the features include:

- Applicant Income
- Coapplicant Income
- Employment Status
- Age
- Marital Status
- Dependents
- Credit Score
- Existing Loans
- Debt-to-Income Ratio
- Savings
- Collateral Value
- Loan Amount
- Loan Term
- Loan Purpose
- Property Area
- Education Level
- Gender
- Employer Category

The target variable is:

`Loan_Approved`

---

## Project Workflow

The project follows these steps:

1. Data loading and understanding
2. Handling missing values
3. Exploratory Data Analysis (EDA)
4. Removing unnecessary features
5. Encoding categorical variables
6. Correlation analysis
7. Train-test split
8. Feature scaling
9. Feature engineering
10. Model training
11. Model evaluation and comparison

---

##  Data Preprocessing

The following preprocessing steps were performed:

- Missing numerical values were handled using mean imputation.
- Missing categorical values were handled using the most frequent value.
- `Applicant_ID` was removed from the dataset.
- Categorical features were encoded using Label Encoding and One-Hot Encoding.
- Features were standardized using `StandardScaler`.

---

##  Exploratory Data Analysis

Exploratory Data Analysis was performed to better understand the dataset and relationships between features.

The analysis included:

- Dataset inspection
- Missing value analysis
- Summary statistics
- Loan approval distribution
- Feature distributions
- Correlation heatmap

---

## Feature Engineering

Additional features were created to experiment with possible relationships in the data:

- `DTI_Ratio_sq`
- `Credit_Score_sq`
- Log transformation of Applicant Income

---

## Machine Learning Models

The following classification models were trained and evaluated:

- Logistic Regression
- K-Nearest Neighbors (kNN)
- Gaussian Naive Bayes

---

##  Model Evaluation

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1 Score
- Confusion Matrix

### Final Model Results

| Model | Accuracy | Precision | Recall | F1 Score |
|---|---:|---:|---:|---:|
| Logistic Regression | 88% | 78.46% | 83.61% | 80.95% |
| kNN | 78.5% | 67.31% | 57.38% | 61.95% |
| Gaussian Naive Bayes | 86% | 81.13% | 70.49% | 75.44% |

---

##  Results

Based on the evaluation results:

- **Logistic Regression achieved the highest accuracy and recall.**
- **Gaussian Naive Bayes achieved the highest precision.**
- **Logistic Regression achieved the highest F1 Score among the tested models.**

Overall, Logistic Regression performed strongly on this dataset, while Gaussian Naive Bayes showed the highest precision for loan approval predictions.

---

##  Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

---

##  Project Structure
```text
loan-approval-prediction/
│
├── data/
│   └── loan_approval_data.csv
│
├── notebooks/
│   └── loan_approval_prediction.ipynb
│
├── README.md
├── requirements.txt
└── .gitignore