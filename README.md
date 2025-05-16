# 🛒 Online Retail Customer Analytics

This project explores customer behavior using the [Online Retail dataset](https://archive.ics.uci.edu/ml/datasets/online+retail). It serves as a hands-on playground to practice data wrangling, analysis, and customer segmentation using Python (pandas, lifetimes, matplotlib/seaborn, etc.).


## 📊 Project Objectives

- ✅ Clean and prepare raw transaction data
- 📈 Visualize purchasing patterns and trends
- 🔁 Apply **RFM Analysis** for customer segmentation
- 💸 Estimate **Customer Lifetime Value (CLTV)** using both heuristic and probabilistic models
- 🔍 Explore **Customer Churn** using recency and frequency behavior
- 🎯 Lay foundation for data-driven marketing strategies


## 🧹 Data Cleaning Highlights

- Handle missing `Description`
- Number columns inspection (negative, outliers)
- Created new columns: `TotalSales` and added month-level granularity


## 🔍 Exploratory Analysis

- Sales trends over time
- Top-selling products and countries


## 📦 RFM Segmentation

| Metric     | Description                       |
|------------|-----------------------------------|
| **Recency** | Days since last purchase          |
| **Frequency** | Number of transactions           |
| **Monetary** | Total revenue per customer       |

Segment scores (1–4), combined into:
- `RFM_Score` (numeric)
- `RFM_Segment` (tuple)
- `Segment_Name` (e.g., Champions, Loyal Customers, Lost)


## 🔮 Customer Lifetime Value (CLTV)

### Simple Heuristic CLTV:
- Based on: `AOV × Purchase Frequency × Lifetime (months)`
- Conservative adjustments for one-time buyers

### Probabilistic CLTV (BG/NBD + Gamma-Gamma):
- Uses customer purchase history to forecast:
  - Future transactions
  - Expected order value
  - Predicted CLTV over 6 months


## 📚 Tech Stack

- Python 3
- pandas, numpy
- matplotlib, seaborn
- lifetimes
- jupyter notebook
