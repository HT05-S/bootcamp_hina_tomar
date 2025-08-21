HOMEWORK 1

1. Problem Statement

This file summarizes the development of a simple rule‑based trading strategy using SPY minute‑level data to investigate whether momentum signals, defined via VWMA crossovers combined with volatility (ATR) and volume filters, can deliver profitable and risk‑balanced returns.

2. Stakeholder & Use Case

Stakeholder / User: Trading strategy researcher

Primary Need: To determine whether the methodological approach produces credible performance and whether it merits further expansion.

3. Analytical Scope & Methodology

Data: SPY minute‑level OHLCV data from Jan–Sep 2023.

Indicators: a. VWMA_short (20‑period)
            b. VWMA_long (1000‑period)
            c. ATR (10‑period)
            c. Average Volume (10‑period)

Signals: Buy when VWMA_short crosses above VWMA_long, close > open, and volume above average. Sell when the reverse holds.

Backtest Engine: Simulate trades with fixed set size (100), leverage = 5, $25 cost per trade, with stop‑loss at 1.5×ATR.

Outcomes Tracked: Trade log, daily profit/loss, cumulative returns, Sharpe ratio, maximum drawdown, net profit, price with signal visualization.

4. Deliverable Artifacts

Quantitative: Sharpe ratio, maximum drawdown, total net profit.

Visual: Price graph with VWMA indicators and buy/sell markers; cumulative PnL over time.

Logs: Detailed trade log and daily P&L summary.

Interpretation: Insights into whether signals are too noisy, prone to large drawdowns, or supported by volume/volatility dynamics.

5. Why This Matters

This serves as a reproducible case study in rule‑based trading strategy evaluation. It helps build maturity in developing, testing, and interpreting systematic trading models, which is foundational for rigorous quantitative finance research. Overall, the insights will guide whether to refine parameter selection, risk controls, or explore machine learning enhancements.