# Data Science Internship: Trader Behavior vs Market Sentiment
**Author:** Vidushi Singh

## Methodology
- [cite_start]**Data Preparation:** Cleaned two datasets (Bitcoin Market Sentiment and Hyperliquid Historical Trader Data) by removing duplicates and handling missing values[cite: 7].
- [cite_start]**Time Alignment:** Converted raw Unix timestamps (milliseconds) to datetime objects and normalized them to a daily level to align trading activity with the Fear/Greed index[cite: 7].
- [cite_start]**Segmentation:** Classified traders into 'Frequent' (above average trade count) and 'Infrequent' segments to analyze behavioral differences[cite: 10].

## Key Insights
1. **Performance Variance:** Win rates are highly sensitive to sentiment. [cite_start]Frequent traders peak at a **49.7% win rate** during Extreme Greed but struggle during Neutral days (29.8%)[cite: 8].
2. **Behavioral Shifts:** Traders exhibit "Emotional Sizing." [cite_start]Average position sizes nearly double to **$5,660** during Extreme Greed compared to **$3,058** on Neutral days[cite: 9].
3. [cite_start]**Segment Risks:** Infrequent traders are "Neutral Specialists" with a **65.6% win rate** in calm markets but are statistically likely to fail during Extreme Greed (7.8% win rate)[cite: 10].

## Actionable Strategy Recommendations
- [cite_start]**Rule 1:** Infrequent traders should implement a "Greed Circuit Breaker," pausing all trading when the index hits Extreme Greed to preserve capital.
- [cite_start]**Rule 2:** Frequent traders should standardize position sizes across all sentiments to avoid the "oversizing" bias observed during Fear and Extreme Greed.
