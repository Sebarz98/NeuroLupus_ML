# NPSLE Classification Project

## Project Overview

This project aims to classify patients into three categories: NPSLE (Neuropsychiatric Systemic Lupus Erythematosus), SLE (Systemic Lupus Erythematosus), and controls, based on MRI-derived features obtained with Volbrain. We have applied various machine learning algorithms to achieve this classification task.

## Results

### Machine Learning

#### Logistic Regression
- Accuracy on Test Set: 0.6
- Classification Report:
               precision    recall  f1-score   support

           0       0.00      0.00      0.00         2
           1       0.00      0.00      0.00         2
           2       1.00      1.00      1.00         6

#### Support Vector Machine (SVM)
- Average Cross-Validation Accuracy: 0.76
- Accuracy on Test Set: 0.8
- Classification Report:
               precision    recall  f1-score   support

           0       0.50      0.50      0.50         2
           1       0.50      0.50      0.50         2
           2       1.00      1.00      1.00         6

#### Random Forest (RF)
- Accuracy on Test Set: 0.9
- Average Cross-Validation Accuracy: 0.75
- Classification Report:
               precision    recall  f1-score   support

           0       1.00      0.67      0.80         3
           1       0.75      1.00      0.86         3
           2       1.00      1.00      1.00         4

#### XGBoost
Accuracy: 0.67
Balanced Accuracy: 0.61

Micro Precision: 0.67
Micro Recall: 0.67
Micro F1-score: 0.67

Macro Precision: 0.72
Macro Recall: 0.61
Macro F1-score: 0.60

Weighted Precision: 0.74
Weighted Recall: 0.67
Weighted F1-score: 0.63

--------------- Classification Report ---------------

              precision    recall  f1-score   support

           0       1.00      0.33      0.50         3
           1       0.50      0.50      0.50         2
           2       0.67      1.00      0.80         4

### Ensemble Learning

#### Voting Classifier
- Average Cross-Validation Accuracy: 0.75
- Accuracy on Test Set: 0.8
- Classification Report:
               precision    recall  f1-score   support

           0       0.50      0.50      0.50         2
           1       0.50      0.50      0.50         2
           2       1.00      1.00      1.00         6

#### Stacking Classifier 
- Average Cross-Validation Accuracy: 0.67
- Accuracy on Test Set: 0.6
- Classification Report:
               precision    recall  f1-score   support

           0       0.33      0.33      0.33         3
           1       0.33      0.33      0.33         3
           2       1.00      1.00      1.00         4

#### Extremely Randomized Trees 
- Average Accuracy: 0.53
- Classification Report:
               precision    recall  f1-score   support

           0       0.15      0.15      0.15        13
           1       0.21      0.21      0.21        14
           2       1.00      1.00      1.00        20


## Conclusion

In this project, we experimented with different machine learning models to classify patients with NPSLE, SLE, and controls based on MRI-derived features. Random Forest emerged as the top-performing model, achieving the highest accuracy and balanced metrics on the test set. Further analysis and fine-tuning may be required to improve classification performance, especially regarding the correct classification of NPSLE patients.
On this note, we tried to deploy the SVM model to classifify NPSLE patients from HC, showing an accuracy of 100%. This further supports the findings of all the models, as they struggled to differentiate between SLE and NPSLE, but not between HC and the other groups.

### Plots

![Alt text](results/confusion.png)

 Confusion matrix of RF Model.


 ![Alt text](results/features.png)

Most relevant features of RF Model.


![Alt text](results/SVM.png)

Different classes plotted on the first two PC of SVM.