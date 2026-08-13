# K-Means Clustering - Customer Segmentation

## Overview

This exercise demonstrates the implementation of the **K-Means Clustering algorithm** using Python and Scikit-learn.

The goal is to group customers into different segments based on their **annual income** and **spending score**.

Since the dataset does not contain predefined customer categories, this is an **unsupervised machine learning** problem.

---

## Algorithm Used

### K-Means Clustering

K-Means is an **unsupervised machine learning algorithm** used to divide data points into a specified number of groups called **clusters**.

The algorithm works by:

1. Selecting K initial cluster centers (centroids)
2. Assigning each data point to its nearest centroid
3. Recalculating the centroid of each cluster
4. Repeating the process until the clusters stabilize

In this project, K-Means was used to identify different customer groups based on income and spending behavior.

---

## Dataset

The dataset used is `Customers.csv`.

The exercise uses two features from the dataset:

- `Annual Income (k$)`
- `Spending Score (1-100)`

These columns were renamed to:

- `Income`
- `Score`

for easier use in the analysis.

---

## Features Used

| Feature | Description |
|---|---|
| Income | Customer's annual income in thousands of dollars |
| Score | Customer's spending score from 1 to 100 |

---

## Technologies Used

- Python
- Pandas
- Matplotlib
- Scikit-learn
- Jupyter Notebook

---

## Workflow

The project follows these steps:

1. Load the customer dataset
2. Select annual income and spending score
3. Rename the selected columns
4. Visualize the customer data
5. Test different values of K
6. Calculate WCSS for each K value
7. Use the Elbow Method to determine a suitable number of clusters
8. Train the K-Means model
9. Assign customers to clusters
10. Visualize the resulting clusters and centroids

---

## Selecting the Number of Clusters

One of the important parameters in K-Means is the number of clusters, represented by **K**.

Different values of K from 1 to 10 were tested.

```python
k_values = [1,2,3,4,5,6,7,8,9,10]

wcss_error = []

for i in k_values:
    model = KMeans(n_clusters=i)
    model.fit(Data[['Income','Score']])
    wcss_error.append(model.inertia_)