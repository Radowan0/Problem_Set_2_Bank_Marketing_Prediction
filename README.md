## Bank Marketing Prediction — Logistic Regression

This project predicts whether a customer will subscribe to a **term deposit** based on demographic and banking information.

The dataset used is **bank-full.csv**, containing **41,188 rows** and **17 features**.

---

## Objective
To build a **Logistic Regression model** that predicts:
- **1 → Customer subscribes (yes)**
- **0 → Customer does not subscribe (no)**

---

## Dataset Description

The dataset contains the following attributes:

- age  
- job  
- marital  
- education  
- default  
- balance  
- housing  
- loan  
- contact  
- day  
- month  
- duration  
- campaign  
- pdays  
- previous  
- poutcome  
- **y (target)** → yes/no

---

## Data Preprocessing

- Converted output labels:  
  `yes → 1`, `no → 0`
- Identified all categorical columns.
- Applied **One-Hot Encoding** using `ColumnTransformer`.
- No scaling was used (as required in assignment).
- Split dataset into **80% training / 20% testing**.

---

## Model Used: Logistic Regression

Logistic Regression is ideal for binary classification:
- Outputs probability of subscribing  
- Easy to interpret  
- Computationally efficient  

Model used:

python 

 ```LogisticRegression(max_iter=1000) ```

---

## Model Performance

Test Accuracy: ~88%

Classification Report:
- Precision (yes): ~0.54
- Recall (yes): ~0.33
- F1-score (yes): ~0.41
- Precision (no): ~0.92
- Recall (no): ~0.97


```text
Confusion Matrix:

                Predicted No     Predicted Yes
Actual No            7781             230
Actual Yes            892             435
```

ROC-AUC Score: ~0.90

The model performs well, especially identifying "no" class, which is the majority.

---

## ROC Curve
The ROC curve shows a strong separability with AUC ≈ 0.90.

---

## Conclusion
Logistic Regression works effectively for this dataset with 88% accuracy. The model predicts non-subscribers more accurately (dataset imbalance). AUC score of 0.90 indicates strong predictive power. One-hot encoding was essential due to many categorical variables.This model can help banks identify likely customers for marketing campaigns.

