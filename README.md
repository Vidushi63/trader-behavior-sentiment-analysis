Trader Performance vs. Market Sentiment Analysis
Project for Primetrade.ai Data Science Internship Author: Vidushi Singh

1. Project Overview
This project analyzes the relationship between market sentiment (Bitcoin Fear & Greed Index) and actual trader performance on the Hyperliquid exchange. The goal is to identify behavioral shifts in traders and provide data-backed strategy recommendations to improve profitability.

2. Methodology
Data Acquisition: Integrated two datasets: historical_data.csv (Hyperliquid trades) and fear_greed_index.csv (Sentiment data).

Data Cleaning: - Resolved Unix timestamp issues by converting millisecond integers to normalized datetime objects.

Handled missing values and duplicates to ensure accurate daily alignment.

Feature Engineering: - Created a is_win metric to identify profitable trades.

Segmented traders into Frequent (above average trade counts) and Infrequent groups to isolate behavior patterns.

3. Key Insights (Task B)
Based on the analysis of thousands of trades, the following insights were discovered:

Performance Sensitivity: Win rates fluctuate significantly with sentiment. Frequent traders achieve their highest win rate (~49.7%) during Extreme Greed, while their performance drops during Neutral markets (~29.8%).

Emotional Sizing: Traders exhibit "Emotional Sizing." The average position size nearly doubles during Extreme Greed ($5,660) compared to Neutral days ($3,058), indicating that traders chase momentum with higher risk.

Segment Failure: Infrequent traders are highly successful in Neutral markets (65.6% win rate) but fail catastrophically during Extreme Greed (7.8% win rate), suggesting they are often caught on the wrong side of rapid market expansions.

4. Actionable Output & Strategies (Task C)
Based on the win-rate drops observed, I propose the following two strategy "Rules of Thumb":

Strategy 1: The "Greed Circuit Breaker"
Target: Infrequent/Retail Segment.

Rule: When the Fear & Greed Index enters the "Extreme Greed" zone (above 75), traders in this segment should stop trading or reduce position sizes by 90%.

Reasoning: Data shows this group's win rate drops below 10% during these periods, indicating they are likely providing exit liquidity for larger players.

Strategy 2: The "Size-Standardization" Protocol
Target: Frequent Traders.

Rule: Cap maximum position size to the "Neutral" market average ($3,000) regardless of sentiment.

Reasoning: Frequent traders currently increase their risk to ~$5,200 during Fear days, yet their win rate remains sub-50%. Standardizing size reduces total drawdown without significantly impacting the win-rate potential.

5. Technical Stack
Python: Primary analysis language.

Pandas: Data manipulation and cleaning.

Matplotlib/Seaborn: Data visualization.

Jupyter Notebook: Interactive development environment.
