# Feature Selection - Machine Learning

## Overview

Feature Selection is a **machine learning preprocessing technique** used to select the most useful features from a dataset.

A feature is an input variable or column used by a machine learning model. Feature selection removes features that are:

- Irrelevant
- Redundant
- Constant
- Highly correlated with other features

This can help reduce model complexity, improve efficiency, reduce overfitting, and make models easier to interpret.

---

# Supervised Feature Selection

In supervised learning, feature selection uses the **target variable (`y`)** to determine which features are useful.

Two common approaches demonstrated here are:

- Mutual Information for Regression
- Mutual Information for Classification

---

## Mutual Information - Regression

Mutual Information measures how much information one variable provides about another variable.

For regression, `mutual_info_regression` is used to measure the relationship between each feature and the continuous target.

## Mutual Information - Classification

For classification problems, mutual_info_classif is used instead of mutual_info_regression.