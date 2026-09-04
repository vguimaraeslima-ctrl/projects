# 🚗 Vehicle Emissions — Statistical Analysis

## Overview

This project applies statistical analysis to a dataset of Canadian vehicles to investigate the factors associated with CO₂ emissions.

The analysis explores relationships between vehicle characteristics, fuel consumption, and emissions, with a particular focus on engine size and fuel type.

## 🎯 Objective

The main objectives are to:

- Explore the structure and characteristics of the vehicle dataset
- Analyze relationships between vehicle characteristics and CO₂ emissions
- Measure the correlation between engine size and CO₂ emissions
- Compare CO₂ emissions between hybrid and gasoline vehicles
- Use statistical hypothesis testing to determine whether the difference in mean emissions is statistically significant

## 📊 Dataset

The dataset contains **7,385 vehicle records and 12 variables**.

Key variables include:

- `Make`
- `Model`
- `Vehicle_Class`
- `Engine_Size(L)`
- `Cylinders`
- `Transmission`
- `Fuel_Type`
- `Fuel_Consumption_City_(L/100_km)`
- `Fuel_Consumption_Hwy_(L/100_km)`
- `Fuel_Consumption_Comb_(L/100_km)`
- `Fuel_Consumption_Comb_(mpg)`
- `CO2_Emissions(g/km)`

The main outcome analyzed in this project is **CO₂ emissions measured in grams per kilometer**.

## 🔍 Data Overview

The analysis begins by examining the dataset structure, variables, data types, and descriptive statistics.

![Data Loading](https://raw.githubusercontent.com/vguimaraeslima-ctrl/projects/statistics-analysis/vehicle-emissions-statistics/screenshots/01-data-loading.png)

The dataset contains **7,385 observations across 12 variables**, with both categorical and numerical features.

![Data Overview](https://raw.githubusercontent.com/vguimaraeslima-ctrl/projects/statistics-analysis/vehicle-emissions-statistics/screenshots/02-data-overview.png)

## 📈 Descriptive Statistics

Descriptive statistics were calculated for key numerical variables including engine size, number of cylinders, fuel consumption, and CO₂ emissions.

![Descriptive Statistics](https://raw.githubusercontent.com/vguimaraeslima-ctrl/projects/statistics-analysis/vehicle-emissions-statistics/screenshots/03-descriptive-statistics.png)

The mean CO₂ emission level in the dataset is approximately **250.58 g/km**.

## 🔗 Engine Size and CO₂ Emissions

A strong positive relationship was identified between engine size and CO₂ emissions.

The correlation coefficient was:

**r = 0.851**

This indicates a strong positive linear association: vehicles with larger engines tend to produce higher CO₂ emissions.

![Engine Size Correlation](https://raw.githubusercontent.com/vguimaraeslima-ctrl/projects/statistics-analysis/vehicle-emissions-statistics/screenshots/04-engine-size-correlation.png)

## 🧪 Hypothesis Testing — Hybrid vs Gasoline

An independent two-sample t-test was used to compare the mean CO₂ emissions of hybrid and gasoline vehicles.

### Hypotheses

**H₀:** There is no difference in mean CO₂ emissions between hybrid and gasoline vehicles.

**H₁:** There is a difference in mean CO₂ emissions between hybrid and gasoline vehicles.

Using a significance level of **α = 0.05**, the test produced:

| Metric | Result |
|---|---:|
| Hybrid mean | 235.12 g/km |
| Gasoline mean | 266.04 g/km |
| t-statistic | -22.38 |
| p-value | < 0.001 |

Because the p-value is below 0.05, the null hypothesis is rejected.

The results provide strong statistical evidence that the mean CO₂ emissions differ between hybrid and gasoline vehicles in this dataset.

![Hybrid vs Gasoline Test](https://raw.githubusercontent.com/vguimaraeslima-ctrl/projects/statistics-analysis/vehicle-emissions-statistics/screenshots/05-hybrid-vs-gasoline-test.png)

## 💡 Key Findings

The analysis highlights three main findings:

- Engine size has a **strong positive correlation** with CO₂ emissions (`r = 0.851`).
- The average CO₂ emissions for hybrid vehicles were lower than for gasoline vehicles in this dataset.
- The difference in mean emissions between hybrid and gasoline vehicles was **statistically significant** based on the independent two-sample t-test.

## 🔬 Workflow

```text
Data Loading
     ↓
Dataset Structure & Data Types
     ↓
Descriptive Statistics
     ↓
Exploratory Analysis
     ↓
Correlation Analysis
     ↓
Hypothesis Formulation
     ↓
Independent Two-Sample T-Test
     ↓
Statistical Interpretation
     ↓
Key Findings
