# Principal Component Analysis (PCA)

This folder contains practical examples of **Principal Component Analysis (PCA)** using Python and Scikit-learn.

PCA is a dimensionality reduction technique that transforms a dataset with many features into a smaller number of new features called **principal components**, while trying to preserve as much of the important variation in the data as possible.

---

## 📌 What is PCA?

Principal Component Analysis (PCA) is commonly used to:

* Reduce the number of features in a dataset
* Visualize high-dimensional data
* Remove redundant information
* Reduce computational cost for machine learning models
* Identify the directions in which the data varies the most

For example, if a dataset has **64 features**, PCA can transform those 64 features into 10 principal components.

Instead of working with:

```text
Feature 1
Feature 2
...
Feature 64
```

we can work with:

```text
PC1
PC2
...
PC10
```

The principal components are combinations of the original features.

---

# 1. PCA for Data Visualization

The first example uses the **Digits dataset** from Scikit-learn.

```python
from sklearn.datasets import load_digits

digits = load_digits()
```

The dataset contains images of handwritten digits.

Each image is:

```text
8 × 8 pixels = 64 features
```

Therefore:

```python
digits.data.shape
```

returns:

```text
(1797, 64)
```

There are 1797 images and each image has 64 pixel features.

---

## Visualizing an Individual Digit

The original image can be displayed using:

```python
import matplotlib.pyplot as plt

plt.matshow(digits.images[33])
plt.show()
```

The corresponding target tells us which digit the image represents:

```python
digits.target[33]
```

---

## Reducing 64 Features to 3 Components

PCA can reduce the 64-dimensional data into only 3 dimensions:

```python
from sklearn.decomposition import PCA

pca = PCA(n_components=3)
new
```
