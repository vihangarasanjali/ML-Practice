# Random Forest - Student Performance Prediction

## Overview

This project demonstrates the implementation of a **Random Forest Classification algorithm** using Python and Scikit-learn.

The goal of this project is to predict a student's final grade based on academic, personal, and behavioral factors such as study hours, attendance, subject scores, and other student attributes.

Random Forest is an ensemble machine learning algorithm that combines multiple decision trees to improve prediction accuracy and reduce overfitting.

---

# Algorithm Used

## Random Forest Classifier

Random Forest creates multiple Decision Trees and combines their predictions.

For classification problems, each tree gives a prediction and the final output is selected based on majority voting.

Example:

```
Decision Tree 1 → Grade A
Decision Tree 2 → Grade B
Decision Tree 3 → Grade A
Decision Tree 4 → Grade A

Final Prediction → Grade A
```

---

# Dataset

The dataset used is:

```
Student_Performance.csv
```

The dataset contains information about students and their academic performance.

## Features Used

| Feature | Description |
|---|---|
| age | Student age |
| gender | Student gender |
| school_type | Type of school |
| parent_education | Parent education level |
| study_hours | Daily study hours |
| attendance_percentage | Attendance percentage |
| internet_access | Internet availability |
| travel_time | Travel time to school |
| extra_activities | Participation in extra activities |
| study_method | Study method |
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

- `student_id` is only an identifier and does not provide predictive information.
- `overall_score` was removed to avoid data leakage because it is directly related to final grade calculation.

---

# Handling Categorical Features

Machine learning algorithms cannot directly process text values.

Example:

```
gender:
male
female
```

Therefore, categorical variables were converted into numerical representations using One-Hot Encoding.

Implementation:

```python
OneHotEncoder(handle_unknown="ignore")
```

Numerical columns were preserved using:

```python
remainder="passthrough"
```

---

# Model Training

The dataset was divided into:

- Training data: 80%
- Testing data: 20%

Implementation:

```python
train_test_split(
    x,
    y,
    test_size=0.2,
    random_state=0
)
```

The Random Forest model was created using:

```python
from sklearn.ensemble import RandomForestClassifier

model = RandomForestClassifier(
    n_estimators=100,
    random_state=0
)

model.fit(x_train, y_train)
```

---

# Model Parameters

## n_estimators

```
n_estimators=100
```

Defines the number of Decision Trees created inside the Random Forest.

In this project:

```
100 Decision Trees
```

were used.

---

## random_state

```
random_state=0
```

Ensures reproducible results by controlling randomness during model training.

---

# Prediction

The trained model predicts grades for unseen test data.

```python
pred = model.predict(x_test)
```

---

# Model Evaluation

## Accuracy Score

The model performance was evaluated using accuracy.

```python
accuracy_score(y_test, pred)
```

Results:

| Model | Accuracy |
|---|---|
| Random Forest | 90.10% |
| Decision Tree | 86.68% |

Random Forest achieved better performance compared to a single Decision Tree.

---

# Confusion Matrix

The confusion matrix was used to compare actual and predicted classes.

```python
confusion_matrix(y_test, pred)
```

It shows:

- Correct predictions
- Incorrect predictions
- Performance for each grade category

---

# Feature Importance Analysis

Random Forest provides feature importance values to understand which features contribute most to predictions.

Top important features:

| Feature | Importance |
|---|---:|
| study_hours | 0.200780 |
| science_score | 0.171951 |
| math_score | 0.170148 |
| english_score | 0.161648 |
| attendance_percentage | 0.084542 |

Interpretation:

- Study hours was the most influential feature.
- Subject scores contributed significantly to final grade prediction.
- Academic-related features had more impact than demographic features.

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

- How Random Forest algorithms work
- Difference between Decision Tree and Random Forest
- Ensemble learning concepts
- Handling categorical variables using One-Hot Encoding
- Training multi-class classification models
- Evaluating models using accuracy and confusion matrix
- Interpreting feature importance

---

