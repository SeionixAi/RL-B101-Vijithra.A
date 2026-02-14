
# Vehicle Insurance Claim Fraud Detection
Data Preprocessing & Visualization

## Dataset Source
Vehicle Insurance Claim Fraud Detection Dataset
link:https://www.kaggle.com/datasets/shivamb/vehicle-claim-fraud-detection
(Row count ~15,400)

---

## Problem Statement
The objective is to predict whether an insurance claim is fraudulent 
based on customer, vehicle, and claim-related attributes.

Target Variable:
FraudFound_P
0 = No Fraud
1 = Fraud

This is a binary classification problem.

---

## Summary of Preprocessing Decisions

• Removed identifier columns that do not add predictive value.
• Checked class imbalance 
• Applied One-Hot Encoding to categorical features.
• Performed train-test split before scaling to avoid data leakage.
• Standardized numerical features using StandardScaler.

---

## Key Insights & Observations

• Fraud cases represent a smaller proportion of total claims.
• Certain categorical features (e.g., Fault, AccidentArea) show noticeable fraud patterns.
• Numerical variables show some distribution differences between fraud and non-fraud cases.
• Accuracy alone is not sufficient due to class imbalance.

---

## Potential Next Modeling Steps

• Train Logistic Regression and Random Forest models.
• Use class weighting to handle imbalance.
• Evaluate using Recall, Precision, F1-score, and ROC-AUC.
• Focus on minimizing false negatives (missed fraud cases).
• Perform feature importance analysis.

---

## Modeling Consideration

In fraud detection, false negatives are more costly than false positives. 
Therefore, Recall for the fraud class should be prioritized during model evaluation.
