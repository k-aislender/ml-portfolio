# Binary Classification: Bank Loan Default Prediction

**Dataset:** Banking Customer Details with Credit Ratings (Kaggle)  
**Tools:** Python, Pandas, Scikit-learn, Matplotlib, Seaborn  
**Language:** Russian  

## Business Problem

Predict whether a bank client will default on a loan based on demographic
and financial features. Key challenge: class imbalance (76% no default / 24% default).

## What's inside

- Data preprocessing: missing target labels removal, outlier analysis (IQR ×3.0)
- Scatter plot validation: confirmed high `employ` values are real, not errors
- Three classifiers trained and compared: Logistic Regression, SVM (RBF kernel), Decision Tree (CART)
- Hyperparameter tuning: `max_depth` and `min_samples_leaf` selected empirically via F1-score plots
- Class imbalance handled via `class_weight='balanced'`
- Full evaluation: Accuracy, Precision, Recall, F1, ROC-AUC, confusion matrices, ROC curves
- Feature importance analysis (Gini)

## Model Comparison

| Model | Accuracy | Precision | Recall | F1 | ROC-AUC |
|-------|----------|-----------|--------|----|---------|
| Logistic Regression | ~0.692 | ~0.426 | ~0.697 | ~0.531 | **0.789** |
| SVM (RBF) | ~0.679 | ~0.375 | **0.788** | **0.553** | ~0.782 |
| Decision Tree (CART) | ~0.679 | ~0.393 | ~0.727 | ~0.510 | ~0.756 |

## Key Findings

- Most important features: `employ` (Gini importance ~0.57), `creddebt`, `debtinc`
- SVM leads on Recall and F1 - best for minimizing missed defaults (dangerous for a bank)
- Logistic Regression leads on ROC-AUC - best for ranking clients by risk score
- Decision Tree: most interpretable, good for explaining decisions to business stakeholders

## Files
- [`Binary_Classification_Bankloan.ipynb`](./Binary_Classification_Bankloan.ipynb) — full notebook (Russian)
