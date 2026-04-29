# Statistical Analysis and Market Basket

## Overview
This repo groups five analytics projects covering regression modeling, dimensionality reduction, statistical hypothesis testing, and market basket analysis. It demonstrates applied statistics and machine learning across health insurance, housing, and retail transaction datasets.

## Academic Context
Completed during my M.S. in Data Analytics at Western Governors University (WGU), then packaged here as a public portfolio project. Screenshots from the original written submissions are preserved in `assets/task2-report-extracts/` and `assets/task3-report-extracts/`.

## What It Shows
- linear regression modeling and coefficient interpretation
- logistic regression for binary classification
- PCA for dimensionality reduction and variance explanation
- exploratory data analysis
- statistical testing and interpretation
- transaction encoding for basket analysis
- association rule mining and business interpretation

## Included Files
- `notebooks/linear_regression.ipynb`
- `notebooks/logistic_regression.ipynb`
- `notebooks/pca_analysis.ipynb`
- `notebooks/statistical_tests.ipynb`
- `notebooks/market_basket.ipynb`
- `data/housing_data.csv`
- `data/Health Insurance Dataset.xlsx`
- `data/megastore_transactions.csv`
- `requirements.txt`

## Results

- One-way ANOVA on BMI by region found a statistically significant regional difference with `F = 39.4069` and `p = 0.0000`.
- Mann-Whitney U testing for smoker status versus medical charges produced `p = 4.58e-129`, strongly supporting a meaningful cost difference between smokers and non-smokers.
- The market basket analysis surfaced top Apriori rules with support of `0.011338`, perfect confidence of `1.0`, and lift of `88.2`.
- The strongest retail rules linked themed children's gift items, making the repo a good example of translating association rules into bundling and cross-sell strategy.

## Selected Visuals

![Statistical testing report visual](assets/task2-report-extracts/report_image_01.png)

![Market basket report visual](assets/task3-report-extracts/report_image_01.png)
