# 🏦 Loan Approval Prediction

## Overview

This project develops a machine learning classification system to predict whether a loan application will be approved based on applicant and loan characteristics.

The analysis compares multiple classification algorithms and evaluates their performance using several metrics before selecting the strongest-performing model.

## 🎯 Objective

The main objective is to predict the loan approval outcome using information available in a loan application.

The project explores whether applicant characteristics such as:

* Credit history
* Applicant income
* Co-applicant income
* Loan amount
* Loan term
* Education
* Employment status
* Property area

can be used to predict loan approval.

## 📊 Dataset

The project uses a loan application dataset containing **614 observations and 13 variables**.

The dataset includes demographic, financial, employment, and loan-related information.

The target variable is:

* `Loan_Status` — approved or rejected

## 🔍 Exploratory Analysis

The analysis begins by examining the structure of the dataset, missing values, categorical variables, and numerical distributions.

![Exploratory Analysis](https://github.com/vguimaraeslima-ctrl/projects/blob/8a30ffa2b0feaf683d8b78fe3dda23e655c70b50/loan-approval-prediction/screenshots/03-exploratory-analysis.png)

The exploratory analysis provides an overview of the characteristics of the applicants and the distribution of loan approval outcomes.

## 🧹 Data Preparation

The data preparation process includes handling missing values, separating numerical and categorical variables, and preparing the features for machine learning.

A preprocessing pipeline was implemented using:

* `SimpleImputer`
* `StandardScaler`
* `OneHotEncoder`
* `ColumnTransformer`

The dataset was divided into training and test sets using stratified sampling.

![Data Preparation](https://github.com/vguimaraeslima-ctrl/projects/blob/0ba3f9731d6bab7502548b93aada0f98447d7472/loan-approval-prediction/screenshots/04-data-preparation.png)

## 🤖 Machine Learning Models

Four classification approaches were evaluated:

* Logistic Regression
* Random Forest
* Tuned Random Forest
* LightGBM

Hyperparameter tuning was performed for the Random Forest model using `GridSearchCV`.

## 📈 Model Performance

| Model                   |  Accuracy | Precision |    Recall |        F1 |   ROC-AUC |
| ----------------------- | --------: | --------: | --------: | --------: | --------: |
| **Logistic Regression** | **86.2%** |     84.0% | **98.8%** | **90.8%** | **85.2%** |
| Random Forest           |     82.1% |     84.6% |     90.6% |     87.5% |     78.6% |
| Tuned Random Forest     |     82.1% |     83.2% |     92.9% |     87.8% |     79.0% |
| LightGBM                |     80.5% | **86.7%** |     84.7% |     85.7% |     79.9% |

### Model selection

Logistic Regression achieved the strongest overall performance on the test set.

It achieved:

* **86.2% accuracy**
* **84.0% precision**
* **98.8% recall**
* **90.8% F1-score**
* **85.2% ROC-AUC**

The result is particularly interesting because the simpler Logistic Regression model outperformed the tree-based and boosting approaches evaluated in this project.

![Model Comparison](https://raw.githubusercontent.com/vguimaraeslima-ctrl/projects/machine-learning/loan-approval-prediction/screenshots/05-model-comparison.png)

## 📉 ROC Curve Comparison

The ROC curve comparison provides another view of the models' ability to distinguish between approved and rejected loan applications.

![ROC Curve Comparison](https://raw.githubusercontent.com/vguimaraeslima-ctrl/projects/machine-learning/loan-approval-prediction/screenshots/06-roc-curve-comparison.png)

Logistic Regression achieved the highest ROC-AUC among the evaluated models at **0.852**.

## 🔎 Feature Importance

Feature importance analysis was used to identify the variables that contributed most strongly to the Random Forest predictions.

![Feature Importance](https://raw.githubusercontent.com/vguimaraeslima-ctrl/projects/machine-learning/loan-approval-prediction/screenshots/07-feature-importance.png)

The most influential variables included:

* Credit History
* Applicant Income
* Loan Amount
* Co-applicant Income
* Loan Term

This provides an additional layer of interpretability and helps connect the machine learning results to the characteristics of the loan applications.

## 🔬 Workflow

```text
Data Loading
     ↓
Data Cleaning
     ↓
Exploratory Analysis
     ↓
Feature Preparation
     ↓
Preprocessing Pipeline
     ↓
Train/Test Split
     ↓
Model Training
     ↓
Hyperparameter Tuning
     ↓
Model Comparison
     ↓
Final Model Selection
     ↓
Feature Interpretation
```

## 🛠️ Technologies

* Python
* Pandas
* NumPy
* Scikit-learn
* LightGBM
* Matplotlib
* Seaborn
* SHAP
* Jupyter Notebook

## 📁 Project Structure

```text
loan-approval-prediction/
│
├── README.md
├── VitorLimaML.ipynb
│
└── screenshots/
    ├── 01-data-loading.png
    ├── 02-data-cleaning.png
    ├── 03-exploratory-analysis.png
    ├── 04-data-preparation.png
    ├── 05-model-comparison.png
    ├── 06-roc-curve-comparison.png
    └── 07-feature-importance.png
```

## 💡 Key Takeaways

This project demonstrates an end-to-end supervised machine learning workflow for a binary classification problem.

Key skills demonstrated include:

* Data cleaning and exploratory analysis
* Numerical and categorical feature preprocessing
* Machine learning pipeline construction
* Model comparison
* Hyperparameter tuning with cross-validation
* Classification model evaluation
* ROC-AUC analysis
* Feature importance and model interpretation

One of the main findings was that **Logistic Regression provided the strongest overall performance** on this dataset, outperforming the more complex ensemble models evaluated.
