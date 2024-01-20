# NPSLE Classification Project

## Project Overview

This project aims to classify patients into three categories: NPSLE (Neuropsychiatric Systemic Lupus Erythematosus), SLE (Systemic Lupus Erythematosus), and controls, based on MRI-derived features obtained with Volbrain. We have applied various machine learning algorithms to achieve this classification task.

## Results

### Logistic Regression
- Accuracy on Test Set: 0.3
- Confusion Matrix:
[[0 4 0]
[3 0 0]
[0 0 3]]

Comments: The Logistic Regression model achieved a relatively low accuracy on the test set. It struggled to differentiate between the three classes, as indicated by the confusion matrix.

### Support Vector Machine (SVM)
- Average Cross-Validation Accuracy: 0.7536
- Accuracy on Test Set: 0.7
- Classification Report:
               precision    recall  f1-score   support

           0       0.00      0.00      0.00         3
           1       0.40      1.00      0.57         2
           2       1.00      1.00      1.00         5

    accuracy                           0.70        10
   macro avg       0.47      0.67      0.52        10
weighted avg       0.58      0.70      0.61        10

Comments: The SVM model showed improved performance compared to Logistic Regression. It achieved a higher accuracy on the test set and provided a detailed classification report. However, further analysis of class-specific metrics is needed.

### Random Forest (RF)
- Average Cross-Validation Accuracy: 0.725
- Accuracy on Test Set: 0.6

- Classification Report:
               precision    recall  f1-score   support

           0       0.20      1.00      0.33         1
           1       1.00      0.20      0.33         5
           2       1.00      1.00      1.00         4

    accuracy                           0.60        10
   macro avg       0.73      0.73      0.56        10
weighted avg       0.92      0.60      0.60        10
  
Comments: The Random Forest model demonstrated competitive performance, with decent cross-validation accuracy. However, the accuracy on the test set was lower than the SVM model.

### XGBoost
- Confusion Matrix:
[[2 1 0]
[1 1 0]
[0 0 4]]

- Accuracy: 0.78
- Balanced Accuracy: 0.72
- Micro Precision: 0.78
- Micro Recall: 0.78
- Micro F1-score: 0.78
- Macro Precision: 0.72
- Macro Recall: 0.72
- Macro F1-score: 0.72
- Weighted Precision: 0.78
- Weighted Recall: 0.78
- Weighted F1-score: 0.78

- Classification Report:
  precision    recall  f1-score   support

           0       0.67      0.67      0.67         3
           1       0.50      0.50      0.50         2
           2       1.00      1.00      1.00         4

    accuracy                           0.78         9
   macro avg       0.72      0.72      0.72         9
weighted avg       0.78      0.78      0.78         9

Comments: XGBoost outperformed other models with a high accuracy of 0.78 on the test set. It also provided a balanced accuracy and detailed classification report with strong metrics across various categories.

## Conclusion

Summarize the key findings from your results. In this project, we experimented with different machine learning models to classify patients with NPSLE, SLE, and controls based on MRI-derived features. XGBoost emerged as the top-performing model, achieving the highest accuracy and balanced metrics on the test set. Further analysis and fine-tuning may be required to improve classification performance, especially for Logistic Regression and Random Forest models.

