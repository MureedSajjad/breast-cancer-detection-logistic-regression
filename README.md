# breast-cancer-detection-logistic-regression
Logistic Regression model for breast cancer diagnosis using the Wisconsin dataset. Achieves 98.25% accuracy and 1.00 ROC-AUC. Includes confusion matrix, ROC curve, and feature importance analysis.
# 🔬 Breast Cancer Diagnosis Using Logistic Regression

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](YOUR_COLAB_LINK_HERE)

**Author:** Mureed Sajjad | 2k23/DS/77 | University of Sindh
**Course:** Machine Learning

---

## Overview

This project applies **Logistic Regression** to predict whether a breast cancer tumor is **Malignant** or **Benign** using 30 cell nucleus features extracted from Fine Needle Aspiration (FNA) biopsy images.

The key insight of this project is that in medical AI, **recall matters more than accuracy** — missing a cancer (False Negative) is far more dangerous than a false alarm (False Positive).

## Dataset

**Wisconsin Breast Cancer Dataset** (built into scikit-learn)
- 569 samples: 357 Benign, 212 Malignant
- 30 numerical features from FNA biopsy images
- No missing values — clean, tabular data

## Results

| Metric | Value |
|--------|-------|
| **Test Accuracy** | **98.25%** |
| **ROC-AUC** | **1.00** |
| Malignant Recall | 0.98 |
| Malignant Precision | 0.98 |
| False Negatives | 1 |
| False Positives | 1 |

## Pipeline

1. Load Wisconsin Breast Cancer dataset
2. Visualize class distribution
3. Train/Test split (80/20, stratified)
4. Feature scaling (StandardScaler)
5. Train Logistic Regression (`max_iter=10000`)
6. Evaluate: accuracy, classification report, confusion matrix
7. Plot: ROC curve, feature importance, prediction distribution

## Why Logistic Regression?

- **Probabilistic output** — doctors need risk scores, not just labels
- **Interpretable coefficients** — clinicians can trust and understand the model
- **Gold standard in medical research** — used in thousands of PubMed papers
- **Ideal for small, clean, tabular data** — no overfitting on 569 samples
- **Exceptional results** — 98.25% accuracy, 1.00 ROC-AUC

## Clinical Insight

> 4 False Negatives in 114 test samples means the model would miss a small proportion of actual cancers. In a real deployment, the decision threshold would be tuned lower (e.g., 0.3) to prioritize catching all cancers, even at the cost of more false alarms.

## Repository Structure
```
breast-cancer-logistic-regression/
│
├── README.md                          ← You are here
├── Breast_Cancer_Logistic_Regression.ipynb   ← Main notebook (pre-run)
├── requirements.txt                   ← Dependencies
└── presentation.pdf                   ← Class presentation slides
```

## Installation
```bash
pip install numpy pandas matplotlib seaborn scikit-learn
```

Or open directly in Google Colab (no setup required): [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](YOUR_COLAB_LINK_HERE)

## Technologies

- Python 3.x
- scikit-learn (dataset + model)
- pandas, numpy (data manipulation)
- matplotlib, seaborn (visualization)

---

*"Early detection through data science can save lives" — Mureed Sajjad*
