# Gradient Descent from Scratch

**Dataset:** Generated via `sklearn.make_regression` (300 samples, 5 features)  
**Tools:** Python, NumPy, Matplotlib  
**Language:** Russian  

## What's inside

Implementation and comparison of gradient descent variants for linear regression - built from scratch using NumPy only, without sklearn's solver.

**Steps covered:**
- Batch Gradient Descent implementation from scratch
- Learning rate experiments (η = 0.001 → 0.5)
- Stochastic Gradient Descent implementation
- BGD vs SGD comparison on the same data
- L2 regularization (Ridge): weight shrinkage as α grows

## Key Findings

| Experiment | Result |
|------------|--------|
| Best learning rate | η = 0.1 — converged in 112 iterations |
| η = 0.001 | Too slow, MSE ~1597 after 500 iterations |
| η = 0.5 | Diverges |
| BGD vs SGD | BGD: smooth convergence to MSE 216.67; SGD: noisy, MSE 609 after 300 iter |
| L2 regularization | All weights shrink toward 0 as α increases; uninformative features suppressed first |

## Files
- [`Gradient_Descent.ipynb`](./Gradient_Descent.ipynb) — full notebook (Russian)
