# NPSLE Classification Project

## Project Overview

This project aims to classify patients into three categories: NPSLE (Neuropsychiatric Systemic Lupus Erythematosus), SLE (Systemic Lupus Erythematosus), and controls, based on MRI-derived features obtained with Volbrain. We have applied various machine learning algorithms to achieve this classification task.

## Model Results

### Logistic Regression

- **Accuracy on Test Set:** 0.60
- **Confusion Matrix:**
[[0 4 0]
[0 2 0]
[0 0 4]]

- **Classification Report:**
          precision    recall  f1-score   support
       0       0.00      0.00      0.00         4
       1       0.33      1.00      0.50         2
       2       1.00      1.00      1.00         4

accuracy 0.60 10
macro avg 0.44 0.67 0.50 10
weighted avg 0.47 0.60 0.50 10


### Support Vector Machine (SVM)

- **Average Cross-Validation Accuracy:** 0.87
- **Accuracy on Test Set:** 0.80
- **Classification Report:**
          precision    recall  f1-score   support
       0       1.00      0.50      0.67         4
       1       0.50      1.00      0.67         2
       2       1.00      1.00      1.00         4

accuracy 0.80 10
macro avg 0.83 0.83 0.78 10
weighted avg 0.90 0.80 0.80 10


### Random Forest (RF)

- **Accuracy:** 0.80
- **F1-Score:** 0.722
- **Recall:** 0.77
- **Precision:** 0.83
- **Balanced Accuracy:** 0.77

### XGBoost

- **Accuracy:** 0.80
- **Balanced Accuracy:** 0.83
- **Micro Precision:** 0.80
- **Micro Recall:** 0.80
- **Micro F1-score:** 0.80
- **Macro Precision:** 0.83
- **Macro Recall:** 0.83
- **Macro F1-score:** 0.78
- **Weighted Precision:** 0.90
- **Weighted Recall:** 0.80
- **Weighted F1-score:** 0.80

## Discussion

- The Logistic Regression model achieved an accuracy of 0.60 on the test set. It appears to struggle with the classification task, especially for class 0.

- In contrast, the SVM model showed improved performance with an accuracy of 0.80 on the test set. It demonstrates better classification results for class 0.

- The Random Forest model also performed well with an accuracy of 0.80. It shows a balanced performance with good precision, recall, and F1-score.

- XGBoost achieved an accuracy of 0.80 and shows balanced performance across multiple metrics, making it a strong candidate for further investigation.

## Conclusion

Based on the results, the SVM, Random Forest, and XGBoost models show promise in classifying patients with NPSLE, SLE, and controls based on MRI-derived features. Further fine-tuning and feature engineering may lead to even better performance. This project is ongoing, and additional experiments and optimizations will be conducted.






