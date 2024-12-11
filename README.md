# Pairs-Trading-strategy

Cointegration and Pair Trading Strategy

This repository showcases a detailed project focused on cointegration analysis and pair trading strategies, blending theoretical foundations with practical implementation. The analysis leverages advanced statistical methods to identify cointegrated pairs and develop profitable trading strategies while addressing the challenges of real-world market conditions.

Project Overview

The primary goal of this project is to explore statistical arbitrage through cointegration and implement pair trading strategies. Using financial data, the project identifies pairs of stocks that exhibit long-term equilibrium relationships and constructs trading strategies based on deviations from their historical spread.

Key Features

Statistical Analysis
Descriptive Statistics: Examines daily and weekly returns, comparing simple and log returns to understand skewness, kurtosis, and variability.
Stationarity Testing: Utilizes the Dickey-Fuller test to confirm the stationarity of log prices and identify potential cointegrated pairs.
Cointegration Analysis
Conducts tests to identify pairs of stocks with cointegrated price series, indicating a stable long-term relationship.
Key pairs identified include Visa-Mastercard (V-MA) and Goldman Sachs-Morgan Stanley (GS-MS), which are optimal candidates for pair trading due to strong cointegration.
Pair Trading Strategy
Spread Calculation: Constructs a normalized spread (zt) to trigger trading signals based on mean reversion.
Trading Signals: Implements a threshold-based approach to identify entry and exit points for trades.
Risk Management: Incorporates leverage, stop-loss mechanisms, and rolling-window recalibration to enhance robustness.
Out-of-Sample Testing
Applies rolling-window analysis to estimate parameters dynamically, ensuring the strategy adapts to changing market conditions.
Implements tests for cointegration within each rolling window, avoiding trades during periods of weak or broken cointegration.
Methodology

Cointegration Testing
Tests pairs of assets for cointegration using the Phillips-Ouliaris test, ensuring statistical evidence of a long-term relationship.
Identifies the strongest cointegrated pairs by comparing p-values and critical thresholds.
Pair Trading Framework
Trading Logic: Short-sell one asset while buying the other when the spread exceeds a threshold, anticipating mean reversion.
Profit Calculation: Demonstrates that profit equals the standardized spread at entry, multiplied by the spread’s standard deviation.
Dynamic Adjustments: Uses rolling windows to continuously update parameters, reflecting the evolving market environment.
Risk Controls
Leverage Management: Examines the impact of different leverage levels (e.g., 2x vs. 20x) on risk and returns.
Stop-Loss Mechanisms: Implements thresholds to mitigate risks from extreme market deviations.
No-Cointegration Periods: Ceases trading during non-cointegration periods to avoid unfavorable conditions.
Results and Observations

Performance: The pair trading strategy generated consistent profits under various configurations, with higher leverage amplifying returns and risks.
Challenges:
Autocorrelation in spread residuals suggests deviations may persist longer than anticipated, requiring a dynamic approach.
Transaction Costs and frequent trades can significantly impact profitability.
Insights: Strong cointegration pairs (e.g., V-MA) provide the best opportunities for pair trading, but strategies must adapt to changing relationships.
Applications

This project is highly relevant for:

Quantitative Finance: Demonstrating statistical arbitrage through robust analytical frameworks.
Algorithmic Trading: Developing systematic, rule-based trading strategies.
Risk Management: Addressing challenges like non-stationarity, autocorrelation, and dynamic market conditions.
Future Enhancements

Incorporate Transaction Costs: Simulate the impact of fees on trading profitability.
Explore Machine Learning: Use advanced models to predict spread behavior and improve entry/exit signals.
Expand to Multivariate Analysis: Analyze more than two assets simultaneously to capture complex relationships.
This project provides a comprehensive framework for pair trading and statistical arbitrage, offering valuable insights into the practical application of cointegration in financial markets.
