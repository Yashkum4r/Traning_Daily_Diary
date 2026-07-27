# Day 10 – Automated Exploratory Data Analysis (Auto EDA)

Today, I explored **Automated Exploratory Data Analysis (Auto EDA)**, a technique that simplifies the process of understanding datasets. Instead of manually applying multiple analysis functions, Auto EDA tools generate detailed reports containing statistics, visualizations, and data quality insights in just a few steps.

---

# Topics Covered

* Introduction to Auto EDA
* Importance of Auto EDA
* Popular Auto EDA Tools
* Creating an Auto EDA Report
* Advantages and Drawbacks

---

# Introduction to Auto EDA

**Automated Exploratory Data Analysis (Auto EDA)** is the process of examining a dataset automatically with the help of Python libraries. These libraries analyze the dataset and generate a complete report, making it easier to understand the data before applying machine learning models.

An Auto EDA report generally includes:

* Basic dataset information
* Data types of each feature
* Missing and duplicate values
* Statistical summaries
* Feature distributions
* Correlation between variables
* Outlier identification
* Graphical visualizations
* Data quality alerts

---

# Importance of Auto EDA

Auto EDA is useful because it:

* Speeds up the data analysis process.
* Minimizes manual effort.
* Detects missing and duplicate records quickly.
* Highlights outliers and inconsistencies.
* Provides useful statistical information automatically.
* Helps prepare data for machine learning projects.

---

# Common Auto EDA Libraries

## 1. ydata-profiling

The **ydata-profiling** library generates a detailed HTML report that includes descriptive statistics, correlations, missing values, charts, and dataset warnings.

### Example

```python
import pandas as pd
from ydata_profiling import ProfileReport

df = pd.read_csv("house_price.csv")

profile = ProfileReport(df, title="Auto EDA Report")

profile.to_file("EDA_Report.html")
```

---

## 2. Sweetviz

**Sweetviz** creates interactive reports that help users explore datasets and compare training and testing data visually.

### Example

```python
import sweetviz as sv

report = sv.analyze(df)

report.show_html("Sweetviz_Report.html")
```

---

## 3. AutoViz

**AutoViz** automatically generates multiple charts and visualizations with only a few lines of code, making data exploration much faster.

### Example

```python
from autoviz.AutoViz_Class import AutoViz_Class

AV = AutoViz_Class()

AV.AutoViz(
    filename="house_price.csv",
    depVar="Price"
)
```

---

# Steps to Perform Auto EDA

1. Load the dataset into Python.
2. Install and import an Auto EDA library.
3. Generate the analysis report.
4. Examine the statistics, charts, and warnings.
5. Use the report to clean and prepare the dataset for further analysis.

---

# Advantages

* Automatically creates detailed reports.
* Saves time during data exploration.
* Beginner-friendly and easy to use.
* Offers clear visualizations for better understanding.

---

# Limitations

* Processing large datasets may require more time.
* Reports can consume considerable memory.
* Manual analysis is still necessary for deeper business understanding and decision-making.

