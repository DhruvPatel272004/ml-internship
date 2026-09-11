# Codeveda Technologies ML Internship

This repository contains the machine learning tasks completed during my remote internship with Codeveda Technologies. The work progresses from dataset preprocessing to supervised classification, model evaluation, tuning, and feature analysis.

## Repository Structure

```text
Data/
├── 1) Iris.csv
├── 2) Stock Prices Data Set.csv
├── 3) Sentiment dataset.csv
├── 4) House Prediction Data Set.csv
└── Churn Prediction Data/
	├── churn-bigml-20.csv
	└── churn-bigml-80.csv

Level 1/
├── Task 1/  Data preprocessing
├── Task 2/
└── Task 3/  K-nearest neighbors classification

Level 2/
├── Task 1/  Logistic regression
├── Task 2/  Decision tree classification
└── Task 3/

Level 3/
├── Task 1/  Random forest classification
├── Task 2/  Support vector machine classification
└── Task 3/
```

Each completed task includes a Jupyter Notebook and a task-specific README where applicable.

## Topics Covered

- Data inspection and preprocessing with pandas
- Missing-value and duplicate-value checks
- Categorical encoding and feature scaling
- Train/test splitting and stratification
- KNN, logistic regression, decision tree, random forest, and SVM models
- Classification metrics including accuracy, precision, recall, F1-score, confusion matrix, and ROC-AUC
- Decision-tree visualization and pruning
- Hyperparameter tuning with grid search and cross-validation
- Random-forest feature importance analysis

## Tools and Libraries

- Python 3
- Jupyter Notebook
- pandas
- NumPy
- scikit-learn
- matplotlib

## Running the Notebooks

1. Clone the repository and open it in JupyterLab, Jupyter Notebook, Google colab or VS Code.
2. Ensure the notebook kernel has the required Python libraries installed:

   ```bash
   pip install numpy pandas scikit-learn matplotlib jupyter
   ```

3. Open a notebook inside the relevant `Level` and `Task` directory.
4. Run the cells from top to bottom. Dataset paths are relative to the repository structure, so run the notebook from its task directory or update the path if needed.

## Notes

The churn datasets are used for binary classification tasks, while `Iris.csv` is used for multiclass classification. Model results are documented in the README files inside the completed task directories and in the corresponding notebooks.
