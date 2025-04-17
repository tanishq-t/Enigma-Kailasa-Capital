# 🚀 Kailasa Capital | Cross‑Timeframe Trading Architecture for Consistent Alpha

A quantitative finance project designed to build, test, and evaluate robust trading strategies across multiple timeframes and instruments. This initiative focuses on sustainable alpha generation with well-calibrated risk management and capital allocation.

---

## 📌 Project Objectives

- ✅ Improve profit consistency through diversified strategies
- 📉 Minimize drawdowns (absolute & time under drawdown)
- 📈 Maximize risk-adjusted returns (Calmar & Sharpe Ratios)
- 💰 Implement realistic capital allocation and dynamic position sizing

---

## 📊 Data Overview

- **Instruments:** Nifty 50 & Bank Nifty
- **Timeframes:** 1D (Positional), 60-min (Swing), 15-min (Intraday)
- **Source:** [Kaggle - Nifty Minute Data](https://www.kaggle.com/datasets/debashis74017/nifty-50-minute-data)
- **Period:** January 1, 2020 to March 31, 2025

---

## 🧹 Data Cleaning & Resampling

Two primary preprocessing utilities were built:
- `clean_daily(df)`: Handles daily-level data
- `clean_and_resample(df, timeframe)`: Cleans and resamples minute data into desired OHLCV formats

---

## 🧠 Strategy Architecture

Three distinct trading strategies were developed and tested:

1. **ATR Channel Breakout**  
   - Combines trend-following with volatility bands
   - Entry/Exit based on price breaking above/below ATR bands

2. **MACD Histogram Reversal**  
   - Captures momentum reversals
   - Buy/Sell when MACD histogram flips polarity

3. **SuperTrend + SMA Filter**  
   - Filters SuperTrend signals using a moving average to reduce noise

---

## 📈 Backtesting & Evaluation

Each strategy was applied to both instruments across all timeframes. Key performance metrics:

- ✅ Cumulative Returns & Equity Curves
- 📊 Sharpe Ratio, Calmar Ratio, Win Rate
- 📉 Max Drawdown & Duration
- 🔁 Monthly Performance Consistency

---

## 💸 Capital Allocation

- **Total Capital:** ₹1 Crore
- **Minimum Allocation:** ₹10L per strategy
- **Lot Sizes:** Nifty = 75, Bank Nifty = 3
- **Leverage Considered:** 20% margin requirement
- **Compounding:** Enabled when sufficient margin exists

---

## 📂 Project Structure

