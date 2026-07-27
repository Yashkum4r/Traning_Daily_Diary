# Day 14 – Exploring Regression Algorithms

Today, I learned about **Regression Algorithms**, which are used in supervised machine learning to estimate **continuous numerical values**. I studied three important regression techniques: **Linear Regression, Ridge Regression, and Lasso Regression**. I also learned where these algorithms are applied, how they work, and their strengths and limitations.

---

# Topics Covered

* Introduction to Regression
* Linear Regression
* Ridge Regression
* Lasso Regression
* Comparison of Regression Algorithms

---

# Introduction to Regression

**Regression** is a supervised learning technique that predicts numerical values based on the relationship between input features and a target variable. It is widely used whenever the expected output is a continuous value instead of a category.

### Common Applications

* House Price Prediction
* Salary Estimation
* Sales Forecasting
* Weather Forecasting
* Stock Price Prediction

---

# Why is Regression Important?

Regression helps us to:

* Estimate future numerical values.
* Discover relationships between variables.
* Analyze business trends.
* Support decision-making using data.
* Build predictive models for real-world problems.

---

# Linear Regression

## What is Linear Regression?

**Linear Regression** is one of the simplest machine learning algorithms. It predicts the target value by fitting a straight line that best represents the relationship between the input variables and the output.

The mathematical equation is:

```text id="x4n72p"
Y = mX + c
```

Where:

* **Y** = Predicted value
* **X** = Input variable
* **m** = Slope of the line
* **c** = Intercept

---

## Where is Linear Regression Used?

Linear Regression is suitable when:

* The target variable is numerical.
* The relationship between variables is approximately linear.
* A simple prediction model is required.
* The dataset has minimal multicollinearity.

---

## Working Process

1. Collect the input data.
2. Find the best-fit straight line.
3. Minimize prediction errors.
4. Use the equation to predict new values.

### Python Example

```python id="f3m1kv"
from sklearn.linear_model import LinearRegression

model = LinearRegression()

model.fit(X_train, y_train)

prediction = model.predict(X_test)
```

---

## Advantages

* Easy to understand.
* Fast training process.
* Simple mathematical interpretation.
* Effective for linear relationships.

---

## Limitations

* Cannot model complex non-linear patterns.
* Sensitive to outliers.
* Performance decreases when features are highly correlated.

---

# Ridge Regression

## What is Ridge Regression?

**Ridge Regression** is an extension of Linear Regression that applies **L2 Regularization**. It reduces the impact of large coefficient values, helping the model avoid overfitting.

Unlike Lasso Regression, Ridge keeps every feature in the model while reducing the size of their coefficients.

---

## Why is Ridge Regression Used?

Ridge Regression is useful when:

* The dataset contains many input features.
* Features are strongly correlated.
* The Linear Regression model is overfitting.
* Better model stability is required.

---

## Working Process

1. Build a Linear Regression model.
2. Add an L2 penalty to the loss function.
3. Reduce large coefficient values.
4. Produce a more generalized model.

### Python Example

```python id="r29syj"
from sklearn.linear_model import Ridge

model = Ridge(alpha=1.0)

model.fit(X_train, y_train)

prediction = model.predict(X_test)
```

---

## Advantages

* Helps reduce overfitting.
* Handles multicollinearity effectively.
* Produces more stable predictions.
* Improves model generalization.

---

## Limitations

* Does not remove unnecessary features.
* Requires selecting an appropriate regularization parameter.

---

# Lasso Regression

## What is Lasso Regression?

**Lasso Regression** is another improved version of Linear Regression that uses **L1 Regularization**. It reduces the coefficients of less important features to zero, automatically removing them from the model.

This makes Lasso useful for both prediction and feature selection.

---

## Why is Lasso Regression Used?

Lasso Regression is preferred when:

* The dataset contains many features.
* Some variables have little effect on the prediction.
* Feature selection is required.
* A simpler model is preferred.

---

## Working Process

1. Begin with a Linear Regression model.
2. Apply an L1 penalty.
3. Reduce unimportant feature coefficients to zero.
4. Keep only the most relevant features for prediction.

### Python Example

```python id="z64cnh"
from sklearn.linear_model import Lasso

model = Lasso(alpha=0.1)

model.fit(X_train, y_train)

prediction = model.predict(X_test)
```

---

## Advantages

* Performs automatic feature selection.
* Reduces model complexity.
* Helps prevent overfitting.
* Improves model interpretability.

---

## Limitations

* Important features may be removed if the penalty is too high.
* Choosing the correct alpha value is essential for good performance.

---
