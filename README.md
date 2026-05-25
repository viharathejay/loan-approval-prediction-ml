# Loan Approval Prediction — Machine Learning

## Overview
This project applies machine learning techniques to predict loan approval status and estimate the maximum loan amount offered to approved clients. The project is structured across three Jupyter notebooks covering data preprocessing, classification modelling and regression modelling using the Python Scikit-learn library.

---

## Research Questions
- Does machine learning have the potential to assist bankers and finance analysts in predicting which client can be approved a loan?
- Does machine learning have the potential to assist bankers in predicting the Maximum Loan Amount offered to clients who were approved a loan?

---

## Dataset
The dataset contains loan application records with the following key variables:

- Age, Income, Employment Length, Education Qualifications
- Home Ownership, Loan Intent, Loan Amount, Loan Interest Rate
- Loan-to-Income Ratio, Payment Default on File, Credit History Length
- Loan Approval Status (Classification Target)
- Maximum Loan Amount (Regression Target)

---

## Project Structure

### Notebook 1 — Data Understanding and Preprocessing
- Data exploration and visualisation
- Handling missing values using mean and mode imputation
- Standardising inconsistent categorical labels
- Outlier detection and removal using the IQR method
- Label encoding of categorical variables
- Creating two prepared datasets for classification and regression

### Notebook 2 — Classification Modelling and Hyperparameter Tuning
- Building three classification models — Logistic Regression, Naive Bayes and K-Nearest Neighbours
- Evaluating models using Accuracy, Precision, Recall, F1-Score and AUC-ROC
- Finding optimal k value using error rate plot
- Selecting the best model based on accuracy
- Hyperparameter tuning using GridSearchCV with n_neighbors and distance metric optimisation

### Notebook 3 — Regression Decision Trees and Ensemble Learners
- Building a soft voting ensemble classifier combining KNN and Logistic Regression
- Building two Decision Tree regression models — DT1 fully grown and DT2 pruned to four levels
- Evaluating regression models using MAE, MSE and R2
- Predicting Maximum Loan Amount for a new approved client

---

## Models Used

| Model | Task | Best Result |
|---|---|---|
| Logistic Regression | Classification | Accuracy: 0.89 |
| Naive Bayes | Classification | Accuracy: 0.86 |
| K-Nearest Neighbours (k=9) | Classification | Accuracy: 0.91 |
| KNN + LR Voting Ensemble | Classification | Accuracy: 0.91, AUC: 0.90 |
| GridSearchCV Tuned KNN | Classification | Accuracy: 0.92, AUC: 0.93 |
| DT1 Fully Grown | Regression | R2: 0.9976, MAE: 650 |
| DT2 Pruned (max_depth=4) | Regression | R2: 0.8515, MAE: 7917 |

---

## Technologies Used

- Python 3
- Pandas
- NumPy
- Scikit-learn
- Plotly Express
- Matplotlib
- Google Colab

---

## Key Findings

- KNN with k=9 was identified as the best classification model achieving an accuracy of 0.91 and AUC of 0.87
- GridSearchCV tuning identified optimal parameters of n_neighbors=24 and metric=Manhattan improving AUC to 0.93
- DT1 fully grown was identified as the best regression model achieving R2 of 0.9976 and MAE of 650
- The predicted Maximum Loan Amount for Client 60256 using DT1 was 97,996

---

## How to Run

1. Clone or download this repository
2. Upload the loan applications dataset to Google Colab
3. Run Notebook 1 first to generate the prepared datasets
4. Run Notebook 2 for classification modelling
5. Run Notebook 3 for ensemble learning and regression modelling

---

## Author
Vihara Thejaka Kularathna

## Peer Reviewer
Muhammad Abdullah
