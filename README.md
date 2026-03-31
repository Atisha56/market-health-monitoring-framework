# Market-health-monitoring-framework

## Overview
A quantitative framework that treats financial markets as a living system, 
building a composite "health score" to detect true financial stability vs. 
apparent wellness.

## Objective
Detect early-stage market stress before it becomes visible in price performance.

## Methodology
- Built a 3-layer Market Health Score mapping biological vitals to market indicators
- Layer 1 (Vital Signs): Volatility, market breadth, cross-asset correlations, liquidity proxies
- Layer 2 (Lab Tests): Credit spreads, skew/tail-risk pricing, volatility term structure
- Layer 3 (Stress Tests): Market reaction to macro shocks, recovery speed metrics
- Applied Hidden Markov Models to classify market regimes: Healthy / Stable-but-Fragile / Unstable /       Recovering
- Backtested Hidden Stress Index against drawdowns across 2008, 2020, and 2022 crisis episodes

## Key Findings
- Markets can show positive returns while the Market Health Score deteriorates
- Rising correlations + weakening breadth + worsening liquidity is a reliable signature of systemic fragility
- HMM regime classification achieved strong accuracy on backtested S&P 500 and VIX data

## Tools & Data
- Python (Pandas, NumPy, Statsmodels, Matplotlib)
- Data: S&P 500 constituents, VIX, credit spreads, FRED macroeconomic indicators
- Methods: GARCH, Hidden Markov Models, Time-Series Classification
