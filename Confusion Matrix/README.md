---

# Model Evaluation

After training the Logistic Regression models, the performance was evaluated using:

- Confusion Matrix
- Accuracy
- Precision
- Recall
- F1-score
- Classification Report

## Confusion Matrix

A confusion matrix shows the comparison between actual values and predicted values.

It helps identify:

- True Positives (TP)
- True Negatives (TN)
- False Positives (FP)
- False Negatives (FN)

Example:

```
              Predicted
              0     1

Actual 0      TN    FP

Actual 1      FN    TP
```

---

## Evaluation Metrics

### Accuracy

Accuracy represents the percentage of correct predictions made by the model.

```
Accuracy = Correct Predictions / Total Predictions
```

---

### Precision

Precision measures how reliable the positive predictions are.

```
Precision = TP / (TP + FP)
```

It answers:

> "When the model predicts a class, how often is it correct?"

---

### Recall

Recall measures how many actual positive cases were successfully identified.

```
Recall = TP / (TP + FN)
```

It answers:

> "How many actual cases did the model find?"

---

### F1-score

F1-score is the balance between precision and recall.

It is useful when the dataset contains uneven class distributions.

---

## Classification Report

The classification report provides:

- Precision for each class
- Recall for each class
- F1-score for each class
- Support (number of samples in each class)
- Macro average
- Weighted average

### Macro Average

Macro average calculates the average performance of all classes while treating every class equally.

### Weighted Average

Weighted average considers the number of samples in each class when calculating the average.

---

## Learning Outcome

Through this project, I learned:

- How to evaluate classification models
- How to interpret confusion matrices
- Difference between accuracy, precision, recall, and F1-score
- How to analyze model performance using Scikit-learn classification reports