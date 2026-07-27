Here's a rewritten version of your **Day 12** report with the same concepts but different wording and structure, making it look like an independently written daily diary.

# Day 12 – Understanding Classification Algorithms

Today, I studied some of the most important **classification algorithms** used in supervised machine learning. These algorithms are designed to classify data into different categories based on patterns learned from labeled datasets. I explored their purpose, working principles, suitable use cases, and practical applications.

---

# Topics Covered

* Logistic Regression
* Naive Bayes
* K-Nearest Neighbors (KNN)
* Support Vector Machine (SVM)

---

# Logistic Regression

## Introduction

**Logistic Regression** is a supervised learning algorithm mainly used for **classification tasks**. It predicts the probability that a data sample belongs to a particular class and is commonly used for binary classification problems.

### Examples

* Spam or Not Spam
* Pass or Fail
* Customer Will Buy or Not

---

## Why Do We Use Logistic Regression?

Logistic Regression is preferred when:

* The output consists of two categories.
* A simple and interpretable model is required.
* Fast predictions are needed.
* The relationship between input features and output is relatively straightforward.

---

## How Does It Work?

1. Receives the input features.
2. Applies the **Sigmoid Function** to calculate probabilities.
3. Classifies the data based on the probability value.

### Python Example

```python
from sklearn.linear_model import LogisticRegression

model = LogisticRegression()

model.fit(X_train, y_train)

prediction = model.predict(X_test)
```

---

## Applications

* Email Spam Detection
* Medical Diagnosis
* Loan Approval Systems
* Customer Churn Prediction

---

# Naive Bayes

## Introduction

**Naive Bayes** is a probabilistic classification algorithm based on **Bayes' Theorem**. It assumes that all input features are independent of each other, making it simple and efficient for many classification problems.

---

## Why Do We Use Naive Bayes?

It is commonly used when:

* Working with text-based datasets.
* Solving document classification problems.
* Performing sentiment analysis.
* Building spam detection systems.

---

## How Does It Work?

1. Calculates the probability of each class.
2. Applies Bayes' Theorem.
3. Assigns the class with the highest probability.

### Python Example

```python
from sklearn.naive_bayes import GaussianNB

model = GaussianNB()

model.fit(X_train, y_train)

prediction = model.predict(X_test)
```

---

## Applications

* Spam Email Filtering
* Language Detection
* News Categorization
* Sentiment Analysis

---

# K-Nearest Neighbors (KNN)

## Introduction

**K-Nearest Neighbors (KNN)** is a distance-based classification algorithm. It predicts the class of a new data point by examining the classes of its nearest neighboring data points.

---

## Why Do We Use KNN?

KNN is suitable when:

* The dataset is relatively small.
* Similar records belong to the same category.
* A simple classification technique is sufficient.

---

## How Does It Work?

1. Select the value of **K**.
2. Calculate the distance between the new sample and all training samples.
3. Find the K nearest neighbors.
4. Predict the class with the majority vote.

### Python Example

```python
from sklearn.neighbors import KNeighborsClassifier

model = KNeighborsClassifier(n_neighbors=5)

model.fit(X_train, y_train)

prediction = model.predict(X_test)
```

---

## Applications

* Recommendation Systems
* Image Classification
* Handwriting Recognition
* Customer Segmentation

---

# Support Vector Machine (SVM)

## Introduction

**Support Vector Machine (SVM)** is a supervised classification algorithm that separates different classes by creating the **best possible decision boundary (hyperplane)**.

Its main objective is to maximize the distance between different classes, improving classification accuracy.

---

## Why Do We Use SVM?

SVM is useful when:

* High prediction accuracy is required.
* The dataset contains many features.
* Data can be separated using a clear decision boundary.
* Working on image or text classification problems.

---

## How Does It Work?

1. Identifies the optimal separating hyperplane.
2. Maximizes the margin between different classes.
3. Uses support vectors to define the decision boundary.

### Python Example

```python
from sklearn.svm import SVC

model = SVC(kernel="linear")

model.fit(X_train, y_train)

prediction = model.predict(X_test)
```

---

## Applications

* Face Recognition
* Image Classification
* Text Categorization
* Medical Diagnosis

---


-

