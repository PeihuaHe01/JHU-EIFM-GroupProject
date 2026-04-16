# JHU-EIFM-GroupProject
Python code for portfolio strategy and analysis
# EIFM Group Project – Investment Strategy

## Strategy

This project implements a two-stage portfolio construction approach:

### 1. Stock Selection (Short-Term Signal)
- Uses the most recent **3 months of data**
- Stocks are ranked based on a composite score:
  
  Score = 0.7 × Sharpe Ratio + 0.3 × Alpha − 0.2 × Beta

- The top-ranked stocks are selected subject to:
  - Sector constraints
  - Maximum number of stocks per sector

### 2. Portfolio Optimization (Long-Term Stability)
- Uses **10 years of historical data**
- Selected stocks are assigned optimal weights by:
  - Minimizing portfolio variance (or maximizing Sharpe ratio)
  - Subject to:
    - Minimum weight constraints
    - Sector allocation constraints

---

## Key Insight
This approach combines:
- **Short-term momentum / performance signals (3 months)** for stock selection  
- **Long-term risk estimation (10 years)** for robust portfolio optimization  

This helps balance responsiveness to recent market conditions with stability in risk estimation.

## Reproducibility Note

All code in this project was executed using data available as of **March 5, 2026**.

Due to the nature of the data source (Yahoo Finance), historical price data may be subject to revisions, including adjustments for dividends, stock splits, and data corrections. As a result, the exact numerical results (e.g., scores, rankings, and portfolio weights) may not be perfectly reproducible when the code is run at a later date.

However, the overall methodology, stock selection logic, and portfolio structure remain consistent, and the results are robust to such minor data variations.


## Author
Peihua He, Yitong Zhang, Anzi Yao, Tracy Wang

Johns Hopkins University
