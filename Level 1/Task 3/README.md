# Level 1 (Task 3) - Implement KNN Classifier
Build a KNN classifier to classify data into categories.

# Dataset
Dataset used here is `Iris.csv` for KNN modelling.

## Objectives
- Train a KNN model on a labeled dataset
- Evaluate the performance using accuracy, confusion matrix and precision / recall
- Use of different K values and compare the results
- Tools: Python, Scikit-Learn, Pandas

## Process Followed
1. Importing libraries.
2. Loading of dataset and display first few data values.
3. Checking dataset details, missing values and duplicated values.
4. Droping duplicated rows.
5. Checking unique species names (specific step for this dataset).
6. Converting categorical `species` column to int data type by maping species to number.
7. Describing numerical data to check if there is any anomalies or not.
8. Feture selection.
9. Splitting dataset into train and test sets.
10. Feature scaling.
11. KNN modeling, metrices and comparing for different `k` values.

## Discussion on the task
The dataset was loaded. It was checked for details, missing values and duplicated values. On examining, dataset had duplicated values which were droped by using in-built function `.drop_duplicated()`. Printed unique flower species. `species` column was categorical so its values were mapped as follows `1 - setosa, 2 - versicolor and 3 - virginica`. Dataset was described using `.describe()` to check of anomalies in numerical data, no anomalies were found. Next step was feature selection and target column selected was `species` column. Dataset was splitted into 80/20 ratio followed by feature scaling. After data pre-processing, KNN modelling was done. Loop was used to model knn for `4` different `k` values. The metrices used was `accuracy` and `confusion matrix`. Also different other metrices were printed along `confusion matrix`. They were `precision, recall and f1-score` for all `k` values. For `k=1` accuracy was `93.33%` and for rest of `k` values from `2 to 4` was `96.67%`. This shows that for `k=2` it is giving best performance and model is converged as we can see for `k` values more than that is has same values for all metrices.