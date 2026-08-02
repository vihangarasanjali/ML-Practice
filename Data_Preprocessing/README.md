# One-Hot Encoding and Label Encoding

## Overview

This project demonstrates how to convert **categorical data into numerical values** using **Label Encoding** and **One-Hot Encoding** with Scikit-learn.

These preprocessing techniques are commonly used before training machine learning models.

## Techniques Used

### Label Encoding

Label Encoding converts each category into a unique numerical value.

Example:

| Colour | Encoded Value |
|--------|---------------|
| Blue | 0 |
| Green | 1 |
| Red | 2 |

Implemented using:

```python
from sklearn.preprocessing import LabelEncoder

encoder = LabelEncoder()
encoded = encoder.fit_transform(colour_category)
```

### One-Hot Encoding

One-Hot Encoding creates a separate binary column for each category.

Example:

| Colour | Blue | Green | Red |
|--------|------|-------|-----|
| Red | 0 | 0 | 1 |
| Blue | 1 | 0 | 0 |
| Green | 0 | 1 | 0 |

Implemented using:

```python
from sklearn.preprocessing import LabelBinarizer

encoder = LabelBinarizer()
encoded = encoder.fit_transform(colour_category)
```

## Technologies Used

- Python
- Pandas
- Scikit-learn
- Jupyter Notebook

## Workflow

1. Load the dataset
2. Extract the categorical column
3. Apply Label Encoding
4. Apply One-Hot Encoding
5. View the encoded output
6. Examine the generated class labels

## Learning Outcome

Through this exercise, I learned:

- How to encode categorical variables
- The difference between Label Encoding and One-Hot Encoding
- How to use `LabelEncoder`
- How to use `LabelBinarizer`
- Why preprocessing is important in machine learning

## Project Structure

```text
One_Hot_Encoding/
│
├── colours.csv
├── one_hot_encoding.ipynb
└── README.md
```

This project is part of my **Machine Learning preprocessing practice**, focusing on preparing categorical data for machine learning algorithms.