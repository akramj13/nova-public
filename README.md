# Nova

<div align="center">
    <img src="./original-logo.png" alt="Nova" width="256" height="256">
</div>

**A tick-by-tick backtesting engine and real-time trading dashboard for automated futures strategies.**

## About

Nova is a quantitative trading system built for researching and monitoring automated futures strategies. It combines:

- A Python backtesting engine that processes market data one tick at a time
- Realistic bid/ask execution and position risk controls
- Monte Carlo analysis for drawdown and risk-of-ruin estimates
- A desktop dashboard for positions, P&L, performance, and system health

The project is designed around live-trading realism: strategies receive sequential market data, entries use the appropriate side of the spread, and exits can be controlled by take-profit, stop-loss, and time-stop rules.

## Public Repository

This is the public information page for Nova. The full source code and associated research materials are not distributed in this repository.

If you are interested in obtaining access to the code, please contact the repository owner. Access is provided at the owner's discretion.

## System Overview

The backtesting workflow is organized around four components:

```text
Market data -> DataHandler -> Strategy -> TradeManager
                              ^              |
                              |              v
                         BacktestEngine <- Results
```

The dashboard complements the engine with live position monitoring, unified P&L and equity views, strategy settings, performance metrics, and operator controls.

## Highlights

- Tick-by-tick execution without look-ahead bias
- Bid/ask-aware long and short fills
- Take-profit, stop-loss, and time-based risk controls
- Automatic front-month futures filtering by liquidity
- Strategy abstraction for interchangeable research implementations
- Performance reporting including win rate, profit factor, drawdown, and Sharpe ratio
- Monte Carlo simulations for evaluating outcome ranges and risk

## Technology

- **Backtesting:** Python
- **Desktop application:** Electron
- **User interface:** Next.js and React
- **Styling:** Tailwind CSS and shadcn/ui
- **Charts:** Recharts

## Market Data

Nova was built to work with Databento MBP-1 futures data in `.dbn.zst` format. The data layer uses timestamps, prices, bid/ask quotes, symbols, and trade sizes to reproduce market conditions during a backtest.

## Further Information

The full project includes architecture notes and strategy documentation covering the shared engine, BTC and SOL strategy tracks, runtime configuration, and analysis workflows. These materials are available with the source code.

Nova is a research and monitoring system, not financial advice. Trading futures involves substantial risk.
