# Hidden Fragility in Financial Markets
## A Network-Based Early Warning System for Equity Market Crashes
"Can we detect that the market is getting sick by monitoring the connections between its parts — before prices fall?"

## Overview
This project develops a daily early warning system for US equity market crashes by treating the stock market as a living system — where each sector is an organ and cross-sector correlations act as the nerves connecting them. Just as a doctor monitors a patient's vital signs before collapse, we monitor the network structure of S&P 500 sector correlations to detect hidden fragility before it becomes visible in prices. The framework constructs a Composite Fragility Score from four daily network biomarkers extracted from rolling cross-sector correlation matrices across all ten S&P 500 GICS sectors. Models are evaluated under a strict out-of-sample design — trained on 2000–2010 and tested on 2011–2024 — ensuring results reflect genuine predictive ability rather than in-sample overfitting.

## Approach
## Core Idea
Standard risk measures like VIX only rise after the market has already started falling. This framework asks whether the structure of connections between market sectors contains forward-looking information about vulnerability — before prices reflect it.

## Data
- Universe: S&P 500 constituents across 10 GICS sectors
- Period: January 2000 – December 2024 (~25 years)
- Crisis episodes: Dot-com collapse, Global Financial Crisis, European Sovereign Debt Crisis, COVID-19, 2022 Bear Market

## Network Biomarkers
- Four daily scalar measures extracted from rolling sector correlation matrices:
- Network Density — degree of sector co-movement
- Clustering Coefficient — speed of shock propagation
- Max Eigenvector Centrality — systemic hub dominance
- Average Edge Weight — broad market synchronization

## Models
- Logistic Regression (baseline)
- Gradient Boosted Trees (XGBoost)
- Sector Rotation Signal integration for earlier warning generation

## Evaluation
- Strict out-of-sample design: trained 2000–2010, tested 2011–2024
- Primary metric: AUC (robust to class imbalance from rare crash events)
- Economic validation via backtested Long/Cash trading strategy

## Key Findings
- Network biomarkers contain forward-looking crash prediction information beyond VIX
- XGBoost captures non-linear fragility signals with meaningful out-of-sample performance
- Sector Rotation Signal generates signals 2–4 weeks earlier than correlation-only models
- Long/Cash trading strategy achieves superior risk-adjusted returns vs buy-and-hold SPY with meaningfully reduced maximum drawdown
- COVID-19 treated as an explicit boundary condition — the framework targets endogenous fragility, not exogenous shocks
###### Full results, methodology, and code will be released upon journal publication.

## Tools & Libraries
- Language: Python
- Pandas, NumPy, Scikit-learn, XGBoost, Matplotlib, NetworkX, SciPy, Statsmodels

## Key References
- Billio et al. (2012) — Connectedness and systemic risk
- Gu, Kelly & Xiu (2020) — Empirical asset pricing via machine learning
- Welch & Goyal (2008) — Equity premium prediction
- Moskowitz & Grinblatt (1999) — Industry momentum and sector rotation
- Watts & Strogatz (1998) — Small-world network dynamics

## Author
- Atisha Karki | MS Quantitative Finance & Economics, Texas State University
atishakarki28@gmail.com 
