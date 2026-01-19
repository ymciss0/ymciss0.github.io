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
- **46% improvement** in negative feedback detection (61% → 88% precision) from baseline model (VADER)
- **Multi-platform validated** on 4K additional Ulta reviews
- Automated quality scoring to surface top-5 representative reviews per product


<!-- Thumbnail -->
<div class="pdf-thumbnail" style="text-align: center; margin: 2em 0;">
  <img src="/assets/images/skinwise_pres_thumbnail.png" 
       alt="View Presentation" 
       style="cursor: pointer; max-width: 400px; border: 2px solid #ddd;" 
       id="pdfThumbnail">
  <p><em>Click to view full presentation</em></p>
</div>

<!-- Modal -->
<div id="pdfModal" style="display: none; position: fixed; z-index: 9999; left: 0; top: 0; width: 100%; height: 100%; background-color: rgba(0,0,0,0.9);">
  <div style="position: relative; background-color: white; margin: 2% auto; padding: 0; width: 90%; max-width: 1000px; height: 90vh;">
    <span id="closeModal" style="position: absolute; top: 10px; right: 20px; color: #333; font-size: 35px; font-weight: bold; cursor: pointer; z-index: 10000;">&times;</span>
    <iframe id="pdfFrame" src="" width="100%" height="100%" style="border: none;"></iframe>
  </div>
</div>

<script>
(function() {
  const modal = document.getElementById('pdfModal');
  const thumbnail = document.getElementById('pdfThumbnail');
  const closeBtn = document.getElementById('closeModal');
  const iframe = document.getElementById('pdfFrame');
  const pdfPath = '/assets/pdfs/skinwise_pres.pdf';

  // Open modal
  thumbnail.addEventListener('click', function() {
    iframe.src = pdfPath;
    modal.style.display = 'block';
    document.body.style.overflow = 'hidden'; // Prevent background scrolling
  });

  // Close modal
  function closeModal() {
    modal.style.display = 'none';
    iframe.src = ''; // Stop loading PDF
    document.body.style.overflow = 'auto'; // Restore scrolling
  }

  closeBtn.addEventListener('click', closeModal);
  
  // Close on background click
  modal.addEventListener('click', function(e) {
    if (e.target === modal) {
      closeModal();
    }
  });

  // Close on Escape key
  document.addEventListener('keydown', function(e) {
    if (e.key === 'Escape' && modal.style.display === 'block') {
      closeModal();
    }
  });
})();
</script>

## Technical Stack
Python • scikit-learn • pandas • NumPy • VADER • TF-IDF • Logistic Regression

## What I Learned
This project taught me how to extract meaningful signals from noisy user feedback, and practice with Natural Language Processing through TF-IDF implementation. The 46% improvement in detecting negative reviews came from careful handling of class imbalance and optimizing for precision on the minority class.

[View Code on GitHub](https://github.com/ymciss0/SkinWise){: .btn .btn--primary}