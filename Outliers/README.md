# Outlier Detection Using Z-Score

## Overview

This project demonstrates how to identify and remove outliers from a dataset using the Z-score method.

The `insurance.csv` dataset is used, and outliers are detected based on the `charges` column.

## Dataset

The dataset contains insurance-related information, including:

- Age
- Sex
- BMI
- Number of children
- Smoking status
- Region
- Insurance charges

The analysis focuses on the `charges` column.

## Workflow

The project follows these steps:

1. Load the insurance dataset
2. Explore the dataset using `head()`, `shape`, and `describe()`
3. Visualize the distribution of insurance charges
4. Calculate the mean and standard deviation
5. Calculate the Z-score for each charge
6. Identify potential outliers
7. Remove observations with Z-scores outside the range of -3 to +3
8. Compare the data before and after removing outliers

## What is a Z-Score?

A Z-score indicates how far a value is from the mean in terms of standard deviations.

The formula is:

**Z = (x - mean) / standard deviation**

A large positive or negative Z-score indicates that the value is far from the average.

In this project, values with:

- Z-score > 3
- Z-score < -3

are treated as outliers.

## Detecting Outliers

The Z-score is calculated for each insurance charge:

```python
data['charges_z_score'] = (data['charges'] - mean) / std
```

The outlier indices are then identified:

```python
outlier_indices = data[
    (data['charges_z_score'] > 3) |
    (data['charges_z_score'] < -3)
].index
```

## Removing Outliers

The identified rows are removed from the dataset:

```python
new_data = data.drop(outlier_indices)
```

The temporary Z-score column is then removed:

```python
new_data = new_data.drop('charges_z_score', axis=1)
```

## Visualization

Histograms are used to visualize the distribution of insurance charges before and after removing outliers.

### Before Removing Outliers

```python
plt.hist(data['charges'])
plt.xlabel("Charges")
plt.ylabel("Count")
plt.show()
```

### After Removing Outliers

```python
plt.hist(new_data['charges'])
plt.xlabel("Charges")
plt.ylabel("Count")
plt.show()
```

Comparing the two histograms helps visualize how the distribution changes after removing extreme values.

## Libraries Used

- **NumPy** - numerical calculations
- **Pandas** - data loading and manipulation
- **Matplotlib** - data visualization

## Key Concepts Practiced

- Loading CSV data with Pandas
- Exploratory data analysis
- Mean and standard deviation
- Z-score calculation
- Outlier detection
- Removing outliers
- Data visualization