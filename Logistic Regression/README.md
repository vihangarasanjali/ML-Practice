# Logistic Regression - Cancer Prediction

## Overview

This project demonstrates the implementation of a **Logistic Regression machine learning algorithm** using Python and Scikit-learn.

The goal is to predict whether a person is a cancer patient or not based on their age.

## Algorithm Used

### Logistic Regression

Logistic Regression is a supervised machine learning algorithm used for classification problems.

In this project:

- Input feature: Age
- Target variable: Cancer patient or not
- Output:
  - 1 → Cancer patient
  - 0 → Not a cancer patient

## Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- Jupyter Notebook

## Workflow

1. Load the dataset using Pandas
2. Visualize the relationship between age and cancer status
3. Separate features (X) and target (Y)
4. Split the dataset into training and testing sets
5. Train a Logistic Regression model
6. Make predictions
7. Evaluate the model accuracy

## Dataset

The dataset contains:

| Feature | Description |
|---------|-------------|
| age | Age of the person |
| cancer_patient_or_not | Target label indicating cancer status |

## Model Training

The dataset was divided into:

- Training data: 80%
- Testing data: 20%

The model was trained using:

class LogisticRegression:
pass

```python
LogisticRegression()
```

## Prediction Example

The trained model can predict cancer status for new age values:

```python
age = [[3]]
model.predict(age)
```

## Evaluation

The model performance was evaluated using accuracy score:

```python
model.score(x_test, y_test)
```

## Learning Outcome

Through this exercise, I learned:

- How supervised learning works
- Difference between classification and regression
- How Logistic Regression performs binary classification
- How to train and evaluate a machine learning model