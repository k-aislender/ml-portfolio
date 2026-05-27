# Decision Tree from Scratch

**Dataset:** Synthetic (`sklearn.make_classification`, 300 samples, 4 features)  
**Tools:** Python, NumPy, Scikit-learn (for validation only)  
**Language:** Russian  

## Goal

Implement a Decision Tree classifier from scratch in pure Python/NumPy —
without using sklearn's tree implementation — and verify correctness by
comparing predictions with `DecisionTreeClassifier` from sklearn.

## What's inside

- `Node` and `Leaf` classes implemented manually
- Gini impurity calculated from scratch
- Information gain function with full formula
- Recursive `build_tree` with two stopping criteria: `max_depth` and `min_samples_leaf`
- `classify_object` and `predict` functions
- Tree structure printed as text (if-then rules)
- **Validation:** custom tree predictions match sklearn's 100% on test set
- Overfitting demonstration: comparison of unconstrained vs constrained tree

## Key Result

| Model | Train Accuracy | Test Accuracy |
|-------|---------------|---------------|
| Custom Decision Tree | — | matches sklearn |
| sklearn DecisionTree (same params) | — | same result |

Custom implementation fully reproduces sklearn's behavior with identical
`max_depth=5`, `min_samples_leaf=3`, Gini criterion.

## Overfitting Demo

| Config | Train Acc | Test Acc | Gap |
|--------|-----------|----------|-----|
| No constraints | ~1.000 | lower | high |
| max_depth=5, min_leaf=3 | lower | higher | reduced |
| max_depth=3, min_leaf=5 | balanced | balanced | minimal |

## Files
- [`Decision_Tree_from_Scratch.ipynb`](./Decision_Tree_from_Scratch.ipynb) — full notebook (Russian)
