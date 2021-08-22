# credit-risk-analysis

# Overview
The purpose of this project is to develop a model that can predict the risk of customers not being able to pay back their loans. Six different machine learning models were tested -- RandomOverSampler, SMOTE, RandomUnderSampler, SMOTEENN, BalancedRandomForestClassifier, and EasyEnsembleClassifier. Positive predictions indicate a customer who has a high risk level.

# Results

### Logistic Regression
- **Oversampling (RandomOverSampler)**
  - Balanced Accuracy Score: 0.660
  - Confusion Matrix:
    
    |                 | Predicted Positive | Predicted Negative |
    |-----------------|--------------------|--------------------|
    | Actual Positive |         76 	   |         26         |
    | Actual Negative |        7,216       |       9,888        |
    
  - Imbalanced Classification Report

    |             | pre  | rec  | spe  | f1   | geo  | iba  | sup   |
    |-------------|------|------|------|------|------|------|-------|
    | high_risk   | 0.01 | 0.74 | 0.58 | 0.02 | 0.66 | 0.44 | 101   |
    | low_risk    | 1.00 | 0.58 | 0.74 | 0.73 | 0.66 | 0.42 | 17104 |
    | avg / total | 0.99 | 0.58 | 0.74 | 0.73 | 0.66 | 0.42 | 17205 |

- **SMOTE**
  - Balanced Accuracy Score: 0.654
  - Confusion Matrix:
    
    |                 | Predicted Positive | Predicted Negative |
    |-----------------|--------------------|--------------------|
    | Actual Positive |         62 	   |         38         |
    | Actual Negative |        5,410       |       11,694       |
    
  - Imbalanced Classification Report

    |             | pre  | rec  | spe  | f1   | geo  | iba  | sup   |
    |-------------|------|------|------|------|------|------|-------|
    | high_risk   | 0.01 | 0.62 | 0.68 | 0.02 | 0.65 | 0.42 | 101   |
    | low_risk    | 1.00 | 0.68 | 0.62 | 0.81 | 0.65 | 0.43 | 17104 |
    | avg / total | 0.99 | 0.68 | 0.62 | 0.81 | 0.65 | 0.43 | 17205 |

- **Undersampling (RandomUnderSampler)**
  - Balanced Accuracy Score: 0.585
  - Confusion Matrix:
    
    |                 | Predicted Positive | Predicted Negative |
    |-----------------|--------------------|--------------------|
    | Actual Positive |         65 	   |         36         |
    | Actual Negative |        8,094       |       9,010        |
    
  - Imbalanced Classification Report

    |             | pre  | rec  | spe  | f1   | geo  | iba  | sup   |
    |-------------|------|------|------|------|------|------|-------|
    | high_risk   | 0.01 | 0.64 | 0.53 | 0.02 | 0.58 | 0.34 | 101   |
    | low_risk    | 1.00 | 0.53 | 0.64 | 0.69 | 0.58 | 0.34 | 17104 |
    | avg / total | 0.99 | 0.53 | 0.64 | 0.69 | 0.58 | 0.34 | 17205 |

- **Combination (Over and Under) Sampling (SMOTEENN)**
  - Balanced Accuracy Score: 0.681
  - Confusion Matrix:
    
    |                 | Predicted Positive | Predicted Negative |
    |-----------------|--------------------|--------------------|
    | Actual Positive |         78 	   |         23         |
    | Actual Negative |        7,024       |       10,080       |
    
  - Imbalanced Classification Report

    |             | pre  | rec  | spe  | f1   | geo  | iba  | sup   |
    |-------------|------|------|------|------|------|------|-------|
    | high_risk   | 0.01 | 0.77 | 0.59 | 0.02 | 0.67 | 0.46 | 101   |
    | low_risk    | 1.00 | 0.59 | 0.77 | 0.74 | 0.67 | 0.45 | 17104 |
    | avg / total | 0.99 | 0.59 | 0.77 | 0.74 | 0.67 | 0.45 | 17205 |

### Ensemble Learners
- **Balanced Random Forest Classifier**
  - Balanced Accuracy Score: 0.789
  - Confusion Matrix:
    
    |                 | Predicted Positive | Predicted Negative |
    |-----------------|--------------------|--------------------|
    | Actual Positive |         71         |         30         |
    | Actual Negative |        2,153       |       14,951       |
    
  - Imbalanced Classification Report

    |             | pre  | rec  | spe  | f1   | geo  | iba  | sup   |
    |-------------|------|------|------|------|------|------|-------|
    | high_risk   | 0.03 | 0.70 | 0.87 | 0.06 | 0.78 | 0.60 | 101   |
    | low_risk    | 1.00 | 0.87 | 0.70 | 0.93 | 0.78 | 0.62 | 17104 |
    | avg / total | 0.99 | 0.87 | 0.70 | 0.93 | 0.78 | 0.62 | 17205 |

- **Easy Ensemble AdaBoost Classifier**
  - Balanced Accuracy Score: 0.932
  - Confusion Matrix:
    
    |                 | Predicted Positive | Predicted Negative |
    |-----------------|--------------------|--------------------|
    | Actual Positive |         93         |         8          |
    | Actual Negative |         983        |       16,121       |
    
  - Imbalanced Classification Report

    |             | pre  | rec  | spe  | f1   | geo  | iba  | sup   |
    |-------------|------|------|------|------|------|------|-------|
    | high_risk   | 0.09 | 0.92 | 0.94 | 0.16 | 0.93 | 0.87 | 101   |
    | low_risk    | 1.00 | 0.94 | 0.92 | 0.97 | 0.93 | 0.87 | 17104 |
    | avg / total | 0.99 | 0.94 | 0.92 | 0.97 | 0.93 | 0.87 | 17205 |

# Summary



Based on the results, it appears that the Easy Ensemble AdaBoost Classifier is by far the most effective model to predict high risk customers, and is the only model with less than 2,000 false positives. All other models have a large quantity of false predictions, and very low accuracy and sensitivity scores as a result.