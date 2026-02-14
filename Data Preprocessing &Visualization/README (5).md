
# Medical Insurance Cost Prediction
Data Preprocessing & Visualization

## Dataset Source
US Health Insurance Dataset
link:https://www.kaggle.com/datasets/mirichoi0218/insurance
Row Count: ~13,000+
Target Variable: charges (Annual medical insurance cost in USD)
Type: Regression

---

## Problem Statement
The objective is to predict annual medical insurance charges 
based on demographic and health-related attributes such as 
age, BMI, number of children, smoking status, and region.

This is a regression problem.

---

## Summary of Preprocessing Decisions

• Checked and handled missing values (none significant found).
• Removed duplicate records to prevent modeling bias.
• Assessed outliers using IQR method; retained valid high-cost cases.
• Encoded categorical variables (sex, smoker, region) using One-Hot Encoding.
• Performed train-test split before scaling to avoid data leakage.
• Standardized numerical features (age, bmi, children) using StandardScaler.
• Identified right-skewness in target variable; log transformation may improve performance.

---

## Key Insights

• Smoking status has the strongest impact on insurance charges.
• Age shows a clear positive relationship with cost.
• BMI has moderate influence.
• Charges distribution is right-skewed with high-cost outliers.
• Interaction effects (e.g., age × smoker) may enhance model accuracy.

---

## Potential Next Modeling Steps

• Train Linear Regression and Random Forest Regressor.
• Evaluate using RMSE and R².
• Apply log transformation to target variable if needed.
• Introduce interaction features.
• Perform cross-validation for robust evaluation.

---

## Modeling Consideration

High insurance charges represent legitimate high-risk individuals.
Outliers were retained as they carry meaningful business value.
