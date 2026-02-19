# US Renewable Energy Forecasting

A machine learning project analyzing 57 years of US renewable energy production data (1965-2021) and forecasting generation through 2034. Applies clustering, regression, and SVM-based forecasting across solar, wind, hydro, and other renewable sources.

## Overview

This project performs end-to-end analysis of US renewable energy trends:

- **EDA** on 22 features across 57 years from multiple renewable sources
- **Unsupervised learning** to identify temporal energy production eras
- **Supervised learning** for predicting energy generation
- **Forecasting** renewable energy production through 2034

## Key Results

### Clustering
K-Means identified **2-3 distinct temporal periods** in US energy production (silhouette score: 0.881), revealing a clear shift from hydro-dominated generation to rapid solar/wind growth post-2000s.

### Forecasting (SVM Predictions for 2034)

| Energy Source | 2024 (TWh) | 2034 Forecast (TWh) |
|--------------|------------|---------------------|
| Solar | 50.80 | **62.94** |
| Wind | 189.25 | **233.32** |
| Hydro | 282.90 | **285.47** (stable) |

## Dataset

- **57 years** of annual data (1965-2021)
- **22 features** covering solar, wind, hydro, biofuels, geothermal generation and capacity
- **17 source CSV files** from global renewable energy databases
- Integrated with **EIA API** for real-time data access

## Tech Stack

**Python:** pandas, numpy, scikit-learn (KMeans, Decision Trees, Naive Bayes, SVR), matplotlib, seaborn
**R:** arules, arulesViz (Association Rule Mining), hierarchical clustering

## Methods

### Unsupervised Learning
- **K-Means Clustering** (k=2-9, silhouette analysis)
- **Hierarchical Clustering** (cosine distance, complete linkage)
- **Association Rule Mining** (Apriori algorithm in R)

### Supervised Learning
- **Decision Tree Regression** (Solar, Wind, Hydro targets)
- **Naive Bayes Classification** (binned energy generation)
- **SVM Regression** (Linear, RBF, Polynomial kernels)

### Forecasting
- SVM-based extrapolation with polynomial features for 2024-2034 predictions

## Project Structure

```
├── ML_Project_Part-1.ipynb                          # Data wrangling & EDA
├── ML_Project_Part_2_K_Means_Clustering.ipynb       # K-Means analysis
├── ML_Project_Part_2_Hierarchical_Clustering.ipynb  # Hierarchical clustering (R)
├── ML_Project_Part_2_ARM-2.ipynb                    # Association Rule Mining (R)
├── ML_Project_Part_3_Decision_Trees.ipynb           # Decision Tree regression
├── ML_Project_Part_3_Naive_Bayes.ipynb              # Naive Bayes classification
├── ML_Project_Part_4_SVM-2.ipynb                    # SVM regression & forecasting
├── Ml_Project_API.ipynb                             # EIA API integration
├── Initial_data/                                    # 17 source CSV files
├── merged_total_dataset.csv                         # Global merged data
└── merged_usa_dataset.csv                           # US-specific data
```

## How to Run

1. Clone the repository
2. Install dependencies: `pip install pandas numpy scikit-learn matplotlib seaborn`
3. Run notebooks in order (Part 1 -> Part 2 -> Part 3 -> Part 4)
