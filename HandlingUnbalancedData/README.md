# Handling Imbalanced Data

## Overview

This exercise demonstrates different techniques for handling **imbalanced datasets** using Python and the `imbalanced-learn` library.

The `kyphosis.csv` dataset is used to demonstrate:

- Random Under Sampling
- Random Over Sampling
- SMOTE (Synthetic Minority Over-sampling Technique)

The goal is to balance the target classes and observe how the class distribution changes after applying each technique.

## Dataset

The dataset contains information related to **Kyphosis**, a spinal disorder.

The `Kyphosis` column is used as the target variable, while the remaining columns are used as input features.

## Workflow

The project follows these steps:

1. Load the Kyphosis dataset
2. Separate the features and target variable
3. Check the original class distribution
4. Visualize the class distribution
5. Apply Random Under Sampling
6. Apply Random Over Sampling
7. Apply SMOTE
8. Compare the class distributions after each technique

## What is Imbalanced Data?

An imbalanced dataset is a dataset where one class contains significantly more observations than another class.

For example:

- Class A: 80 observations
- Class B: 20 observations

In this situation, Class A is the majority class and Class B is the minority class.

Imbalanced data can cause machine learning models to favor the majority class and perform poorly when predicting the minority class.

## Why Handle Imbalanced Data?

Handling class imbalance is important because a model can achieve high accuracy while still performing poorly on the minority class.

Balancing the data can help the model learn patterns from both classes more effectively.

## Under Sampling

**Random Under Sampling** reduces the number of observations in the majority class.

This creates a more balanced dataset by removing some majority-class observations.

```python
from imblearn.under_sampling import RandomUnderSampler

undersample = RandomUnderSampler()

x_under, y_under = undersample.fit_resample(x, y)
```

The resulting class distribution can be checked using:

```python
y_under.value_counts()
```

## Over Sampling

**Random Over Sampling** increases the number of observations in the minority class by randomly duplicating existing minority-class samples.

```python
from imblearn.over_sampling import RandomOverSampler

oversample = RandomOverSampler()

x_over, y_over = oversample.fit_resample(x, y)
```

The resulting class distribution can be checked using:

```python
y_over.value_counts()
```

## SMOTE

**SMOTE (Synthetic Minority Over-sampling Technique)** creates synthetic samples for the minority class instead of simply duplicating existing samples.

```python
from imblearn.over_sampling import SMOTE

smote = SMOTE()

x_smote, y_smote = smote.fit_resample(x, y)
```

The resulting class distribution can be checked using:

```python
y_smote.value_counts()
```

## Visualization

Bar charts are used to visualize the class distribution before and after applying the balancing techniques.

### Original Data

```python
y.value_counts().plot(kind='bar')
```

### After Under Sampling

```python
y_under.value_counts().plot(kind='bar')
```

### After Over Sampling

```python
y_over.value_counts().plot(kind='bar')
```

### After SMOTE

```python
y_smote.value_counts().plot(kind='bar')
```

These visualizations make it easier to compare the class distributions produced by each technique.

## Libraries Used

- **NumPy** - numerical operations
- **Pandas** - data loading and manipulation
- **Matplotlib** - data visualization
- **imbalanced-learn** - techniques for handling imbalanced datasets

## Key Concepts Practiced

- Class imbalance
- Majority and minority classes
- Random Under Sampling
- Random Over Sampling
- SMOTE
- Class distribution
- Data visualization
- `fit_resample()`