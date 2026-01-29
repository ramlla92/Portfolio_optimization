# Portfolio Optimization and Backtesting Project

This project applies a data-driven, quantitative approach to portfolio construction and evaluation using Python. It combines historical market data, forecast-informed assumptions, and Modern Portfolio Theory (MPT) to construct optimal portfolios and validate their performance through backtesting against a traditional benchmark.

The primary objective is to assess whether a model-driven portfolio strategy can outperform a simple passive allocation on a risk-adjusted basis.

---

## Project Overview

The project follows a structured analytical workflow:

1. **Data Preparation**
   - Historical daily price data for SPY (equities) and BND (bonds) is loaded from CSV files.
   - Data is cleaned, aligned by date, and transformed into daily returns.
   - A forward-looking TSLA price series (forecast) is incorporated to represent an expected return hypothesis.

2. **Portfolio Optimization (Modern Portfolio Theory)**
   - Annualized expected returns and covariance matrices are computed.
   - Two optimized portfolios are constructed using PyPortfolioOpt:
     - Maximum Sharpe Ratio Portfolio
     - Minimum Volatility Portfolio
   - The efficient frontier and covariance matrix are visualized to understand the risk–return tradeoff and asset relationships.

3. **Strategy Backtesting**
   - The optimized portfolio from Task 4 is treated as a hypothesis.
   - A backtest is conducted on the final year of available data, which was not used in model estimation.
   - Performance is compared against a static benchmark portfolio:
     - **60% SPY / 40% BND**
   - Metrics evaluated:
     - Total return
     - Annualized return
     - Sharpe ratio
     - Maximum drawdown

4. **Evaluation**
   - Strategy performance is analyzed relative to the benchmark.
   - Results are interpreted with clear acknowledgment of modeling and data limitations.

---

## Project Structure

```bash
portfolio-optimization/
├── data/
│   └── raw/
│       ├── SPY_historical.csv
│       ├── BND_historical.csv
│       └── TSLA_historical.csv
├── notebooks/
│   ├── task_3_forecasting.ipynb
│   ├── task_4_portfolio_optimization.ipynb
│   └── task_5_backtesting.ipynb
├── src/
│   └── portfolio_optimization.py
├── requirements.txt
└── README.md
