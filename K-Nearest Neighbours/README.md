# K-Nearest Neighbors (KNN) - Iris Classification

## Overview

This project demonstrates the implementation of the **K-Nearest Neighbors (KNN) machine learning algorithm** using Python and Scikit-learn.

The goal of this project is to classify iris flowers into different species based on their physical measurements.

KNN is a supervised machine learning algorithm that predicts the class of a new data point by looking at the classes of its nearest neighbors.

---

# Algorithm Used

## K-Nearest Neighbors (KNN)

KNN is a classification algorithm based on similarity between data points.

The algorithm:

1. Calculates the distance between the new data point and existing data points.
2. Selects the K nearest neighbors.
3. Predicts the class based on the majority vote.

The distance is commonly calculated using **Euclidean distance**.

---

# Dataset

The project uses the **Iris dataset**.

The dataset contains measurements of iris flowers.

## Features

| Feature | Description |
|---------|-------------|
| Sepal Length | Length of the sepal |
| Sepal Width | Width of the sepal |
| Petal Length | Length of the petal |
| Petal Width | Width of the petal |

## Target Variable

| Target | Description |
|---|---|
| Species | Iris flower species |

Classes:

```
Iris-setosa
Iris-versicolor
Iris-virginica
```

---

# Data Preprocessing

## Feature Selection

The input features were separated from the target variable.

```python
x = data.iloc[:,1:5]

y = data.iloc[:,-1]
```

---

## Feature Scaling

Since KNN calculates distances between data points, feature scaling is important.

Standardization was applied using:

```python
from sklearn.preprocessing import StandardScaler

scaler = StandardScaler()

x = scaler.fit_transform(x)
```

Scaling prevents features with larger values from dominating the distance calculation.

---

# Model Training

The dataset was divided into:

- Training data: 80%
- Testing data: 20%

```python
train_test_split(
    x,
    y,
    test_size=0.2,
    random_state=0
)
```

The KNN model was trained using:

```python
from sklearn.neighbors import KNeighborsClassifier

model = KNeighborsClassifier(n_neighbors=1)

model.fit(x_train, y_train)
```

---

# Selecting the Best K Value

Different values of K were tested from 1 to 19.

```python
for i in range(1,20):
    model = KNeighborsClassifier(n_neighbors=i)
```

The number of correct predictions was recorded for each K value to find a suitable neighbor count.

The final model was trained using:

```python
KNeighborsClassifier(n_neighbors=8)
```

---

# Model Evaluation

The model performance was evaluated using:

## Accuracy Score

Accuracy represents the percentage of correct predictions.

```python
from sklearn.metrics import accuracy_score

accuracy_score(y_test, pred)
```

---

## Confusion Matrix

A confusion matrix shows the comparison between actual and predicted classes.

```python
from sklearn.metrics import confusion_matrix

confusion_matrix(y_test, pred)
```

It helps identify:

- Correct classifications
- Misclassified samples
- Class-wise performance

---

# Technologies Used

- Python
- NumPy
- Pandas
- Scikit-learn
- Jupyter Notebook

---

# Learning Outcomes

Through this project, I learned:

- Fundamentals of K-Nearest Neighbors algorithm
- How distance-based algorithms work
- Importance of feature scaling
- Training classification models
- Selecting a suitable value of K
- Evaluating models using accuracy and confusion matrix
- Working with real-world datasets

---

# Future Improvements

- Compare KNN performance with other algorithms:
  - Logistic Regression
  - Decision Trees
  - Random Forest
  - Support Vector Machines

- Perform hyperparameter tuning using GridSearchCV.

- Visualize decision boundaries.