# Hierarchical Agglomerative Clustering

This exercise demonstrates **Hierarchical Agglomerative Clustering** using Python and scikit-learn. The exercise also visualizes the hierarchical structure of the data using a **dendrogram**.

## Technologies Used

- Python
- Pandas
- Matplotlib
- SciPy
- Scikit-learn

## Dataset

A small manually created dataset containing two numerical features:

- `x`
- `y`

The dataset contains 8 data points labeled from **A to H**.

## Implementation

The exercise performs the following steps:

1. Create the dataset using Pandas.
2. Visualize the data points using a scatter plot.
3. Generate a hierarchical clustering dendrogram using SciPy.
4. Apply **Agglomerative Hierarchical Clustering** using:
   - `n_clusters = 2`
   - `metric = 'euclidean'`
   - `linkage = 'ward'`
5. Assign each data point to a cluster.
6. Separate the data points into the two resulting clusters.
7. Visualize the final clusters using a scatter plot.

## Clustering Configuration

```python
AgglomerativeClustering(
    n_clusters=2,
    metric='euclidean',
    linkage='ward'
)