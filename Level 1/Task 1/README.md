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
