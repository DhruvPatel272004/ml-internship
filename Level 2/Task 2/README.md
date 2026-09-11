# Level 2 (Task 2) -  Decision Trees for Classification
Build a decision tree classifier to predicta categorical outcome

# Dataset 
`Iris.csv` is used for Decision Tree clasifier.

# Objective
- Train a decision tree on a labeled dataset.
- Visualize the tree structure.
- Prune the tree to prevent overfitting.
- Evaluate the model using classification metrics such asaccuracy and F1-score.
- Tools: Python, scikit-learn, pandas, matplotlib.

# Discussion on the task
The task begins with importing libraries, loading data, checking first few entries and displaying all information of the dataset. Missing values and Duplicated values are checked and no missing values were found whereas 3 duplicated entries were found and removed from the dataset. List of unique flower species was built. Categorical data changed to numerical data, column affected `species`. Then shape of the dataset is checked for feature selection. After feature selection, the dataset is splitted into 80/20 ratio of training and testing respectively. The model is defined with default setting and and fitted for training. The tree is visualized using `plot_tree(dtc)`. Then prediction on training test set was performed followed by comparison with on testing test case to get metrices like accuracy and f1 score which was around `96.67%` and `96.66%` respectively. After this, the tree was pruned with `max_depth=2` and `random_state=0` with gave different result from original tree. But after that changed `max_depth=3` which gave same metrices result as original tree but on further analysis if it by comparing the `y_pred` and `y_pred_pruned` also gave that the prediction were same but further on tree depth and no of leaves were check which gave less than original tree
`(Original tree depth: 6
Pruned tree depth: 3
Original number of leaves: 9
Pruned number of leaves: 4)`. This shows that pruned have less depth and also no of leaves are less which shows us that rest of the nodes in original are irrelevant which we can conclude by checking the result of both the tree as same.

Note: The above case of `max_depth=3` is taken instead `max_depth=2` to have more analysis on Decision Tree Classifier and how it works and also what can be analyse further to choose better model.