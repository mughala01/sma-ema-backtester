# sma-ema-backtester
Quantitative trading backtester in Python implementing SMA &amp; EMA crossover strategy, portfolio simulation, and performance metrics
# SMA–EMA Crossover Backtester

**Author:** [YOUR NAME] • **Repo:** SMA-EMA-Backtester

## What this is (in one sentence)
A small Python script that backtests a simple moving-average crossover (SMA vs EMA) and plots the equity curve.

## Why I built it
I wanted a clean, short example of a trading idea I can explain in interviews: how to form a signal, avoid look-ahead, add basic costs, and calculate performance.

## How it works (plain English)
- Download daily prices for a ticker (default: `[TICKER, e.g., AAPL]`, dates `[YYYY-MM-DD]` to `[YYYY-MM-DD]`).
- Compute **SMA `[SHORT]`** and **EMA `[LONG]`**.  
- **Signal:** long when SMA crosses **above** EMA; flat/exit when it crosses **below**.  
- Positions are **shifted by one day** so I don’t trade on information I couldn’t have known.  
- Track portfolio value from an initial cash balance.

## Quick start
```bash
pip install pandas matplotlib yfinance
python backtester.py  # (or run in your IDE)
