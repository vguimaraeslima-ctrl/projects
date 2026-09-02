# ⚽ Football Match Outcome Prediction

## Overview

This project explores the use of machine learning to predict football match outcomes using historical match, team, player and contextual data.

The objective is to investigate whether a combination of performance statistics and match-related features can provide useful predictions of match outcomes.

---

## 🎯 Objective

The main objective is to predict the outcome of a football match based on information available in the dataset.

The project explores:

* Data preparation
* Feature selection and engineering
* Exploratory analysis
* Machine learning classification
* Model evaluation
* Feature importance
* Prediction performance

---

## 📊 Dataset & Features

The dataset contains football-related information covering team and player performance as well as contextual match information.

Examples of variables explored include:

* Goals
* Assists
* Shots
* Minutes played
* Expected goals (xG)
* Team performance
* Player statistics
* Attendance
* Weather
* Temperature
* Travel distance
* Disciplinary statistics
* Betting-related information

### Data overview

![Dataset and analysis](screenshots/overview.png)

---

## 🔧 Methodology

The project follows the following workflow:

```text
Historical Football Data
          ↓
Data Preparation
          ↓
Feature Selection / Engineering
          ↓
Exploratory Analysis
          ↓
Model Training
          ↓
Model Evaluation
          ↓
Prediction
```

### Feature engineering

A range of football performance and contextual variables were incorporated into the modelling process.

![Feature engineering](screenshots/features.png)

---

## 🤖 Machine Learning

The project evaluates machine learning approaches for football match outcome prediction.

The modelling process includes:

* Train/test data preparation
* Feature preprocessing
* Classification models
* Model comparison
* Performance evaluation

### Models

The notebook explores models including:

* Logistic Regression
* Random Forest
* LightGBM

![Model development](screenshots/models.png)

---

## 📈 Results

The final models were evaluated using classification performance metrics including:

* Accuracy
* Precision
* Recall
* F1-score
* ROC-AUC
* Confusion matrix

The current experimental results achieved approximately:

**Accuracy: 66.7%**

**ROC-AUC: 64.8%**

These results should be interpreted in the context of the dataset, feature availability and validation methodology.

![Model results](screenshots/results.png)

---

## 🔍 Key Takeaways

The project demonstrates how football performance and contextual variables can be combined to build a predictive classification model.

The modelling experiments also highlight the difficulty of predicting football outcomes, where uncertainty and a large number of interacting factors make consistently accurate predictions challenging.

---

## ⚠️ Limitations

The results are dependent on the available historical data and selected features.

Football matches are influenced by many factors that may not be completely captured by the dataset, including injuries, tactical changes, player availability and unexpected events.

The reported results therefore should not be interpreted as a guarantee of future match outcomes.

---

## 🛠️ Technologies

* Python
* pandas
* NumPy
* scikit-learn
* LightGBM
* Matplotlib
* Seaborn
* Jupyter Notebook

---

## 📁 Project Structure

```text
football-match-prediction/
│
├── README.md
├── quarter-final head-to-head prediction.ipynb
└── screenshots/
    ├── overview.png
    ├── features.png
    ├── models.png
    └── results.png
```

---

## 📓 Notebook

The complete analysis, modelling process and results are available in:

`quarter-final head-to-head prediction.ipynb`
