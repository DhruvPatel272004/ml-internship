# Level 2 (Task 1) -  Logistic Regression for Binary Classification

 Implement a logistic regression model topredict binary outcomes.

## Dataset
`churn-bigml-80.csv` is used here for binary classification.

## Objectives
- Load and preprocess the dataset.
- Train a logistic regression model using scikit-learn.
- Interpret model coefficients and the odds ratio.
- Evaluate the model using metrics such as accuracy,precision, recall, and the ROC curve.
- Tools: Python, pandas, scikit-learn, matplotlib.

## Discussion on the task
The dataset was loaded and checked for details, missing values and duplicated values. It was found that there were no missing values and no duplicated values, which indicates a better structured data. Then categorical data was converted to numerical data type, columns affected are `International plan, Voice mail plan and State`. Columns are rearranged for easier feature selection. Features are selected like target and predictor and then train and test split of 80/20 ratio followed by feature scaling to get all feture on one scale. Then the main part begins of defining model. Logistic regression is used to model data. It has two important model parameters based on each other that are `coefficients` and `odds ratio`. `Coefficient` shows the direction towards positive class and also its strength of relationship. `Odds ratio` is e to the power of coefficient.It tells the for every 1 unit increase in feature, the odds of the positive class are multiplied by odds ratio value, assuming all other features stay constant.
- '>1' - increases the odds of the positive class
- '=1' - no effect
- '<1' - decreases the odds of the positive class
After intrepreting the model, labels are give like `churn` and `not churn`. Then the model predicts against the test set and gives accuracy of around `85.39%`. It also plots confusion matrix chart and also various metrics related to confusion matrix. They are `precision - 0.88 , recall - 0.96 and f1-score - 0.92 of No churn` and `precision - 0.50 , recall - 0.21 and f1-score - 0.29 of Churn`. Then `ROC curve` is plotted and got `0.79`.

### Intrepretation of results:
- `Accuracy` tells that model correctly predicted whether they churned or did not churn about `85.39%` of the time out of all customers.
    - Buisness cannot rely on this alone as it gives combine results and not individual based on churn or not churn.
- `Precision` tells when model predicts churn or no churn how many times it was correct.
    - No churn - it is 88% means 88 customers will not churn and 12 will churn, out of 100 customers predicted no churn .
    - Churn - it is 50% means 50 customers will churn and 50 will not churn, out of 100 customers predicted churn.
    - For business, this model can be used for taking further steps on churner as it is giving false alarms which might be terrible to rely on this model for predicting churners. More metrics to look into.
- `Recall` tells of all the customers who actually belong to this class, how many did the model successfully identify?
    - No churn - it is 96% means 96 customers are correctly identified as No churn from 100 actual non-churn customers.
    - Churn - it is 21% means 21 customers are correctly identified as Churn from actual 100 actual churn customers.
    - Model here misses 79% of the actual churners, which also shows model is working well for churners.
- `F1-Score` it combines recall and precision.
    - No Churn - it is 92% means model is reasonably accurate when it predicts No churn and also very good at finding actual No churn customer.
    - Churn - it is 29% means the model is not able to reasonably predicts Churn and also not good at finding actual Churn customer.
    - This metric also shows that the model is bad at predicting churning customer.
- `ROC curve` shows how the model performs at different classification thresholds. It is 0.79 for this model.

In conclusion, by observing all these metrics it can be concluded that the model is good at predicting `No Churn customer` instead of `Churn customer`. 
Note: I think that's why the dataset name ends with 80 which might indicate `80%` of `No Churn customers`.

