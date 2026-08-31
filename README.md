# MSDS422 Final Project - Credit Card Fraud Detection
**Northwestern University** | MSDS422

## Team
Andrea Scherben, Shelagh Haney, Ryenn McAdory 

## Problem
Undetected fraud costs issuers money directly, plus chargeback and operational costs and damage to customer trust. On the flip side, overly aggressive fraud rules cause false declines that annoy legit customers and cost sales. The goal is a model-based approach that catches meaningfully more fraud than current rules while keeping false positives manageable.

## Dataset
Credit Card Fraud Detection dataset (Kaggle) - (https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud) — 284,807 real transactions from European cardholders over a two-day window in September 2013. Only 492 (0.173%) are confirmed fraud, so this is an extremely imbalanced classification problem. Features are PCA-transformed (V1–V28) for confidentiality; only Time and Amount are in their original form.

## Models Compared
| Model | Precision | Recall | PR-AUC |
|---|---|---|---|
| **K-Nearest Neighbors** | **0.908** | **0.806** | **0.841** |
| Linear Discriminant Analysis | 0.823 | 0.806 | 0.708 |
| Logistic Regression | 0.056 | 0.908 | 0.714 |
| Quadratic Discriminant Analysis | 0.061 | 0.878 | 0.144 |

- **KNN** achieved the best balance of precision and recall at the default 0.5 threshold (PR-AUC: 0.841; Precision: 0.908; Recall: 0.806)
- After tuning the decision threshold from 0.5 to 0.159, KNN caught 88.8% of fraud (87 of 98 fraud cases) while flagging 64 legitimate transactions for review.

## Tools
Python 3 · scikit-learn · pandas · NumPy · Matplotlib · Seaborn

## References
- Kaggle Dataset: Machine Learning Group – ULB. “Credit Card Fraud Detection.” https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud
- Dal Pozzolo, A., Caelen, O., Johnson, R. A., & Bontempi, G. (2015). “Calibrating Probability with Undersampling for Unbalanced Classification.” IEEE Symposium Series on Computational Intelligence (SSCI).
