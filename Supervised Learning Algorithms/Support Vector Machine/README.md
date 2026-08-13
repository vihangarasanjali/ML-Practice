# SVM - Iris Species Classification

## Overview

This exercise demonstrates the implementation of a **Support Vector Machine (SVM)** classification algorithm using Python and Scikit-learn.

The goal is to classify Iris flowers into different species based on their physical measurements.

---

## Algorithm Used

### Support Vector Machine (SVM)

Support Vector Machine is a supervised machine learning algorithm commonly used for classification problems.

SVM finds a decision boundary that separates different classes while trying to maximize the margin between them.

In this project, SVM is used to classify Iris flowers into three species:

- Iris-setosa
- Iris-versicolor
- Iris-virginica

---

## Dataset

The dataset used is the **Iris dataset**.

The dataset contains measurements of Iris flowers.

### Features

| Feature | Description |
|---|---|
| SepalLengthCm | Length of the sepal |
| SepalWidthCm | Width of the sepal |
| PetalLengthCm | Length of the petal |
| PetalWidthCm | Width of the petal |

### Target

| Target | Description |
|---|---|
| Species | Iris flower species |

The `Id` column was removed because it is only an identifier and does not provide useful information for classification.

---

## Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

---

## Workflow

The exercise follows these steps:

1. Load the Iris dataset using Pandas
2. Explore the dataset using `info()` and `value_counts()`
3. Visualize feature relationships using a Seaborn pair plot
4. Separate features and target variable
5. Remove unnecessary columns
6. Split the dataset into training and testing sets
7. Create an SVM classifier
8. Train the SVM model
9. Make predictions on the test data
10. Evaluate the model using accuracy and confusion matrix

---

## Data Visualization

A pair plot was used to visualize the relationships between the different features.

```python
sns.pairplot(data, hue='Species')