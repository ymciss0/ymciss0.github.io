---
title: "Bank Marketing Campaign Optimization"
excerpt: "Ensemble ML models achieving 36.9% F1-score on severely imbalanced dataset (11.3% positive class) with 22% improvement over baseline."
header:
  teaser: /assets/images/bank-marketing-teaser.png
tags:
  - Classification
  - Ensemble Methods
  - Imbalanced Data
  - XGBoost
github: https://github.com/ymciss0/Applied_Machine_Learning/tree/main
---

## Overview
Predicted term deposit subscription from bank marketing campaigns using ensemble methods on UCI dataset with 41K+ observations and severe class imbalance.

## Key Results
- **36.9% F1-score** with GBM (vs. 34.8% XGBoost and 30.2% Random Forest baseline)
- **46.4% AUCPR** on severely imbalanced dataset (88.7% negative class)
- Comprehensive evaluation with precision-recall curves, learning curves, and feature importance analysis

## Technical Stack
Python • XGBoost • scikit-learn • GridSearchCV • pandas • Seaborn

## What I Learned
Handling severe class imbalance requires careful metric selection—accuracy was misleading at 88.7% (predict all negatives), so I optimized for F1-score and AUCPR. The breakthrough came from proper class weighting and extensive hyperparameter tuning with 5-fold cross-validation.

[View Code on GitHub](https://github.com/ymciss0/Applied_Machine_Learning/blob/main/project_2/term_deposit_subscription_prediction.ipynb){: .btn .btn--primary}