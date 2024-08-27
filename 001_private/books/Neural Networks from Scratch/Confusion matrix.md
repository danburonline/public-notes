#core/machinelearning

![[confusion-matrix.png]]

A confusion matrix is a **tool often used in classification to visualise the performance of an algorithm.** It’s a table with two dimensions: “actual” and “predicted”. Here’s a breakdown of its components:

1. **True Positives (TP):** These are cases in which the model correctly predicted the positive class. For example, if your model predicts whether an email is spam, this would be the spam emails the model correctly identified as spam.
2. **True Negatives (TN):** These are cases in which the model correctly predicted the negative class. In the spam email example, these would be the non-spam emails the model correctly identified as not spam.
3. **False Positives (FP):** These occur when the model incorrectly predicts the positive class. In the spam example, these would be non-spam emails that the model incorrectly identified as spam. This type of error is also known as a “Type I error” or “False Alarm”.
4. **False Negatives (FN):** These occur when the model incorrectly predicts the negative class. In the spam example, these would be spam emails that the model failed to identify and marked as non-spam. This is also called a “Type II error” or “Miss”.

The matrix is typically set up with actual values in rows and predicted values in columns, or vice versa. It’s a very useful tool because it tells you about the errors the model is making and the type of errors. Various performance metrics like accuracy, precision, recall, and [[README#Core|F1-score]] can be calculated from the confusion matrix. These metrics provide deeper insights into the effectiveness of the classification model.

- **Accuracy:** This measures the overall correctness of the model and is calculated as (TP + TN) / (TP + TN + FP + FN).
- **Precision:** This indicates the proportion of positive identifications that were actually correct, calculated as TP / (TP + FP).
- **Recall (or Sensitivity):** This measures the proportion of actual positives that were correctly identified, calculated as TP / (TP + FN).
- **F1 Score:** This is a harmonic mean of precision and recall, balancing them. It’s calculated as 2 \* (Precision * Recall) / (Precision + Recall).
