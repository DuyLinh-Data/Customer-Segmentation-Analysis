
# 🛍️ UK Online Retail Sales Analysis (2010–2011)

**This project analyzes over 540,000 online retail transactions in the UK to identify customer behavior patterns, segment valuable customers, and generate insights that support business decision-making.**

---

## 📦 Dataset Overview

- **Source**: [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Online+Retail)
- **Period**: 01/12/2010 → 09/12/2011
- **Size**: ~540,000 transactions
- **Features**:
  - `InvoiceNo`, `StockCode`, `Description`, `Quantity`
  - `InvoiceDate`, `UnitPrice`, `CustomerID`, `Country`

---

## 🎯 Objectives

- Clean and preprocess transaction data
- Apply RFM (Recency, Frequency, Monetary) segmentation
- Perform customer clustering using KMeans
- Analyze purchasing behavior by country and region
- Identify customer groups for targeted marketing

---

## 🧹 Data Cleaning & Preparation

- Removed:
  - Rows with missing `CustomerID`
  - Negative quantities (returns)
  - Records with `UnitPrice <= 0`
- Parsed `InvoiceDate` to datetime
- Created:
  - `TotalPrice = Quantity * UnitPrice`
  - `InvoiceMonth` for monthly aggregation

---

## 📊 Key Analyses

### 🔁 RFM Segmentation

| Metric     | Description                      |
|------------|----------------------------------|
| Recency    | Days since last purchase         |
| Frequency  | Number of purchases              |
| Monetary   | Total spending amount            |

Segments identified:
- 🥇 Loyal customers
- 💸 Big spenders
- 💤 Inactive customers

---

### 🧠 Clustering (KMeans)

- Used **Elbow Method** to determine optimal clusters (K=4)
- Applied **KMeans** clustering on scaled RFM data
- Cluster labels:
  - High-value customers
  - Frequent buyers with low spending
  - Recent but low-value spenders
  - Dormant or at-risk customers

---

## 🌍 Key Insights

- 🇬🇧 UK accounts for the majority of sales; top foreign markets include Netherlands, Germany, France
- 💰 ~20% of customers contribute to ~80% of revenue (Pareto principle)
- ⚠️ A large proportion of one-time or low-frequency buyers—potential churn risk
- 🎯 Targeting **high-Monetary, low-Recency** segments can improve ROI

---

## 🚀 How to Run

1. **Clone the repo:**
```bash
git clone https://github.com/yourusername/uk-retail-analysis.git
cd uk-retail-analysis
```

2. **Install required packages:**
```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

3. **Launch Jupyter Notebook:**
```bash
jupyter notebook Final_project_sub.ipynb
```

---

## 🛠️ Technologies Used

- Python 3.x
- Jupyter Notebook
- Pandas, NumPy
- Seaborn, Matplotlib
- Scikit-learn (KMeans)

---

## 📁 Project Structure

```
📦 uk-retail-analysis/
├── data/                      # Raw & cleaned datasets
├── Final_project_sub.ipynb    # Main analysis notebook
├── README.md                  # Project documentation
```

---

## 🔭 Future Improvements

- Add visual dashboard with Streamlit or Power BI
- Test other clustering algorithms (DBSCAN, Agglomerative)
- Incorporate seasonality or product-level behavior
- Segment customers by geographic or channel-based attributes

---

## 📝 License

This project is licensed under the [MIT License](https://opensource.org/licenses/MIT).  
Feel free to use or modify it with credit.

---

## 👤 Author

**Nguyễn Duy Linh**  
📧 Email: linhnguyen.asia@gmail.com  
🔗 LinkedIn: [Nguyễn Duy Linh](https://www.linkedin.com/in/nguy%E1%BB%85n-duy-linh/)  
💻 GitHub: [AntoniNguyen123](https://github.com/AntoniNguyen123)

---

_“Without data, you're just another person with an opinion.” – W. Edwards Deming_
