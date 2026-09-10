# Level 1 (Task 1) - Data Processing for Machine Learning

Preprocess a raw dataset to make it ready for machine learning.

## Objectives
- Handle missing data
- Encode categorical variables
- Normalize numerical features
- Split the dataset into training and testing sets
- Tools: Python, Pandas, Scikit-Learn

## Dataset Used
`churn-bigml-20.csv` is used as dataset to pre-process for this task.

## Process followed
1. Importing required libraries.
2. Loading data and printing first few rows.
3. Looking for dataset information in detail by `.info()` method and `.describe()` for various measures of numerical data to identify anomalies.
4. Handling missing and duplicated values by using `.isna()` and `.duplicated()` respectively.
5. Converting categorical data to numerical data. Columns affected are `International plan`, `Voice mail plan`, `State` and `Churn`.
6. Rearranging columns to access easily for features selection.
7. Features selection for training and testing.
8. Spliting the dataset into 80/20 ratio of train and test.
9. Feature scaling to make all data into one range.
10. Printing shapes for splited data to confirm the spliting.

## Discusion on the task
The task was simple as for this task on describing dataset no anomalies were, no missing values and no duplicated values were found, which shows that data is well prepared and we can proceed further onto next task. Next, converting categorical columns to numerical data was done on `International plan`, `Voice mail plan`, `State` and `Churn` columns. First two columns listed were mapped to 0 and 1 according to the data as it had No and Yes in dat values. `State` column had multiple values so one-hot encoding was used and even to int data type. Last column was bool it can passed for modelling but it is also better to convert to numerical data type so it was also converted to int data type. After that for easy feature selection columns were reaaranged such that `Churn` columns comes first. Then in features selection it was chosed as target column. Then data was splitted into 80/20 ratio and scaled to bring all data to same range.