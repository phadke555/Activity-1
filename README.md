# 📈 Trade & Order Book Analysis for PXA.X

**Author:** Rohan Phadke  
**Last Updated:** 03/07/2025

---

## 📌 Overview
This project analyzes **market microstructure** using **trades and limit order book (LOB) data** for the stock **PXA.X** on **January 15, 2025**. The goal is to **understand order execution dynamics, bid-ask spread behavior, and liquidity conditions** by integrating trade and LOB data.

---

## 📂 Repository Structure

| File | Description |
|------|------------|
| 📄 `PXA.X 20250115 Market Depth Legacy x10.csv` | Raw **limit order book (LOB)** data |
| 📄 `PXA.X 20250115 Stocks Trades.csv` | Raw **trade execution data** |
| 📄 `PXA_filtered_merged.csv` | **Merged LOB & trade data** for analysis |
| 📊 `orders_analysis.ipynb` | **Explores LOB depth, spread, & liquidity metrics** |
| 📊 `trades_analysis.ipynb` | **Analyzes trade price behavior & execution efficiency** |
| 📄 `requirements.txt` | Dependencies for reproducibility |
| 🔬 `test.ipynb` | Testing scripts for data validation |

---

## 🛠️ Methodology

### 1️⃣ Data Preprocessing
- **Merged trades with the closest LOB snapshot** before execution.
- **Cleaned timestamps and converted timezones** to ensure consistency.

### 2️⃣ Market Microstructure Analysis
- **Bid-Ask Spread Analysis** 📊  
  - Measured L1-L10 spreads and liquidity conditions.
  - Plotted **spread changes over time** to detect liquidity shifts.

- **Mid-Price Calculations** 📈  
  - Compared **Simple Mid-Price, Volume-Weighted Mid-Price (VWMP), and Spread-Crossing VWMP**.
  - Evaluated accuracy by computing **MAE, MSE, RMSE, and correlation**.

- **Order Book Depth & Imbalance** 📉  
  - Computed **cumulative order depth** for bids and asks.
  - Measured **depth imbalance** to infer market pressure.

### 3️⃣ Trade Execution & Price Efficiency
- **Trade Price vs. Mid-Price**  
  - Analyzed **execution locations within the spread**.
  - Examined how **hidden orders impact execution quality**.

- **Trade Volume Aggregation**  
  - Grouped trades by timestamp to analyze **liquidity clustering**.

- **Regression Analysis**  
  - Fitted **linear models** to detect **trade price trends**.
  - Measured **correlation between L1 Mid-Price & trade execution prices**.

---

## 🔍 Key Findings

✅ **Liquidity fluctuates throughout the day**, with spread widening at specific periods.  
✅ **Trade prices often execute at or near the mid-price**, except in volatile conditions.  
✅ **Hidden orders & dark pool activity** result in **sub-penny price improvements**, despite a 1-cent bid-ask spread.  
✅ **Order flow imbalance correlates with price movements**, indicating predictive power for short-term price action.  

---

## 🚀 Future Enhancements

- **Implement real-time execution simulation** to test different order execution strategies.  
- **Apply machine learning models** to predict **spread tightening/widening**.  
- **Analyze impact of large institutional orders** on market liquidity.  

---

## 📦 Installation & Usage

### 🔧 Dependencies
Install required packages:
```bash
pip install -r requirements.txt