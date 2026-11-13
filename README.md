# XAUUSD Multi-Factor Confluence Strategy (Pine Script v5)

![Pine Script](https://img.shields.io/badge/Pine%20Script-v5-blue.svg)
![TradingView](https://img.shields.io/badge/Platform-TradingView-orange.svg)
![Market](https://img.shields.io/badge/Asset-XAUUSD%20(Gold)-gold.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)

A quantitative multi-factor confluence strategy developed in **Pine Script v5** for TradingView, optimized for spot gold (`XAUUSD`). The script systematically filters price action by combining macrotrend structures, volatility metrics, relative volume, and momentum indicators to isolate high-probability long entries directly on the charts.

---

## Strategy Logic & Multi-Layer Filters

The indicator evaluates four strict quantitative conditions simultaneously to eliminate market noise:
1. **Macro Trend Filter (EMA 200):** Computes a 200-period Exponential Moving Average (`ta.ema`) to ensure entries are aligned strictly with the long-term bullish trend direction.
2. **Volatility Bands (Bollinger Bands):** Utilizes Bollinger Bands to monitor price positioning relative to market volatility and mean reversion levels.
3. **Relative Volume (RVOL):** Compares current trading volume against its moving average baseline, requiring heightened institutional participation.
4. **Stochastic Trigger (%K & %D):** Implements a smoothed Stochastic oscillator to detect relative oversold conditions combined with bullish crossover momentum (`ta.crossover`).

---

## Implementation & Usage

1. Open **TradingView** and open the **Pine Editor**.
2. Create a new strategy script and paste the contents of `strategy.pine` from this repository.
3. Add the strategy to your `XAUUSD` chart (recommended on daily or 4H timeframes for institutional confluence).
4. Configure backtest parameters, risk management (Stop Loss / Take Profit), and position sizing directly from the TradingView settings panel.
