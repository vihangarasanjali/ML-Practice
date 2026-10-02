# Random Forest Classification - Iris Dataset

## Overview

This exercise demonstrates how to build, train, evaluate, save, and load a **Random Forest Classifier** using the Iris dataset with Python and Scikit-learn.

Two different model persistence methods are demonstrated:

- `joblib`
- Python's built-in `pickle`

The saved models are then loaded and used to make predictions on new Iris flower measurements.

---

## Dataset

The **Iris dataset** contains measurements of three species of Iris flowers:

- Setosa
- Versicolor
- Virginica

Each sample contains four features:

- Sepal Length
- Sepal Width
- Petal Length
- Petal Width

The dataset is loaded directly from Scikit-learn.

---

## Workflow

The project follows these steps:

1. Load the Iris dataset
2. Split the dataset into training and testing sets
3. Create a Random Forest Classifier
4. Train the model
5. Evaluate the model using accuracy
6. Save the trained model using `joblib`
7. Load the saved model
8. Make a prediction using new input data
9. Save the trained model using `pickle`
10. Load the model using `pickle`
11. Make another prediction

---

## Train-Test Split

The dataset is divided into:

- **80%** training data
- **20%** testing data

A `random_state` of `7` is used to make the split reproducible.

```python
X_train, X_test, Y_train, Y_test = train_test_split(
    dataset['data'],
    dataset['target'],
    test_size=0.2,
    random_state=7
)