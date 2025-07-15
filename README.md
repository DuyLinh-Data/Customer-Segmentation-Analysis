# 🛍️ UK Online Retail Sales Analysis (2010–2011)

***This project analyzes transactional data from a UK-based online retail company to uncover customer behavior, identify valuable customer segments, and extract actionable insights that support business decision-making.***

---

## 📦 Dataset Overview

- **Source**: UCI Machine Learning Repository
- **Period**: 01/12/2010 → 09/12/2011
- **Records**: ~540,000 transactions
- **Features**:
  - `InvoiceNo`, `StockCode`, `Description`, `Quantity`
  - `InvoiceDate`, `UnitPrice`, `CustomerID`, `Country`

---

## 🎯 Objectives

- Clean and preprocess transactional data for accuracy
- Conduct RFM (Recency, Frequency, Monetary) analysis
- Perform customer segmentation using clustering (KMeans)
- Analyze customer purchasing behavior by region
- Identify key customer groups for retention and marketing

---

## 🧹 Data Cleaning & Preparation

- Removed:
  - Null `CustomerID`
  - Negative `Quantity` (returns or errors)
  - Transactions with `UnitPrice <= 0`
- Converted `InvoiceDate` to datetime format
- Created new columns:
  - `TotalPrice = Quantity * UnitPrice`
  - `InvoiceMonth` for monthly aggregation

---

## 📊 Key Analyses

### 🔁 RFM Segmentation

| Metric     | Description                            |
|------------|----------------------------------------|
| Recency    | Days since last purchase               |
| Frequency  | Total number of purchases              |
| Monetary   | Total money spent                      |

Customers were grouped into segments based on RFM scores to identify:
- 🥇 Loyal customers
- 💸 Big spenders
- 💤 Inactive customers

### 🧠 Clustering (KMeans)

- Used **Elbow Method** to determine optimal number of clusters (K=4)
- Applied **KMeans** to classify customers into groups
- Labeled clusters for business understanding:
  - High-value customers
  - Low-frequency buyers
  - Recent-but-low spenders
  - Dormant clients

---

## 🌍 Insights

- 🇬🇧 **Most sales came from the UK**, but notable high-spending clients also came from Netherlands, Germany, and France.
- 💵 **A small group of customers generated a large portion of revenue** (Pareto principle holds).
- 📉 Many one-time customers or low-frequency buyers exist — representing churn risk.
- 🧭 Retargeting high-Monetary, low-Recency customers could improve ROI on campaigns.

---

## 🛠️ Technologies Used

- Python 3.x
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn (KMeans)
- Jupyter Notebook

---

## 📁 Folder Structure

├── data/ # Raw and cleaned data files (optional)<br>
├── Final_project_sub.ipynb # Main analysis notebook<br>
├── README.md



---


👤 Author
Nguyễn Duy Linh<br>
Email: linhnguyen.asia@gmail.com<br>
Linkedin: https://www.linkedin.com/in/nguy%E1%BB%85n-duy-linh/
