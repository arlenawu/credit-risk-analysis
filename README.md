# credit-risk-analysis

# Overview
The purpose of this project is to predict the risk of customers not being able to pay back their loans using six different machine learning models -- RandomOverSampler, SMOTE, RandomUnderSampler, SMOTEENN, BalancedRandomForestClassifier, and EasyEnsembleClassifier.

# Results

### Logistic Regression
- **Oversampling (RandomOverSampler)**
  - Balanced Accuracy Score: 0.6603423204808787
  - Confusion Matrix:
    
    | 76 | 26 |
    |------|------|
    | **7,216** | **9,888** |
    
  - Imbalanced Classification Report

    |             | pre  | rec  | spe  | f1   | geo  | iba  | sup   |
    |-------------|------|------|------|------|------|------|-------|
    | high_risk   | 0.01 | 0.74 | 0.58 | 0.02 | 0.66 | 0.44 | 101   |
    | low_risk    | 1.00 | 0.58 | 0.74 | 0.73 | 0.66 | 0.42 | 17104 |
    | avg / total | 0.99 | 0.58 | 0.74 | 0.73 | 0.66 | 0.42 | 17205 |

- **SMOTE**
  - Balanced Accuracy Score: 0.6537310478007576
  - Confusion Matrix:
    
    | 62 | 38 |
    |------|------|
    | **5,410** | **11,694** |
    
  - Imbalanced Classification Report

    |             | pre  | rec  | spe  | f1   | geo  | iba  | sup   |
    |-------------|------|------|------|------|------|------|-------|
    | high_risk   | 0.01 | 0.62 | 0.68 | 0.02 | 0.65 | 0.42 | 101   |
    | low_risk    | 1.00 | 0.68 | 0.62 | 0.81 | 0.65 | 0.43 | 17104 |
    | avg / total | 0.99 | 0.68 | 0.62 | 0.81 | 0.65 | 0.43 | 17205 |

- **Undersampling (RandomUnderSampler)**
  - Balanced Accuracy Score: 0.5851708592281117
  - Confusion Matrix:
    
    | 65 | 36 |
    |------|------|
    | **8,094** | **9,010** |
    
  - Imbalanced Classification Report

    |             | pre  | rec  | spe  | f1   | geo  | iba  | sup   |
    |-------------|------|------|------|------|------|------|-------|
    | high_risk   | 0.01 | 0.64 | 0.53 | 0.02 | 0.58 | 0.34 | 101   |
    | low_risk    | 1.00 | 0.53 | 0.64 | 0.69 | 0.58 | 0.34 | 17104 |
    | avg / total | 0.99 | 0.53 | 0.64 | 0.69 | 0.58 | 0.34 | 17205 |

- **Combination (Over and Under) Sampling (SMOTEENN)**
  - Balanced Accuracy Score: 0.6447993752836463
  - Confusion Matrix:
    
    | 73 | 28 |
    |------|------|
    | **7,409** | **9,695** |
    
  - Imbalanced Classification Report

    |             | pre  | rec  | spe  | f1   | geo  | iba  | sup   |
    |-------------|------|------|------|------|------|------|-------|
    | high_risk   | 0.01 | 0.72 | 0.57 | 0.02 | 0.64 | 0.42 | 101   |
    | low_risk    | 1.00 | 0.57 | 0.72 | 0.72 | 0.64 | 0.40 | 17104 |
    | avg / total | 0.99 | 0.57 | 0.72 | 0.72 | 0.64 | 0.40 | 17205 |

### Emsemble Learners
- **Balanced Random Forest Classifier**
  - Balanced Accuracy Score: 0.7885466545953005
  - Confusion Matrix:
    
    | 71 | 30 |
    |------|------|
    | **2,153** | **14,951** |
    
  - Imbalanced Classification Report

    |             | pre  | rec  | spe  | f1   | geo  | iba  | sup   |
    |-------------|------|------|------|------|------|------|-------|
    | high_risk   | 0.03 | 0.70 | 0.87 | 0.06 | 0.78 | 0.60 | 101   |
    | low_risk    | 1.00 | 0.87 | 0.70 | 0.93 | 0.78 | 0.62 | 17104 |
    | avg / total | 0.99 | 0.87 | 0.70 | 0.93 | 0.78 | 0.62 | 17205 |

- **Easy Ensemble AdaBoost Classifier**
  - Balanced Accuracy Score: 0.7885466545953005
  - Confusion Matrix:
    
    | 71 | 30 |
    |------|------|
    | **2,153** | **14,951** |
    
  - Imbalanced Classification Report

    |             | pre  | rec  | spe  | f1   | geo  | iba  | sup   |
    |-------------|------|------|------|------|------|------|-------|
    | high_risk   | 0.03 | 0.70 | 0.87 | 0.06 | 0.78 | 0.60 | 101   |
    | low_risk    | 1.00 | 0.87 | 0.70 | 0.93 | 0.78 | 0.62 | 17104 |
    | avg / total | 0.99 | 0.87 | 0.70 | 0.93 | 0.78 | 0.62 | 17205 |

# Summary

