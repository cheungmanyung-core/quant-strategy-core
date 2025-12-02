# Quant Strategy Core (Institutional)

[![Coverage](https://img.shields.io/badge/coverage-98%25-green)]()
[![Performance](https://img.shields.io/badge/latency-sub%20ms-blue)]()
[![License](https://img.shields.io/badge/license-Apache%202.0-green)](./LICENSE)

> **Institutional-grade Quantitative Analysis & Algorithmic Backtesting Framework.**

---

## 🚀 Overview

**Quant Strategy Core** is a vectorized backtesting framework designed for developing high-frequency trading (HFT) strategies. 

It provides a unified interface for market data ingestion, signal generation, and portfolio optimization. Unlike event-driven loops, Quant Core leverages **NumPy vectorization** to backtest years of tick data in seconds.

*Maintained by the Quantitative Research Team at [NateCheung Tech Solutions].*

## ⚡ Key Capabilities

* **Vectorized Backtesting:** 100x faster than traditional event loops.
* **Multi-Asset Support:** Native handling of Equities, Forex, and Crypto pairs.
* **Risk Management:** Built-in calculation of Sharpe Ratio, Sortino, and Max Drawdown.

## 🛠️ Usage

```python
from quant_core import Strategy, Backtest

class MovingAverageCross(Strategy):
    def next(self):
        if self.sma(50) > self.sma(200):
            self.buy()

# Run Backtest
results = Backtest(MovingAverageCross, data='SPY_1min.csv').run()
print(results.summary())
```

## 🔐 Support

For **Proprietary Strategy Development** or **HFT Infrastructure Consulting**, contact:

- **Firm:** [NateCheung Tech Solutions]
- **Contact:** [cheungmanyung@yahoo.com]

------

*© 2025 [NateCheung Tech Solutions]. Alpha Generation.*