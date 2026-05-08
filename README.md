# Generate your README.md automatically
# Copy this output directly into your GitHub README

best_strategy = tearsheet['Sharpe Ratio'].idxmax()
best_row      = tearsheet.loc[best_strategy]
bench_row     = tearsheet.loc['60/40 Benchmark']
sharpe_improv = round(
    (best_row['Sharpe Ratio'] - bench_row['Sharpe Ratio'])
    / abs(bench_row['Sharpe Ratio']) * 100, 1)

readme = f"""
# Multi-Asset Portfolio Optimizer

> Institutional-grade portfolio construction across 7 asset classes
> using Modern Portfolio Theory, Risk Parity, and Monte Carlo simulation.

## Project Overview

This project implements a complete quantitative portfolio management
framework — from data pipeline to backtesting — replicating the
methodology used by institutional asset managers.

## Asset Universe

| Ticker | Asset Class        |
|--------|--------------------|
| SPY    | US Equities        |
| EFA    | Intl Equities      |
| TLT    | Long-Term Bonds    |
| BND    | Aggregate Bonds    |
| GLD    | Gold               |
| GSG    | Commodities        |
| VNQ    | Real Estate (REITs)|

## Strategies Implemented

- Mean-Variance Optimization (Markowitz 1952)
- Maximum Sharpe Ratio Portfolio
- Minimum Variance Portfolio
- Risk Parity (Equal Risk Contribution)
- Walk-Forward Backtesting with Monthly Rebalancing

## Backtest Results (2019-2024)

| Strategy        | Ann. Return | Volatility | Sharpe | Max Drawdown |
|-----------------|-------------|------------|--------|--------------|
| Max Sharpe      | {tearsheet.loc['Max Sharpe','Ann. Return %']}%       | {tearsheet.loc['Max Sharpe','Volatility %']}%      | {tearsheet.loc['Max Sharpe','Sharpe Ratio']}  | {tearsheet.loc['Max Sharpe','Max Drawdown %']}%       |
| Min Variance    | {tearsheet.loc['Min Variance','Ann. Return %']}%       | {tearsheet.loc['Min Variance','Volatility %']}%      | {tearsheet.loc['Min Variance','Sharpe Ratio']}  | {tearsheet.loc['Min Variance','Max Drawdown %']}%       |
| Risk Parity     | {tearsheet.loc['Risk Parity','Ann. Return %']}%       | {tearsheet.loc['Risk Parity','Volatility %']}%      | {tearsheet.loc['Risk Parity','Sharpe Ratio']}  | {tearsheet.loc['Risk Parity','Max Drawdown %']}%       |
| Equal Weight    | {tearsheet.loc['Equal Weight','Ann. Return %']}%       | {tearsheet.loc['Equal Weight','Volatility %']}%      | {tearsheet.loc['Equal Weight','Sharpe Ratio']}  | {tearsheet.loc['Equal Weight','Max Drawdown %']}%       |
| 60/40 Benchmark | {tearsheet.loc['60/40 Benchmark','Ann. Return %']}%       | {tearsheet.loc['60/40 Benchmark','Volatility %']}%      | {tearsheet.loc['60/40 Benchmark','Sharpe Ratio']}  | {tearsheet.loc['60/40 Benchmark','Max Drawdown %']}%       |

Best strategy ({best_strategy}) achieved a {sharpe_improv}% Sharpe improvement vs 60/40 benchmark.

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

## Tools and Libraries

Python | Pandas | NumPy | SciPy | Plotly | yFinance

## Author

Your Name | Financial Analyst
LinkedIn: linkedin.com/in/yourprofile
"""

print(readme)
print("")
print("Copy everything above into your GitHub README.md file")
