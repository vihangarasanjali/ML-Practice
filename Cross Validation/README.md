# Cross-Validation - Iris Classification

## Overview

This exercise demonstrates the use of **Cross-Validation** to evaluate and compare different machine learning classification algorithms using the Iris dataset.

The goal is to determine which classification algorithm performs best by evaluating each model across multiple training and validation splits.

---

## Concept Used

### Cross-Validation

Cross-Validation is a model evaluation technique used to estimate how well a machine learning model performs on unseen data.

In this exercise, **5-Fold Cross-Validation** was used.

The dataset is divided into 5 parts. The model is trained using 4 parts and validated using the remaining part. This process is repeated 5 times so that each part is used as the validation set once.

The scores from all 5 folds are then averaged to obtain the overall performance of the model.

---

## Dataset

The **Iris dataset** was used for this exercise.

The dataset contains measurements of Iris flowers belonging to three different species.

### Features

| Feature | Description |
|---|---|
| Sepal Length | Length of the sepal |
| Sepal Width | Width of the sepal |
| Petal Length | Length of the petal |
| Petal Width | Width of the petal |

### Target

| Target | Description |
|---|---|
| Species | Iris flower species |

The three classes are:

- Iris-setosa
- Iris-versicolor
- Iris-virginica

---

## Algorithms Compared

The following classification algorithms were evaluated using Cross-Validation:

- K-Nearest Neighbors (KNN)
- Random Forest
- Support Vector Machine (SVM)
- Naive Bayes

---

## Technologies Used

- Python
- Pandas
- Scikit-learn
- Jupyter Notebook

---

## Workflow

The project follows these steps:

1. Load the Iris dataset
2. Separate features and target variable
3. Create different machine learning classification models
4. Apply 5-Fold Cross-Validation to each model
5. Calculate the cross-validation scores
6. Calculate the average score for each model
7. Compare the performance of the models
8. Identify the best-performing algorithm

---

## Cross-Validation Implementation

Scikit-learn's `cross_val_score()` function was used to perform Cross-Validation.

```python
from sklearn.model_selection import cross_val_score

scores = cross_val_score(
    model,
    x,
    y,
    cv=5
)

print(scores)
print(scores.mean())