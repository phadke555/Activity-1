# 📈 Trade & Order Book Analysis for PXA

**Author:** Rohan Phadke  
**Last Updated:** 03/07/2025
**Part of FINS 3666: Proprietary Trading and Market Making Class at UNSW**

---

## 📌 Overview
This project analyzes **market microstructure** using **trades and limit order book (LOB) data** for the stock **PXA.X** on **January 15, 2025**. The goal is to **understand order execution dynamics, bid-ask spread behavior, and liquidity conditions** by integrating trade and LOB data.

---

## 📂 Repository Structure

| File | Description |
|------|------------|
| 📄 `PXA.X 20250115 Market Depth Legacy x10.csv` | Raw **limit order book (LOB)** data |
| 📄 `PXA.X 20250115 Stocks Trades.csv` | Raw **trade execution data** |
| 📄 `PXA_filtered_merged.csv` | **Merged LOB & trade data** for analysis; created by the author |
| 📊 `orders_analysis.ipynb` | **Explores LOB depth, spread, & liquidity metrics** |
| 📊 `trades_analysis.ipynb` | **Analyzes trade price behavior & execution efficiency** |
| 📄 `requirements.txt` | Dependencies for reproducibility |

---

## 🛠️ Methodology

### 1️⃣ Data Preprocessing
- **Merged trades with the closest LOB snapshot** before execution.
- **Cleaned timestamps and converted timezones** to ensure consistency.
- **Created the PXA_filtered_merged.csv** after filtering and merging containing 4408 observations. Originally there were 25K orders and 4575 trades.

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

---

## 🚀 Future Enhancements

- **Implement real-time execution simulation** to test different order execution strategies.  
- **Apply machine learning models** to predict **spread tightening/widening**.  
- **Analyze impact of large institutional orders** on market liquidity.  

---

## 📦 Installation & Usage

### 🔧 Dependencies
Install required packages:
pip install -r requirements.txt
