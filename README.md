# Trader Performance vs Market Sentiment Analysis

## Overview
This project analyzes how Bitcoin market sentiment (Fear vs Greed) impacts trader behavior and performance on the Hyperliquid trading platform.  
The goal is to identify behavioral patterns and derive actionable trading insights.

---

## Datasets Used
1. **Bitcoin Market Sentiment (Fear/Greed Index)**
   - Columns: Date, Classification
   - Daily sentiment classification

2. **Historical Trader Data (Hyperliquid)**
   - Includes trade-level data such as account, price, size, side, leverage, and PnL

---

## Methodology
- Loaded and cleaned both datasets
- Converted timestamps and aligned data at daily level
- Merged sentiment data with trader performance
- Created key metrics:
  - Daily PnL
  - Win rate
  - Trade frequency
  - Leverage usage
  - Long/Short ratio
  - Drawdown proxy
- Segmented traders by:
  - High vs Low leverage
  - Frequent vs Infrequent traders
  - Consistent vs Inconsistent performers

---

## Key Insights
- Trader performance differs between Fear and Greed days
- During Fear days, traders tend to reduce leverage and trade more cautiously
- Greed days show higher trade frequency and larger position sizes
- High leverage traders experience higher volatility and drawdowns
- Consistent winners show more controlled leverage usage

---

## Output Charts and Tables

The analysis results are supported by visualizations and summary tables generated in the notebook.

### Charts
Saved inside `outputs/charts/`, including:
- PnL distribution across Fear vs Greed days
- Win rate comparison by market sentiment
- Drawdown proxy by sentiment
- Trade frequency, leverage, and position size by sentiment
- Long vs Short bias across sentiment regimes

### Tables
Saved inside `outputs/tables/`, including:
- Trader segment counts (leverage, frequency, consistency)

---

## Strategy Recommendations
- Reduce leverage during Fear periods, especially for high-risk traders
- Increase trade frequency only for consistent performers during Greed days
- Avoid aggressive position sizing during high volatility sentiment phases

---

## Bonus
A simple classification approach was explored to predict next-day profitability using sentiment and behavioral features.

---

## How to Run
1. Open the notebook in Google Colab or Jupyter Notebook
2. Install required libraries:
   - pandas
   - numpy
   - matplotlib
   - seaborn
3. Run cells sequentially

---

## Project Structure
'''
sentiment_trader_behavior_analysis/
│
├── notebook/
│ └── analysis.ipynb
│
├── outputs/
│ ├── charts/
│ └── tables/
│
└── README.md
'''

