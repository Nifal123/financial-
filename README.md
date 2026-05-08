
# Multi-Asset Portfolio Optimizer

Institutional-grade portfolio construction across 7 asset classes
using Modern Portfolio Theory, Risk Parity, and Monte Carlo simulation.

## Asset Universe

| Ticker | Asset Class         |
|--------|---------------------|
| SPY    | US Equities         |
| EFA    | International Equities |
| TLT    | Long-Term Bonds     |
| BND    | Aggregate Bonds     |
| GLD    | Gold                |
| GSG    | Commodities         |
| VNQ    | Real Estate (REITs) |

## Strategies Implemented

- Mean-Variance Optimization (Markowitz 1952)
- Maximum Sharpe Ratio Portfolio
- Minimum Variance Portfolio
- Risk Parity (Equal Risk Contribution)
- Walk-Forward Backtesting with Monthly Rebalancing

## Notebooks

| Notebook | Description |
|----------|-------------|
| 01_Data_Pipeline | Fetch and clean 7-asset price data (2018-2024) |
| 02_Portfolio_Analytics | Risk metrics, VaR, Sharpe, drawdown analysis |
| 03_Optimization_Engine | Efficient frontier and optimal portfolio construction |
| 04_Backtesting_Engine | Walk-forward backtest vs 60/40 benchmark |
| 05_Final_Report | Master dashboard and performance tearsheet |

## Key Visualizations

- Efficient Frontier with 10,000 Monte Carlo portfolios
- Cumulative growth of $100,000 across all strategies
- Correlation heatmap across asset classes
- Rolling 12-month Sharpe ratio by strategy
- Value at Risk on $1,000,000 portfolio
- Annual returns heatmap (2018-2024)

## Tools

Python | Pandas | NumPy | SciPy | Plotly | yFinance

## Author

Financial Analyst | Quantitative Portfolio Research
