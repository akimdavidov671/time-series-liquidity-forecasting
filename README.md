# time-series-liquidity-forecasting

## What is Market Liquidity?

Market liquidity describes how easily an asset can be bought or sold without significantly affecting its price.

In highly liquid markets, trades can be executed quickly, in large size, and with minimal price impact. In illiquid markets, even relatively small trades can move prices, spreads widen, and transaction costs increase. Liquidity therefore reflects the underlying health and stability of financial markets.

In modern financial systems, liquidity plays a central role. Institutional investors, asset managers, market makers, and algorithmic traders all rely on the ability to transact efficiently. When liquidity deteriorates — especially during periods of market stress — trading becomes more expensive, price volatility increases, and risk management becomes more difficult.

Unlike price returns, liquidity is not directly observable as a single number. It must be measured indirectly using trading data. In this project, liquidity is quantified using the Amihud illiquidity measure, which captures how strongly prices move relative to trading volume. Higher values indicate that prices react more aggressively to trades, meaning the market is less liquid.

Why Forecast Liquidity?

Forecasting liquidity is economically important for several reasons:

- Portfolio managers need liquidity estimates to manage transaction costs and execution risk.

- Risk managers monitor liquidity conditions because sudden dry-ups often coincide with market stress.

- Market makers adjust spreads and inventory based on expected trading conditions.

If liquidity exhibits predictable structure this information can improve trading decisions, capital allocation, and risk assessment.

---

## Objectives:

- Quantify the predictability of next-day ETF liquidity

- Compare naive persistence, autoregressive models, and nonlinear machine learning methods to identify the most effective forecasting approach.

- Evaluate how volatility, rolling state variables, and regime indicators contribute to incremental predictive power.

- Test the stability of liquidity dynamics across major macro regimes (Pre-GFC, GFC, QE, COVID/Tightening).

- Validate whether liquidity persistence is asset-specific (XLK) or a general market phenomenon by analyzing multiple ETFs (SPY, IWM, XLF).

---

### Dataset:

The primary dataset consists of daily historical market data for XLK (Technology Select Sector ETF), which serves as the main asset for model development and evaluation.

Data is downloaded using yfinance and includes daily:

- Open, High, Low, Close prices and Trading Volume

The XLK sample spans approximately 2000–2024, covering multiple macroeconomic environments including the Global Financial Crisis, post-crisis QE period, and the COVID/tightening cycle.

For robustness and cross-asset validation, the analysis is later replicated on:

- SPY – S&P 500 ETF

- IWM – Russell 2000 ETF

- XLF – Financial Sector ETF

---

