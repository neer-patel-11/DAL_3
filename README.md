Name :- Neer Patel

Roll no :- DA25M021

# Fraud Detection – Resampling Methods Analysis

## 📋 Overview
This project evaluates different **resampling strategies** to handle a highly imbalanced fraud-detection dataset.  
The goal is to improve the model’s ability to detect minority (fraud) cases while balancing **precision**, **recall**, and **F1-score**.

---


## 🧮 Methodology
1. **Baseline Model**  
   - Trained a classifier on the original imbalanced dataset.
   - Provided a reference for precision, recall, and F1-score.

2. **Resampling Techniques Tested**  
   - **SMOTE (Synthetic Minority Over-sampling Technique)**  
     Generates synthetic minority samples to balance the dataset.
   - **CBO (Clustering-Based Oversampling)**  
     Applies clustering to create realistic synthetic samples only in dense regions.
   - **CBU (Clustering-Based Undersampling)**  
     Reduces majority-class instances using clustering to preserve diversity.

3. **Evaluation Metrics**  
   - **Precision**: Percentage of predicted frauds that are actually fraud.
   - **Recall**: Percentage of real frauds correctly identified.
   - **F1-score**: Harmonic mean of precision and recall.

---

## 📊 Key Results

### Minority Class Performance

| Method | Precision | Recall | F1-score |
|:------:|:--------:|:------:|:-------:|
| **Baseline** | **0.85** | 0.63 | 0.72 |
| **SMOTE**   | 0.06 | **0.89** | 0.11 |
| **CBO**     | 0.11 | 0.88 | 0.20 |
| **CBU**     | 0.04 | 0.89 | 0.08 |

---

**Insights:**
- **Baseline**: Excellent precision but low recall—many frauds go undetected.
- **SMOTE**: Recall jumps to 0.89 but precision collapses to 0.06, causing excessive false positives.
- **CBO**: Balances recall (0.88) and precision (0.11) slightly better than SMOTE.
- **CBU**: High recall but worst precision (0.04) due to aggressive undersampling.

---
