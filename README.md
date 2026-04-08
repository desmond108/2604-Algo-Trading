# QUANTITATIVE TRADING STRATEGY ANALYSIS
## Strategies Summary: Analysis, Comparison & Transaction Cost Impact
**S&P 500 | 2000–2025 | 11 Strategies Evaluated**

**Backtesting & Strategy Research** **April 2026**

---

### Disclaimer
The algorithmic trading strategies, scripts, backtests, and associated content provided here are for **educational and informational purposes only**. They do not constitute financial advice, investment advice, trading advice, or a solicitation to buy or sell any security, cryptocurrency, or derivative instrument. Trading in financial markets carries a high degree of risk and is not suitable for all investors. AI was used extensively in the whole process and hallucinations can be attributed to both the AI and myself.

Please refer to the Strategies_Analysis_Report.pdf for a more detailed Summary of the backtests.
---

### 1. Executive Summary
This report analyses eleven systematic trading strategies backtested on the S&P 500 from 2000 to 2025. The strategies span two structural families—**trend-following** and **mean-reversion**—and are evaluated across return, risk-adjusted performance, trade characteristics, and transaction costs.

The analysis reveals three top-tier strategies:
* **RSI4 25/55:** Strongest risk-adjusted strategy with a 2.79 Sharpe ratio and 9.31% maximum drawdown.
* **Williams %R:** Safest for capital preservation with the lowest maximum drawdown (8.42%).
* **Connors 3-Day Hi-Lo:** Disciplined pullback strategy with a 77% win rate and 2.05 Sharpe ratio.

---

### 2. Strategy Classification
The strategies are categorized by their structural families and typical trade frequencies.

| Strategy | Family | Avg Hold | Trade Freq. | Signal Logic |
| :--- | :--- | :--- | :--- | :--- |
| **SMA200** | Trend-Following | 69.3 days | Very Low (97) | MA crossover |
| **RSI2** | Mean-Reversion | 4.4 days | High (507) | RSI + MA filter |
| **PSAR** | Trend-Following | 16.8 days | Medium (337) | SAR reversal |
| **Inverse PSAR** | Mean-Reversion | 11.4 days | Medium (336) | Contrarian SAR |
| **RSI3** | Mean-Reversion | 12.0 days | Medium (332) | RSI bounce |
| **RSI4 25/55** | Mean-Reversion | 7.5 days | Low-Med (139) | RSI + MA filter |
| **Connors 3-Day** | Mean-Reversion | 4.4 days | Low (122) | Price pattern |
| **Keltner Bands** | Mean-Reversion | 6.5 days | Medium (337) | Band breakout |
| **CCI Momentum** | Mean-Reversion | 5.3 days | High (583) | Oscillator |
| **Williams %R** | Mean-Reversion | 3.1 days | Low-Med (171) | Oscillator |
| **Stochastic K** | Mean-Reversion | 4.6 days | High (538) | Oscillator |

---

### 3. Return Analysis (2000–2025)
*Assumes $100,000 starting capital and zero transaction costs.*

| Strategy | Net Profit | Profit/Mo. | Avg Trade | # Trades | Avg Time |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **SMA200** | 207.77% | 0.67% | 1.45% | 97 | 69.3d |
| **RSI2** | 236.65% | 0.76% | 0.25% | 507 | 4.4d |
| **PSAR** | 5.42% | 0.02% | 0.07% | 337 | 16.8d |
| **Inverse PSAR** | 433.87% | 1.40% | 0.60% | 336 | 11.4d |
| **RSI3** | 296.38% | 0.96% | 0.44% | 332 | 12.0d |
| **RSI4 25/55** | 192.44% | 0.71% | 0.79% | 139 | 7.5d |
| **Connors 3-Day** | 133.40% | 0.50% | 0.74% | 122 | 4.4d |
| **Keltner Bands** | 297.22% | 0.96% | 0.41% | 337 | 6.5d |
| **CCI Momentum** | 788.44% | 2.54% | 0.40% | 583 | 5.3d |
| **Williams %R** | 170.18% | 0.55% | 0.60% | 171 | 3.1d |
| **Stoch K** | 794.18% | 2.56% | 0.43% | 538 | 4.6d |

---

### 4. Risk & Risk-Adjusted Performance
Evaluation of drawdowns and efficiency (Sharpe/Ulcer Index).

| Strategy | Max DD | Sharpe | Ulcer Idx | Kelly % |
| :--- | :--- | :--- | :--- | :--- |
| **SMA200** | 29.25% | 0.40 | 0.1223 | 11.34% |
| **RSI2** | 13.06% | 1.62 | 0.0435 | 32.53% |
| **PSAR** | 51.35% | 0.02 | 0.3018 | 2.47% |
| **RSI4 25/55** | 9.31% | 2.79 | 0.0307 | 56.15% |
| **Connors 3-Day** | 13.29% | 2.05 | 0.0359 | 42.30% |
| **Williams %R** | 8.42% | 0.77 | 0.0141 | 54.49% |

---

### 5. Transaction Cost Impact
Detailed assessment of how friction (slippage and commissions) degrades strategy performance.

| Strategy | Trades | Cost as % of Profit | Adj. Profit (Retail) | Adj. Profit (Futures) |
| :--- | :--- | :--- | :--- | :--- |
| **SMA200** | 97 | 7.5% | 192.25% | 205.34% |
| **RSI2** | 507 | 34.3% | 155.53% | 223.97% |
| **PSAR** | 337 | 994.8% | -48.50% | -3.01% |
| **Stoch K** | 538 | 10.8% | 708.10% | 780.73% |

---

### 6. Highlights
1.  **Prioritize RSI4 25/55:** Best risk-adjusted profile and lowest sensitivity to costs.
2.  **Optimize Execution:** High-frequency strategies (Stoch K, CCI) transaction costs could be reduced via **E-mini (ES)** or **Micro E-mini (MES)** futures.
3.  **Position Sizing:** Utilize a conservative **half-Kelly** approach to manage tail risk while maintaining growth.
