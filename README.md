# Predicting Stroke Risk from Health Indicators

**Authors:** Shree Krishna M.S Basnet, Renan  
**Supervisor:** Dr. Cohen  
**Date:** December 2025

## 📌 Project Overview
Stroke is a leading cause of mortality and disability worldwide. This project analyzes routine health indicators (such as age, hypertension, and glucose levels) to predict stroke risk. We compare interpretable **Logistic Regression** models against complex **Machine Learning algorithms** (Random Forest, GBM, SVM).

## 🚩 The Challenge: Class Imbalance
A major challenge in medical prediction is **class imbalance**—stroke cases are rare (~5% of the data).
* **Initial Results:** Standard models achieved high accuracy (~94%) but failed to detect actual strokes (**Sensitivity ≈ 2%**).
* **The Solution:** We implemented **SMOTE** (Synthetic Minority Over-sampling Technique) and **ROSE** to balance the training data.

## 🚀 Key Results
Addressing the imbalance transformed the model's diagnostic utility:
* **Sensitivity Improvement:** Improved from **~2%** to **~60-80%** using SMOTE/ROSE.
* **Top Performers:** Random Forest and Gradient Boosted Machines (GBM) trained with SMOTE provided the best balance of predictive power and reliability.
* **Risk Factors:** Age, Hypertension, and Average Glucose Level were confirmed as the strongest independent predictors.

## 📂 Repository Contents
* **`report.html`**: The full technical report containing code, visualizations, and detailed analysis.
* **`stroke_slides.html`**: Presentation slides summarizing the methodology and findings.
* **`report.qmd` / `stroke_slides.qmd`**: Source Quarto files for reproducibility.
* **`references.bib`**: Bibliography file.

## 💻 How to Run
1. Clone this repository.
2. Ensure you have **R** and **Quarto** installed.
3. Install required R packages:
   ```r
   install.packages(c("tidyverse", "caret", "pROC", "themis", "randomForest", "gbm"))

