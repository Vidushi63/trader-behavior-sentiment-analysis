# Trader Performance vs. Market Sentiment Analysis
**Project Submission: Junior Data Scientist Intern Assignment** **Author:** Vidushi Singh

---

## 📌 Project Overview
This project investigates the correlation between the **Bitcoin Fear & Greed Index** and trader performance data from the **Hyperliquid** exchange. The objective was to identify behavioral biases and propose data-driven strategies to optimize trading outcomes.

## 🛠️ Methodology
1. **Data Integration:** Cleaned and merged `historical_data.csv` and `fear_greed_index.csv`.
2. **Date Alignment:** Handled Unix timestamps (milliseconds) and normalized them to align with daily sentiment classifications.
3. **Segmentation:** Grouped traders into **Frequent** (active/pro) and **Infrequent** (retail/occasional) segments based on trade counts.
4. **Metric Calculation:** Developed logic for Win Rates, PnL analysis, and Average Position Sizing.

## 📊 Key Insights (Task B)
* **Performance Sensitivity:** Win rates peak for frequent traders during **Extreme Greed (49.7%)**, but drop significantly during **Neutral (29.8%)** phases.
* **The "Size-Up" Bias:** Traders tend to increase risk when emotions are high. Average position size jumps to **$5,660** in Extreme Greed, nearly double the **$3,058** average during Neutral days.
* **Segment Vulnerability:** **Infrequent traders** are highly successful in Neutral markets (65.6% win rate) but struggle during Extreme Greed (7.8% win rate), suggesting they are often "trapped" by high-volatility momentum shifts.

## 💡 Actionable Strategies (Task C)

### **Strategy 1: The "Greed Circuit Breaker"**
* **Target:** Infrequent Traders.
* **Rule:** Reduce capital allocation by **90%** or halt trading when the Fear & Greed Index exceeds 75.
* **Reasoning:** Historical data shows this group provides exit liquidity during extreme optimism, leading to a win rate drop of over 50%.

### **Strategy 2: The "Size Standardization" Protocol**
* **Target:** Frequent Traders.
* **Rule:** Cap position sizes at **$3,000** regardless of sentiment.
* **Reasoning:** Increasing size during "Fear" or "Greed" periods did not result in a higher win rate but significantly increased total drawdown risk.

---

## 🚀 Technical Stack
* **Python** (Pandas, Matplotlib, Seaborn)
* **Jupyter Notebook** (Kaggle Environment)
