# EDA: Superstore Sales

**Dataset:** [Superstore Sales (Kaggle)](https://www.kaggle.com/datasets/bhanupratapbiswas/superstore-sales)  
**Tools:** Python, Pandas, Matplotlib, Seaborn  
**Language:** Russian  

## What's inside

Exploratory data analysis of a US retail store with 9,800 transactions (2015–2018).

**Steps covered:**
- Dataset overview and descriptive statistics
- Missing values and duplicate check
- Outlier analysis (IQR method)
- Data cleaning and datetime conversion
- Feature engineering: Delivery_Days, Order_Month, Order_Year
- Categorical encoding: One-Hot Encoding, binary feature
- Correlation matrix
- Min-Max normalization and Z-score standardization

## Key Findings

| Finding | Detail |
|---------|--------|
| Peak revenue months | September, November, December |
| Revenue trend | Growing YoY: ~$484K (2015) → ~$722K (2018) |
| Avg delivery time | ~4 days; 0-day = Same Day confirmed |
| Outliers in Sales | 11.7% — legitimate large orders, not errors |
| Strongest correlator | `Is_Technology` (r = 0.17) |

## Files
- [`EDA_Superstore_Sales.ipynb`](./EDA_Superstore_Sales.ipynb) — full notebook (Russian)
