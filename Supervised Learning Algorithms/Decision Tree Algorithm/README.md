# Decision Tree - Student Performance Prediction

## Overview

This project demonstrates the implementation of a **Decision Tree Classification algorithm** using Python and Scikit-learn.

The goal of this project is to predict a student's final grade based on academic and personal factors such as study hours, attendance, subject scores, and other attributes.

A Decision Tree is a supervised machine learning algorithm that makes predictions by learning decision rules from the training data.

---

# Algorithm Used

## Decision Tree Classifier

A Decision Tree works by splitting data into smaller groups based on feature conditions and creating a tree-like structure for making predictions.

The model learns rules such as:

```
If study hours are high
    |
    Predict better grade
```

The final prediction is obtained from the leaf nodes of the tree.

---

# Dataset

The dataset contains student information and academic performance details.

## Features Used

| Feature | Description |
|---|---|
| age | Student age |
| gender | Student gender |
| school_type | Type of school |
| parent_education | Parent education level |
| study_hours | Daily study hours |
| attendance_percentage | Attendance percentage |
| internet_access | Availability of internet |
| travel_time | Travel time to school |
| extra_activities | Participation in extra activities |
| study_method | Preferred study method |
| math_score | Mathematics score |
| science_score | Science score |
| english_score | English score |

## Target Variable

| Target | Description |
|---|---|
| final_grade | Student's final grade |

Example classes:

```
A
B
C
D
E
```

---

# Data Preprocessing

## Removing Unnecessary Columns

The following columns were removed:

```python
student_id
overall_score
```

Reasons:

- `student_id` is only an identifier and does not contribute to prediction.
- `overall_score` was removed to avoid data leakage because it is directly related to the final grade.

---

## Handling Categorical Features

Machine learning algorithms cannot directly process text values.

Example:

```
gender:
male
female
```

Therefore, categorical variables were converted into numerical values using **One-Hot Encoding**.

Implementation:

```python
OneHotEncoder(handle_unknown="ignore")
```

Numerical columns were kept unchanged using:

```python
remainder="passthrough"
```

---

# Model Training

The dataset was divided into:

- Training data: 80%
- Testing data: 20%

Code:

```python
train_test_split(
    x,
    y,
    test_size=0.2,
    random_state=0
)
```

The Decision Tree model was created using:

```python
from sklearn.tree import DecisionTreeClassifier

model = DecisionTreeClassifier()

model.fit(x_train, y_train)
```

---

# Prediction

The trained model was used to predict grades for unseen test data.

```python
pred = model.predict(x_test)
```

---

# Model Evaluation

## Accuracy Score

Accuracy measures the percentage of correct predictions.

```python
accuracy_score(y_test, pred)
```

---

## Confusion Matrix

A confusion matrix shows the comparison between actual and predicted classes.

```python
confusion_matrix(y_test, pred)
```

It helps analyze:

- Correct predictions
- Incorrect predictions
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

- How Decision Tree algorithms work
- Difference between numerical and categorical features
- How to preprocess real-world datasets
- One-hot encoding techniques
- Training classification models
- Evaluating models using accuracy and confusion matrix
- Handling multi-class classification problems

---

