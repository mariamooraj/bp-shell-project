# Statistical Arbitrage: BP vs Shell Pairs Trading Strategy 
This project implements a **statistical arbitrage** pairs trading strategy using BP and Shell stock prices. 
It applies **cointegration testing** to identify long-term price relationships, then backtests a mean reversion trading strategy to evaluate profitability. 

## Project Overview
- Goal: Identify and exploit price divergences between two historically correlated energy stocks.
- Time Period: Jan 2015 - Jan 2020
- Data Source: Yahoo Finance via 'yfinance' API
- Methodology: Cointegration testing, Z-score trading signals, backtesting

## Technologies and Libraries 
- Python 3
- pandas, NumPy
- matplotlib, seaborn
- statsmodels
- yfinance

## Methodology
1. Data Collection: Downloaded adjusted close prices for BP and Shell from Yahoo Finance. 
2. Visualization: Plotted historical price trends.
3. Cointegration Test: Used Engle Granger method to test long-term equilibrium.
4. Signal Generation: Calculated Z-scores of the spread to define long/short entry points.
5. Backtesting: Simulated trading strategy performance over historical data.

## Key Results
- P-value < 0.05: Strong evidence of cointegration.
- Generated trade signals capturing mean reversion opportunities.
- Strategy performance evaluated via total returns (measures absolute profitability of strategy over backtest period) and Sharpe ratio (assesses risk-adjusted returns by comparing excess return (over a risk-free rate) to the standard deviation of returns - higher ratio indicates better risk-reward efficiency)

## How to Run
1. Install dependencies:
   '''bash
   pip install yfinance pandas matplotlib numpy statsmodels seaborn
2. Run notebook:
   jupyter notebook "BP vs Shell.ipynb"
