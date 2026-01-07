---
title: "Heart Disease Prediction: Comparative Analysis"
excerpt: "Compared Naive Bayes and regularized regression models, achieving 83.5% accuracy with Ridge regression on UCI medical dataset."
header:
  teaser: /assets/images/heart-disease-teaser.png
tags:
  - Classification
  - Medical ML
  - Ridge Regression
  - Feature Engineering
github: https://github.com/ymciss0/Applied_Machine_Learning/tree/main
---

## Overview
Comparative analysis of three classification approaches for predicting heart disease using UCI dataset with 303 patients and 14 clinical attributes.

## Key Results
- **83.5% accuracy** with Ridge Regression (alpha=1) - best performer
- **90.2% AUC** demonstrating excellent probability calibration
- **81.3% accuracy** with Bernoulli Naive Bayes - strong second place
- LASSO failed completely (53.8% accuracy) due to over-regularization

## Technical Approach

**Data Preprocessing:**
- Winsorization for outliers (cholesterol, ST depression)
- Feature engineering: Medical guideline-based binning (blood pressure, cholesterol, age groups)
- 70-30 train-test split with stratification

**Models Compared:**
- Bernoulli Naive Bayes (4 alpha values tested)
- Gaussian Naive Bayes
- Linear Regression variants (regular, Ridge, LASSO)

**Best Configuration:**
Ridge Regression with alpha=1 achieved optimal balance—48.2% R², low MSE (0.129), and superior discriminative ability.

## Technical Stack
Python • scikit-learn • pandas • NumPy 

## What I Learned
Feature engineering with domain knowledge (CDC guidelines for blood pressure, Johns Hopkins cholesterol ranges) significantly improved model performance. The unexpected LASSO failure highlighted the importance of careful hyperparameter tuning—even minimal regularization can over-penalize in certain feature spaces. Ridge's success demonstrates that proper regularization balance is more valuable than complex feature selection.

[View Code on GitHub](https://github.com/ymciss0/Applied_Machine_Learning/blob/main/project_1/heart_disease_classification_final.ipynb){: .btn .btn--primary}