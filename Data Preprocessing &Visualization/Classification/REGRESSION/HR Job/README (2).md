
# HR Analytics – Job Change of Data Scientists
Data Preprocessing & Visualization

## Dataset Source
Kaggle – HR Analytics Job Change of Data Scientists  
Link: https://www.kaggle.com/datasets/arashnic/hr-analytics-job-change-of-data-scientists

Dataset Size: 19,158 rows (training dataset used)

---

## Problem Statement
The objective is to predict whether a data scientist is likely to change jobs based on demographic, education, and professional attributes.

Target Variable:
0 → Not looking for job change  
1 → Looking for job change  

This is a binary classification problem.

---

## Summary of Preprocessing Decisions

• Removed enrollee_id as it is an identifier.  
• Converted experience column from mixed values (">20", "<1") to numeric format.  
• Imputed missing experience values using median.  
• Replaced missing categorical values with "Unknown" to preserve dataset size.  
• Removed city column due to high cardinality (123 unique values).  
• Applied One-Hot Encoding to remaining categorical variables.  
• Performed train-test split before scaling to prevent data leakage.  
• Standardized numerical features using StandardScaler.

---

## Key Insights & Observations

• Less experienced candidates are more likely to change jobs.  
• Employees from smaller companies show higher job-switch intent.  
• Higher city development index is associated with lower job change probability.  
• Training hours show limited separation between classes.  
• The dataset has moderate class imbalance (~75% vs 25%).

---

## Potential Next Modeling Steps

• Train Logistic Regression and Random Forest models.  
• Use class weighting to handle imbalance.  
• Evaluate using ROC-AUC, Precision, Recall, and F1-score.  
• Perform feature importance analysis.  
• Create experience bins (0–2, 3–5, 6–10, 10+).  
• Explore interaction features such as experience × company_size.
