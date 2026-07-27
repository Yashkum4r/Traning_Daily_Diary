# Day 13 – Decision Tree and Random Forest Algorithms

Today, I learned about **Decision Tree** and **Random Forest**, two popular supervised machine learning algorithms. These algorithms are widely used for solving both **classification** and **regression** problems. I studied their working principles, advantages, limitations, practical uses, and basic implementation in Python.

---

# Topics Covered

* Decision Tree
* Random Forest

---

# Decision Tree

## What is a Decision Tree?

A **Decision Tree** is a supervised learning algorithm that predicts outcomes by dividing a dataset into smaller groups based on feature values. It creates a flowchart-like structure made up of **root nodes, internal nodes, branches, and leaf nodes**.

Each split helps the model make better decisions until it reaches the final prediction.

### Example

A bank wants to decide whether a customer should receive a loan.

```text
Income > 50000?
       /      \
     Yes      No
      |         |
Credit Score?  Reject
   /      \
Good      Poor
 |          |
Approve   Reject
```

---

## Why Do We Use Decision Tree?

Decision Trees are useful because they:

* Are easy to understand and interpret.
* Handle both numerical and categorical data.
* Help identify the most important features.
* Can solve both classification and regression problems.

---

## Where is Decision Tree Used?

Decision Trees are commonly used in:

* Loan approval systems
* Medical diagnosis
* Student performance prediction
* Fraud detection
* Customer segmentation

---

## How Does a Decision Tree Work?

1. Begins with the complete dataset.
2. Selects the best feature for splitting the data.
3. Creates branches based on feature values.
4. Continues splitting until a stopping condition is met.
5. Produces the final prediction at the leaf node.

### Python Example

```python
from sklearn.tree import DecisionTreeClassifier

model = DecisionTreeClassifier(random_state=42)

model.fit(X_train, y_train)

prediction = model.predict(X_test)
```

---

## Advantages

* Easy to visualize and explain.
* Requires minimal data preparation.
* Supports both numerical and categorical features.
* Can be applied to classification and regression tasks.

---

## Limitations

* May overfit the training data.
* Sensitive to small changes in the dataset.
* Large trees can become difficult to manage.

---

# Random Forest

## What is Random Forest?

**Random Forest** is an ensemble learning algorithm that combines the predictions of multiple Decision Trees to improve overall accuracy.

Instead of depending on one tree, it builds several trees using different samples of the data and combines their results through **majority voting** (classification) or **averaging** (regression).

---

## Why Do We Use Random Forest?

Random Forest is preferred because it:

* Produces more accurate predictions.
* Reduces the risk of overfitting.
* Works well with large datasets.
* Handles complex relationships between features.

---

## Where is Random Forest Used?

Random Forest is widely used in:

* House Price Prediction
* Credit Risk Analysis
* Medical Diagnosis
* Fraud Detection
* Customer Churn Prediction

---

## How Does Random Forest Work?

1. Creates multiple random subsets of the training dataset.
2. Builds a Decision Tree for each subset.
3. Each tree generates its own prediction.
4. Combines the predictions of all trees.
5. Returns the final output using majority voting or averaging.

### Python Example

```python
from sklearn.ensemble import RandomForestClassifier

model = RandomForestClassifier(
    n_estimators=100,
    random_state=42
)

model.fit(X_train, y_train)

prediction = model.predict(X_test)
```

---

## Advantages

* Provides high prediction accuracy.
* Reduces overfitting compared to a single Decision Tree.
* Handles large datasets efficiently.
* Can estimate feature importance.
* Performs well even with noisy data.

---

## Limitations

* Requires more computational resources.
* Takes longer to train than a Decision Tree.
* More difficult to interpret due to multiple trees.
