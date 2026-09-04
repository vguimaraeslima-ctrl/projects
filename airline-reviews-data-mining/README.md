# ✈️ Airline Reviews & Ratings — Data Mining Analysis

## Overview

This project explores an airline reviews and ratings dataset from Kaggle to identify patterns in customer satisfaction and relationships between different aspects of the passenger experience.

The analysis focuses on data quality, feature selection, customer service ratings, and relationships between service attributes.

## 🎯 Objective

The main objective is to explore how different aspects of the airline experience relate to customer ratings.

The analysis focuses on variables such as:

- Seat Comfort
- Cabin Staff Service
- Ground Service
- Food & Beverages
- WiFi & Connectivity
- Inflight Entertainment
- Value For Money
- Recommended

The project also examines unusual observations and outliers that may represent specific customer experiences.

## 📊 Dataset

The dataset contains **3,290 airline review records and 15 variables**.

It includes information about:

- Aircraft type
- Traveller type
- Country
- Route
- Seat type
- Customer service ratings
- Overall value for money
- Recommendation status

The ratings are generally measured on a **1–5 scale**, where higher values represent more positive customer evaluations.

## 🔍 Data Exploration

The analysis begins by examining the dataset structure, variable types, missing values, and descriptive statistics.

![Dataset Loading](https://raw.githubusercontent.com/vguimaraeslima-ctrl/projects/data-mining/airline-reviews-data-mining/screenshots/01-data-loading.png)

The dataset contains both categorical and numerical variables, with missing values present in several service-rating fields.

![Data Quality](https://raw.githubusercontent.com/vguimaraeslima-ctrl/projects/data-mining/airline-reviews-data-mining/screenshots/02-data-quality.png)

## 🧹 Data Preparation

Duplicate records were identified and removed before selecting the variables used for the analysis.

The selected variables focus on customer experience and include:

- Seat Comfort
- Cabin Staff Service
- Ground Service
- Food & Beverages
- Recommended
- Seat Types
- Value For Money

![Feature Selection](https://raw.githubusercontent.com/vguimaraeslima-ctrl/projects/data-mining/airline-reviews-data-mining/screenshots/03-feature-selection.png)

Missing ratings were retained rather than replacing them with zero, since zero is outside the 1–5 rating scale and could distort the distribution of customer satisfaction scores.

## 📈 Relationship Analysis

A key part of the analysis examines the relationship between **Value For Money** and **Food & Beverages** ratings.

![Value For Money Analysis](https://raw.githubusercontent.com/vguimaraeslima-ctrl/projects/data-mining/airline-reviews-data-mining/screenshots/04-value-for-money-analysis.png)

The boxplot shows a positive relationship between the two rating dimensions: higher Value For Money ratings tend to be associated with higher Food & Beverages ratings.

The analysis also highlights outliers. These observations are important because they can represent passengers who had a particularly different experience from the general pattern.

## 💡 Key Insights

The analysis highlights several characteristics of the dataset:

- Customer ratings cover multiple dimensions of the airline experience.
- Service-related ratings generally follow a positive relationship with perceived value.
- **Food & Beverages** and **Value For Money** show a noticeable relationship.
- Outliers provide useful information about individual customer experiences and should not automatically be removed.
- Missing values require careful treatment because the rating scale does not use zero as a valid rating.

## 🔬 Workflow

```text
Dataset Loading
      ↓
Data Structure & Quality Analysis
      ↓
Missing Value Analysis
      ↓
Duplicate Detection & Removal
      ↓
Feature Selection
      ↓
Exploratory Analysis
      ↓
Relationship Analysis
      ↓
Outlier Interpretation
      ↓
Key Insights
