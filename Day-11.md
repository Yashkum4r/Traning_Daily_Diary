# Day 11 – Introduction to Supervised Machine Learning

Today, I studied **Supervised Machine Learning**, a learning approach in which a model is trained using labeled data. The model learns the relationship between input features and known outputs so that it can make accurate predictions on new data. I also explored its two major categories: **Classification** and **Regression**, along with the commonly used algorithms in each category.

---

# Topics Covered

* Introduction to Machine Learning
* Types of Machine Learning
* Supervised Learning
* Classification
* Classification Algorithms
* Regression
* Regression Algorithms

---

# Introduction to Machine Learning

**Machine Learning (ML)** is a field of Artificial Intelligence (AI) that allows computers to learn from past data and make predictions or decisions without being explicitly programmed for every task.

Instead of following fixed instructions, ML models identify patterns in data and use those patterns to solve real-world problems.

---

# Types of Machine Learning

Machine Learning is generally divided into three categories:

1. Supervised Learning
2. Unsupervised Learning
3. Reinforcement Learning

During today's session, the main focus was on **Supervised Learning**.

---

# What is Supervised Learning?

**Supervised Learning** is a machine learning technique where the model is trained using **labeled data**. Every training record contains input features along with the correct output, allowing the model to learn the relationship between them.

Once trained, the model can predict the output for new and unseen data.

### Example

A house price dataset:

| Area (sq ft) | Price ($) |
| ------------ | --------: |
| 1000         |    150000 |
| 1500         |    220000 |
| 2000         |    300000 |

The model learns how the house area influences its price and then estimates the price of a new house based on its area.

---

# Categories of Supervised Learning

Supervised Learning is mainly divided into two types:

1. Classification
2. Regression

---

# 1. Classification

Classification is used when the output belongs to a **specific category or class**. The objective is to predict which class a new data point belongs to.

### Examples

* Email: Spam or Not Spam
* Loan: Approved or Rejected
* Student: Pass or Fail
* Disease: Positive or Negative

---

# Common Classification Algorithms

## Logistic Regression

Logistic Regression is used to classify data into categories, especially when there are only two possible outcomes.

**Example:** Predicting whether an email is spam or not.

---

## Naive Bayes

Naive Bayes is a probability-based algorithm that applies Bayes' Theorem to classify data.

**Example:** Text classification and spam filtering.

---

## K-Nearest Neighbors (KNN)

KNN predicts the class of a new data point by comparing it with its nearest neighboring data points.

**Example:** Classifying different types of fruits.

---

## Support Vector Machine (SVM)

SVM separates different classes by finding the best decision boundary between them.

**Example:** Handwritten character recognition.

---

## Decision Tree

Decision Tree creates a tree-like structure to make decisions by splitting the dataset based on feature values.

**Example:** Loan approval prediction.

---

## Random Forest

Random Forest combines multiple decision trees to improve prediction accuracy and reduce overfitting.

**Example:** Fraud detection and customer churn prediction.

---

# 2. Regression

Regression is used when the target variable is a **continuous numerical value** rather than a category.

It helps estimate values based on existing data.

### Examples

* House Price Prediction
* Salary Estimation
* Sales Forecasting
* Temperature Prediction

---

# Common Regression Algorithms

## Linear Regression

Linear Regression predicts numerical values by establishing a linear relationship between input and output variables.

**Example:** Predicting house prices based on area.

---

## Ridge Regression

Ridge Regression is an enhanced version of Linear Regression that applies **L2 Regularization** to reduce overfitting and improve model stability.

**Example:** Predicting house prices when several features are highly correlated.

---

## Lasso Regression

Lasso Regression uses **L1 Regularization**, which can automatically eliminate less important features by reducing their coefficients to zero.

**Example:** Selecting the most important variables in a house price prediction model.

---

# Difference Between Classification and Regression

| Classification                 | Regression                           |
| ------------------------------ | ------------------------------------ |
| Predicts categories or classes | Predicts continuous numerical values |
| Output is discrete             | Output is continuous                 |
| Example: Spam Detection        | Example: House Price Prediction      |
