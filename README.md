# Credit Card Fraud Detection
**MSDS 422 Final Project**
Andrea Scherben, Shelagh Haney, Ryenn McAdory | Northwestern University

## Overview
Machine learning pipeline to detect fraudulent credit card transactions in real time using a dataset of 284,807 transactions (only 0.173% fraud).

## Dataset
[Kaggle – Credit Card Fraud Detection](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)
- 284,807 transactions over 48 hours (September 2013)
- 492 confirmed fraud cases
- 28 PCA-anonymized features + Time + Amount

## Models Compared
| Model | Precision | Recall | PR-AUC |
|---|---|---|---|
| **K-Nearest Neighbors** | **0.908** | **0.806** | **0.841** |
| Linear Discriminant Analysis | 0.823 | 0.806 | 0.708 |
| Logistic Regression | 0.056 | 0.908 | 0.714 |
| Quadratic Discriminant Analysis | 0.061 | 0.878 | 0.144 |

## Key Findings
- **KNN** achieved the best balance of precision and recall (PR-AUC: 0.841)
- After threshold tuning (0.159), KNN caught **88.8% of fraud** with minimal false alarms
- Estimated net benefit: ~$10,300 on the test set alone

## Tools
Python 3 · Google Colab · scikit-learn · pandas · NumPy · Matplotlib · Seaborn

## References
- Kaggle Dataset: Machine Learning Group – ULB. “Credit Card Fraud Detection.” https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud
- Dal Pozzolo, A., Caelen, O., Johnson, R. A., & Bontempi, G. (2015). “Calibrating Probability with Undersampling for Unbalanced Classification.” IEEE Symposium Series on Computational Intelligence (SSCI).
