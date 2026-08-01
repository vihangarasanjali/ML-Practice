# Logistic Regression - Binary & Multi-Class Classification

## Overview

This project demonstrates the implementation of a **Logistic Regression machine learning algorithm** using Python and Scikit-learn.

Two classification problems are implemented:

1. **Binary Classification** - Cancer prediction
2. **Multi-Class Classification** - Student performance prediction

Logistic Regression is a supervised machine learning algorithm mainly used for classification tasks.

---

# 1. Binary Classification - Cancer Prediction

## Problem Statement

The goal of this project is to predict whether a person is a cancer patient or not based on their age.

## Dataset

The dataset contains:

| Feature | Description |
|---------|-------------|
| age | Age of the person |
| cancer_patient_or_not | Target label indicating cancer status |

## Classification Type

This is a **binary classification problem** because there are only two possible outputs:

```
0 → Not a cancer patient
1 → Cancer patient
```

## Workflow

1. Load the dataset using Pandas
2. Visualize the relationship between age and cancer status
3. Separate features (X) and target variable (Y)
4. Split the dataset into training and testing sets
5. Train a Logistic Regression model
6. Make predictions
7. Evaluate model performance

## Model Training

The model was trained using:

```python
from sklearn.linear_model import LogisticRegression

model = LogisticRegression()

model.fit(x_train, y_train)
```

## Prediction Example

```python
age = [[3]]

model.predict(age)
```

## Evaluation

Model accuracy was evaluated using:

```python
model.score(x_test, y_test)
```

---

# 2. Multi-Class Classification - Student Performance Prediction

## Problem Statement

The goal of this project is to predict a student's performance category based on the number of hours studied.

## Dataset

The dataset contains:

| Feature | Description |
|---------|-------------|
| hours_studied | Number of hours studied |
| performance | Student performance category |

## Classification Type

This is a **multi-class classification problem** because the model predicts one class from multiple categories.

Classes:

```
Poor
Average
Good
Excellent
```

## Workflow

1. Load the dataset using Pandas
2. Separate features (X) and target variable (Y)
3. Split the dataset into training and testing sets
4. Train a Logistic Regression classifier
5. Predict student performance categories
6. Evaluate model accuracy

## Model Training

```python
from sklearn.linear_model import LogisticRegression

model = LogisticRegression()

model.fit(x_train, y_train)
```

## Prediction Example

Predict performance for a student who studied 6 hours:

```python
hours = [[6]]

model.predict(hours)
```

Example output:

```
['Good']
```

## Probability Prediction

The model can also predict the probability of each class:

```python
model.predict_proba(hours)
```

Example:

```
Poor        0.145868
Average     0.283383
Good        0.566161
Excellent   0.004588
```

The class with the highest probability is selected as the prediction.

---

# Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- Jupyter Notebook

---

# Concepts Learned

Through these exercises, I learned:

- Basics of supervised learning
- Difference between regression and classification
- Binary classification
- Multi-class classification
- Logistic Regression algorithm
- Training and testing machine learning models
- Model prediction and evaluation
- Working with datasets using Pandas

---

# Future Improvements

- Add more features to improve prediction accuracy
- Try other classification algorithms:
  - Decision Trees
  - Random Forest
  - Support Vector Machines
  - Neural Networks