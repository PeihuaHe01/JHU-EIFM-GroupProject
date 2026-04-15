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

## Author
Peihua He, Yitong Zhang, Anzi Yao, Tracy Wang
Johns Hopkins University
