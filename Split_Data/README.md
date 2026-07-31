# Dataset Splitting with Scikit-Learn

## Overview
This exercise demonstrates how to split a dataset into training and testing sets using Scikit-Learn's `train_test_split()` function.

Dataset splitting is an important step in machine learning because it allows us to:
- Train a model using the training data.
- Evaluate the model's performance using unseen testing data.
- Reduce the risk of overfitting.

## Technologies Used
- Python
- NumPy
- Scikit-Learn

## Concepts Covered
- Creating sample datasets using NumPy arrays.
- Splitting data into training and testing sets.
- Understanding `test_size` and `random_state` parameters.

## Implementation

```python
from sklearn.model_selection import train_test_split
import numpy as np

# Sample dataset
x = np.array([1,2,3,4,5,6,7,8,9,10,
              11,12,13,14,15,16,17,18,19,20])

y = np.array([0,0,1,0,1,0,0,0,0,0,
              1,1,1,0,1,0,1,1,1,1])

# Split dataset into training and testing sets
x_train, x_test, y_train, y_test = train_test_split(
    x, 
    y, 
    test_size=0.2, 
    random_state=10
)

print("Training Features:", x_train)
print("Testing Features:", x_test)
print("Training Labels:", y_train)
print("Testing Labels:", y_test)