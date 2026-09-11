# Level 3 (Task 2) - Support Vector Machine (SVM) for Classification
Implement a Support Vector Machine (SVM) model for binary classification.

# Dataset
`churn-bigml-80.csv` is used for SVM clasification.

# Objective
- Train an SVM model on a labeled dataset.
- Use different kernels (linear, RBF) and compareperformance.
- Visualize the decision boundary.Evaluate the model using accuracy, precision, recall,and AUC.
- Tools: Python, scikit-learn, pandas, matplotlib

# Discussion on the task
The task is till feature scaling from import libraries is same as Level 2 task 1. The insights of that is also same here. Now next `linear SVM and rbf SVM` models are trained and checked for metrics like `accuracy, precision, recall, auc score and classification report`. Then both of the models are compared. 
| Metric    | Linear SVM | RBF SVM |
|-----------|------------|---------|
| Accuracy  | 0.853933   | 0.857678 |
| Precision | 0.500000   | 0.583333 |
| Recall    | 0.038462   | 0.089744 |
| AUC       | 0.774404   | 0.837522 |

Overall rbf SVM performed slightly better than linear SVM on all metrics.Its accuracy increased from `85.39% to 85.77%,` while precision increased from `0.50 to 0.58`. The recall also improved from `0.038 to 0.090`, indicating that the RBF model was able to identify more churn customers than the Linear SVM, although the recall remained relatively low. For AUC score, there was noticeable change which increased from `0.774` for the Linear SVM to `0.838` for the RBF SVM.This indicates that the RBF kernel had better overall ability to distinguish between churn and non-churn customers.

Overall, the RBF SVM was the better-performing model for this dataset.

Then after comparison both the model was visualized.