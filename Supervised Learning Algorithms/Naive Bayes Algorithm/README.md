# Naive Bayes - Student Performance Classification

## Overview

This exercise demonstrates the implementation of the **Naive Bayes machine learning algorithm** using Python and Scikit-learn.

The goal is to predict a student's **final grade** based on their demographic information, study habits, attendance, subject scores, and other academic-related features.

This is a **multi-class classification** problem because the target variable contains multiple possible classes such as A, B, C, D, and E.

---

## Algorithm Used

### Gaussian Naive Bayes

Naive Bayes is a supervised machine learning algorithm based on **Bayes' theorem**.

It predicts the most probable class based on the given input features.

The algorithm makes a "naive" assumption that the features are independent of each other.

In this project, **Gaussian Naive Bayes** is used because the dataset contains numerical features such as:

- Age
- Study hours
- Attendance percentage
- Math score
- Science score
- English score

---

## Dataset

The dataset used is `Student_Performance.csv`.

The dataset contains information about students and their academic performance.

### Features

| Feature | Description |
|---|---|
| age | Age of the student |
| gender | Gender of the student |
| school_type | Type of school |
| parent_education | Parent's education level |
| study_hours | Number of hours spent studying |
| attendance_percentage | Student attendance percentage |
| internet_access | Whether the student has internet access |
| travel_time | Time taken to travel to school |
| extra_activities | Participation in extra activities |
| study_method | Preferred study method |
| math_score | Mathematics score |
| science_score | Science score |
| english_score | English score |

The following columns were not used as input features:

- `student_id` – Identifier only
- `overall_score` – Directly related to the final grade
- `final_grade` – Target variable

---

## Target Variable

The target variable is:

```python
final_grade