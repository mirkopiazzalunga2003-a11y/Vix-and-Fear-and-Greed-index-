# Market Risk Indicators: VIX and Fear & Greed Index

This repository provides an overview of two key risk indicators for the U.S. equity market: the **CBOE Volatility Index (VIX)** and the **CNN Fear & Greed Index**. The content is based on an analytical report describing their calculation, interpretation, and practical application.

---

##  Fear & Greed Index (CNN)

The **CNN Fear & Greed Index** measures market sentiment on a scale from 0 (extreme fear) to 100 (extreme greed). It is composed of 7 equally weighted indicators:

- Market Momentum (S&P 500 vs. 125-day MA)
- Market Volatility (VIX vs. 50-day MA)
- Stock Price Strength (breadth of advancing vs. declining stocks)
- Safe Haven Demand (equity vs. Treasury yield spread)
- Stock Price Breadth (volume-based McClellan Summation Index)
- Junk Bond Demand (high-yield vs. Treasury spread)
- Put/Call Options Ratio

### TradingView Implementation
A custom reconstructed version of the index is available on TradingView:  
[**Fear & Greed Index (Reconstructed) - TradingView Script**](https://www.tradingview.com/script/TyBQNCDn-Fear-Greed-Index-Reconstructed/)

This implementation allows:
- Historical analysis beyond CNN’s default view
- Customization of individual components
- Comparison with other assets (e.g., S&P 500)

#### Advantages Over CNN’s Official Version
- **Longer time horizon** analysis
- **Component-level breakdown** for deeper insight
- **Flexible visualization** and integration with other TradingView tools
- **Real-time customization** of indicator parameters

---

##  CBOE Volatility Index (VIX)

The **VIX**, often called the "fear gauge," is a real-time market index that represents the market's expectation of 30-day forward-looking volatility of the S&P 500. It is derived from the implied volatilities of a wide range of S&P 500 index options (both puts and calls), focusing on out-of-the-money (OTM) contracts.

### Calculation Methodology (Conceptual Overview)
Rather than using historical price movements, the VIX calculates **implied volatility** from the prices of S&P 500 index options. The core idea is that option premiums reflect the market's collective expectation of future price variability. The methodology involves:
1.  Selecting a range of OTM S&P 500 options with near-term and next-term expirations to bracket a constant 30-day horizon.
2.  Using a model-free approach to compute a variance swap rate from the weighted prices of these options.
3.  Interpolating between the two expirations to derive a single, precise 30-day expected volatility measure.
4.  Expressing the result as an annualized percentage.

---

##  VIX vs. S&P 500 Correlation

The VIX exhibits a **strong negative correlation** with the S&P 500, historically around **-0.71** over 20 years. During market downturns, uncertainty rises, leading to:
- Increased demand for protective options
- Higher option premiums
- Elevated implied volatility (VIX rises)

This relationship is especially pronounced in equities, where volatility tends to spike during declines, unlike in commodities where volatility can rise in both bullish and bearish markets.

---

##  Intermarket Analysis Context

Intermarket analysis studies relationships between asset classes (equities, bonds, commodities, currencies) to identify macroeconomic shifts and capital flows. During uncertainty:
- **Safe havens** like gold, USD, and government bonds often appreciate
- **Cyclical commodities** (oil, copper) may decline
- **Defensive equity sectors** (utilities, healthcare) tend to outperform

Understanding these dynamics helps contextualize movements in the VIX and Fear & Greed Index.

---

## Author

**Mirko Piazzalunga**
Obsidian Financial Research

