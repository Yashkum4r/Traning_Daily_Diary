# Day 16 – Wrapper-Based Feature Selection Techniques

Today, I studied the **Wrapper Method**, an important feature selection approach in machine learning. Unlike filter methods, wrapper methods evaluate different feature combinations by training a machine learning model and selecting the subset that produces the best performance. I also learned about three popular wrapper techniques: **Forward Selection**, **Backward Elimination**, and **Recursive Feature Elimination with Cross Validation (RFECV)**.

---

# Topics Covered

* Wrapper Method
* Forward Selection
* Backward Elimination
* Recursive Feature Elimination with Cross Validation (RFECV)

---

# Wrapper Method

## What is the Wrapper Method?

The **Wrapper Method** is a feature selection technique that searches for the best combination of features by repeatedly training a machine learning model and measuring its performance.

Instead of relying only on statistical measures, this method selects features based on how much they improve the model's prediction accuracy.

---

## Why Do We Use the Wrapper Method?

The Wrapper Method is used to:

* Identify the most relevant features.
* Improve the prediction accuracy of the model.
* Eliminate unnecessary or redundant features.
* Reduce the chances of overfitting.
* Build a more efficient machine learning model.

---

## Where is the Wrapper Method Used?

It is commonly applied when:

* The dataset contains many input features.
* Model accuracy is more important than training speed.
* Finding the best feature subset is the main objective.

---

## Advantages

* Produces highly accurate models.
* Evaluates feature combinations using the actual machine learning algorithm.
* Often provides better feature selection than simple statistical methods.

---

## Limitations

* Requires more computation time.
* Slower than Filter Methods.
* Not suitable for very large datasets with hundreds of features.

---

# 1. Forward Selection

## What is Forward Selection?

**Forward Selection** is a wrapper technique that begins with **no selected features**. It gradually adds one feature at a time, choosing the feature that gives the greatest improvement in model performance.

The process stops when adding more features no longer improves the model.

---

## Why Do We Use Forward Selection?

Forward Selection is useful when:

* The dataset contains a large number of features.
* Only the most influential variables are required.
* A simple and efficient model is preferred.

---

## How Does Forward Selection Work?

1. Start with an empty feature set.
2. Train the model using each feature separately.
3. Select the feature that performs best.
4. Continue adding one feature at a time.
5. Stop when no further improvement is observed.

### Python Example

```python id="0rrhqe"
from sklearn.feature_selection import SequentialFeatureSelector
from sklearn.linear_model import LinearRegression

model = LinearRegression()

forward = SequentialFeatureSelector(
    model,
    direction="forward",
    n_features_to_select=3
)

forward.fit(X, y)
```

---

# 2. Backward Elimination

## What is Backward Elimination?

**Backward Elimination** works in the opposite direction of Forward Selection. It starts with **all available features** and removes the least important feature one by one until only the most useful features remain.

---

## Why Do We Use Backward Elimination?

This technique is preferred when:

* Most features are expected to be useful.
* Only unnecessary variables need to be removed.
* A simpler and faster model is required.

---

## How Does Backward Elimination Work?

1. Begin with all features.
2. Train the machine learning model.
3. Identify the least important feature.
4. Remove that feature and retrain the model.
5. Repeat until the optimal feature set is obtained.

### Python Example

```python id="9jb9li"
from sklearn.feature_selection import SequentialFeatureSelector
from sklearn.linear_model import LinearRegression

model = LinearRegression()

backward = SequentialFeatureSelector(
    model,
    direction="backward",
    n_features_to_select=3
)

backward.fit(X, y)
```

---

# 3. Recursive Feature Elimination with Cross Validation (RFECV)

## What is RFECV?

**RFECV (Recursive Feature Elimination with Cross Validation)** is an advanced wrapper technique that automatically determines the optimal number of features.

It repeatedly removes the least important feature while evaluating model performance through **Cross Validation**, ensuring that the selected features generalize well to unseen data.

---

## Why Do We Use RFECV?

RFECV is used because it:

* Automatically selects the ideal number of features.
* Improves prediction performance.
* Helps reduce overfitting.
* Produces more reliable and stable models.

---

## How Does RFECV Work?

1. Train the model using all available features.
2. Remove the least significant feature.
3. Evaluate the model using cross validation.
4. Repeat the elimination process.
5. Select the feature subset with the best validation score.

### Python Example

```python id="e1z22d"
from sklearn.feature_selection import RFECV
from sklearn.linear_model import LinearRegression

model = LinearRegression()

rfecv = RFECV(
    estimator=model,
    cv=5
)

rfecv.fit(X, y)
```

---
