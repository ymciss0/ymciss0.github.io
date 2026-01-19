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
AI-powered skincare recommendation system using product metadata, reviews, and medical knowledge to match users with best products tending to their dermatological needs. Direct [Link to SkinWise chatbot](https://huggingface.co/spaces/kshamaasuresh/skincare-agent)

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

<!-- Thumbnail that triggers modal -->
<div class="pdf-thumbnail">
  <img src="/assets/images/skinwise_pres_thumbnail.png" alt="View Presentation" style="cursor: pointer;" onclick="openPDFModal()">
  <p><em>Click to view full presentation</em></p>
</div>

<!-- Modal -->
<div id="pdfModal" class="modal">
  <div class="modal-content">
    <span class="close" onclick="closePDFModal()">&times;</span>
    <iframe src="/assets/pdfs/skinwise_pres.pdf" width="100%" height="600px"></iframe>
  </div>
</div>

<style>
.modal {
  display: none;
  position: fixed;
  z-index: 1000;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0,0,0,0.8);
}

.modal-content {
  position: relative;
  background-color: #fefefe;
  margin: 2% auto;
  padding: 20px;
  width: 90%;
  max-width: 1000px;
  height: 90vh;
}

.close {
  color: #aaa;
  float: right;
  font-size: 28px;
  font-weight: bold;
  cursor: pointer;
}

.close:hover { color: #000; }
</style>

<script>
function openPDFModal() {
  document.getElementById('pdfModal').style.display = 'block';
}

function closePDFModal() {
  document.getElementById('pdfModal').style.display = 'none';
}

// Close on outside click
window.onclick = function(event) {
  const modal = document.getElementById('pdfModal');
  if (event.target == modal) {
    modal.style.display = 'none';
  }
}
</script>