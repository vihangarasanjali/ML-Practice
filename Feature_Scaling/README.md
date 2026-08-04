# Feature Scaling - Machine Learning Preprocessing

## Overview

This demonstrates the importance of **feature scaling** in machine learning preprocessing using Python and Scikit-learn.

Feature scaling is a technique used to transform numerical features into a similar range so that machine learning algorithms can process them effectively.

In this exercise, age and salary features are scaled because they have very different ranges.

---

## Why Feature Scaling?

Machine learning algorithms can be affected by the scale of input features.

Example:

| Feature | Value Range |
|---------|-------------|
| Age | 20 - 40 |
| Salary | 40000 - 70000 |

Since salary values are much larger than age values, some algorithms may give more importance to salary.

Feature scaling helps prevent this problem by bringing features to a comparable scale.

---

## Dataset

The dataset contains two numerical features:

| Feature | Description |
|---------|-------------|
| Age | Age of a person |
| Salary | Annual salary of a person |

Example:

| Age | Salary |
|---|---|
| 26 | 50000 |
| 29 | 70000 |
| 34 | 55000 |
| 31 | 41000 |

---

# Scaling Techniques

## 1. Standardization

Standardization transforms data so that:

- Mean = 0
- Standard deviation = 1

Formula:

```
z = (x - mean) / standard deviation
```

Implementation:

```python
from sklearn.preprocessing import StandardScaler

scaler = StandardScaler()

scaled_data = scaler.fit_transform(data)
```

---

## 2. Normalization (Min-Max Scaling)

Normalization transforms values into a fixed range, usually:

```
0 to 1
```

Formula:

```
x' = (x - min(x)) / (max(x) - min(x))
```

Implementation:

```python
from sklearn.preprocessing import MinMaxScaler

scaler = MinMaxScaler()

scaled_data = scaler.fit_transform(data)
```

---

# Technologies Used

- Python
- NumPy
- Scikit-learn
- Jupyter Notebook

---

# Machine Learning Algorithms That Benefit From Scaling

Feature scaling is important for:

- Logistic Regression
- Linear Regression
- K-Nearest Neighbors (KNN)
- Support Vector Machines (SVM)
- Neural Networks
- K-Means Clustering

Tree-based algorithms such as Decision Trees and Random Forests usually do not require scaling.

---

# Learning Outcomes

Through this exercise, I learned:

- Why feature scaling is needed in machine learning
- How different feature ranges affect models
- Difference between standardization and normalization
- How to apply `StandardScaler`
- How to apply `MinMaxScaler`
- Importance of preprocessing before model training

---

