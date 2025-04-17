# 🚀 Kailasa Capital | Cross‑Timeframe Trading Architecture for Consistent Alpha

A quantitative finance project aimed at engineering robust, multi-timeframe trading systems for Nifty and Bank Nifty. It blends technical analysis, backtesting, and capital management to deliver sustainable alpha with minimized drawdowns.

---

## 📌 Project Objectives

- ✅ Improve profit consistency across timeframes and instruments
- 📉 Minimize absolute and temporal drawdowns
- 📈 Maximize risk-adjusted returns (Sharpe & Calmar Ratios)
- 💰 Apply dynamic capital allocation and position sizing techniques

---

## 📊 Data Overview

- **Instruments:** Nifty 50 & Bank Nifty
- **Timeframes Used:**
  - Daily (1D): Positional
  - 60-Minute: Swing
  - 15-Minute: Intraday
- **Source:** [Kaggle - Nifty Minute Data](https://www.kaggle.com/datasets/debashis74017/nifty-50-minute-data)
- **Date Range:** Jan 1, 2020 – Mar 31, 2025

---

## 🧹 Data Cleaning & Resampling

Two modular preprocessing functions were created:

- `clean_daily(df)`: Cleans, filters, and indexes daily OHLCV data.
- `clean_and_resample(df, timeframe)`: Cleans minute-level data and resamples it to the desired timeframe (15T, 60T, or 1D) using OHLCV logic.

Key operations:

- Remove nulls and duplicate timestamps
- Ensure chronological integrity
- Aggregate volume and price columns correctly

---

## 🧠 Strategy Architecture

Three core strategies were designed and applied to both instruments across all timeframes:

1. **ATR Channel Breakout**

   - Trend-following with dynamic ATR-based bands
   - Entry: Close > Upper Band | Exit: Close < Lower Band

2. **MACD Histogram Reversal**

   - Reversal-based strategy using MACD histogram polarity flips
   - Entry: Histogram turns positive | Exit: Histogram turns negative

3. **SuperTrend + SMA Filter**

   - Filters SuperTrend signals through SMA alignment
   - Trades only when SuperTrend agrees with moving average trend

---

## 📈 Backtesting & Evaluation

Each strategy underwent rigorous testing across instruments and timeframes. Metrics tracked:

- ✅ Cumulative & Strategy-wise Equity Curves
- 📊 Sharpe Ratio, Calmar Ratio
- 📉 Max Drawdown & Drawdown Duration
- 🔁 Month-wise Return Consistency
- ⚡ Trade Frequency & Win Rate

---

## 💸 Capital Allocation

- **Total Virtual Capital:** ₹1 Crore
- **Minimum Allocation per Strategy:** ₹10L
- **Minimum Tradable Lots:** Nifty = 75, Bank Nifty = 3
- **Margin Requirement:** 20% of notional value
- **Compounding Allowed:** Yes (based on profits)

Example:

> Nifty @ ₹21,000 ⇒ Notional = ₹15.75L ⇒ Margin = ₹3.15L

---

## 🧠 Key Insights

- ✅ Multi-timeframe diversification helped reduce overall risk
- 🔁 SuperTrend with SMA Filter was most consistent across timeframes
- 📈 Bank Nifty strategies showed stronger breakout behavior vs Nifty
- 🚫 Excessive curve fitting was avoided by maintaining core logic

---


