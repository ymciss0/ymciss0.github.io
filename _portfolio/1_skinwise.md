---
title: "Skinwise: AI-Powered Skincare Recommendation System"
excerpt: "Sentiment analysis pipeline on 581K product reviews achieving 86% accuracy with 46% improvement in negative feedback detection."
header:
  teaser: /assets/images/skinwise-teaser.png
tags:
  - NLP
  - Sentiment Analysis
  - Recommendation Systems
  - Python
github: https://github.com/ymciss0/SkinWise
---

## Overview
AI-powered skincare recommendation system using product metadata, reviews, and medical knowledge to match users with best products tending to their dermatological needs. Direct link to the Chatbot: https://huggingface.co/spaces/kshamaasuresh/skincare-agent

As part of this collaborative project, I performed sentiment analysis on 581K+ reviews from a Sephora product reviews dataset, to identify relevant feedback for product recommendation.

## Sentiment Analysis Key Results
- **86% classification accuracy** using TF-IDF + Logistic Regression
- **46% improvement** in negative feedback detection (61% → 88% precision) from baseline model
- **Multi-platform validated** on 4K additional Ulta reviews
- Automated quality scoring to surface top-5 representative reviews per product

## Technical Stack
Python • scikit-learn • pandas • NumPy • TF-IDF • Logistic Regression

## What I Learned
This project taught me how to extract meaningful signals from noisy user feedback, and practice with Natural Language Processing through TF-IDF implementation. The 46% improvement in detecting negative reviews came from careful handling of class imbalance and optimizing for precision on the minority class.

[View Code on GitHub](https://github.com/ymciss0/SkinWise){: .btn .btn--primary}