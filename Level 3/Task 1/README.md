# Level 3 (Task 1) -  Build a Random ForestClassifier
Implement a Random Forest model forclassification on a complex dataset.

# Dataset
`churn-bigml-20.csv` is used here for Random Forest model.

# Objective
- Train a Random Forest model and tune hyperparameters.
- Evaluate the model using cross-validation and classification metrics (precision, recall, F1-score).
- Perform feature importance analysis to identify the most important features in the dataset.
- Tools: Python, scikit-learn, pandas, matplotlib.

# Discussion on the task
The task begins with import libraries, loading dataset, checking all details of dataset and describing numerical data to check for anomalies. Then missing values and duplicated values are checked, no missing values and no duplicated values were found. After that categorical data is converted to numerical data, columns affected are `International plan,Voice mail plan, Churn and State`. Then the columns are rearranged for easier feature selection. Feature selection was next step and selected predictors to `X` and target to `y`. Splitted data into train and test into 80/20 ratio and interestingly stratify is used here which breaks no churn and churn into same portion which give better data for training. Data is then trained on default `Random Forest Classifier model` and metrics like accuracy and classification report are printed. Then parameteres grid was made and used `GridSearchCv` to find best paramaters and best score. Next tuned model is trained on best estimators and fitted to train and prediction are made. After this metrics are assessed like accuracy and classification report. Then cross validation is performed and mean f1 score is printed. Further step was to get important features like `first 10 important features` in random forest model of the data trained. It was then visualized using horizontal bar chart showing highest to lowest. Comparison of original and tuned model is done. The `accuracy` and `f1 score` of original random forest model was `88.81%`and `40%` respectively whereas for tuned random forest was `88.06%` and `38.46%` respectively.