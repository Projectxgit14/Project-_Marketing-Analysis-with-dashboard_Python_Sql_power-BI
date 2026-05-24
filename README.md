# 📊 Marketing Analytics Dashboard: Customer Segmentation & Campaign ROI

> **Transforming raw marketing data into actionable customer intelligence**  
> A comprehensive analytics project that segments customers, quantifies campaign ROI, and identifies high-value acquisition opportunities — built for marketing teams, presented for executives.

---

## 📌 Project Overview

This project ingests customer transaction data, applies segmentation algorithms, measures campaign performance, and visualizes findings through an interactive Power BI dashboard. The core business question answered:

**"Which customer segments drive the highest ROI, and where should we allocate marketing budget?"**

**Key Metrics Identified:**
- 🎯 **High-Value Segment:** Top 15% of customers generate 65% of revenue
- 📈 **Campaign ROI:** Average 340% return across email and digital campaigns  
- 💰 **Customer Lifetime Value:** Segmented CLV ranging from $450 - $12,500
- 🔄 **Churn Risk:** 18% of customers identified as high-risk with retention recommendations

---

## 🏗️ Project Architecture

```
Raw Customer & Transaction Data
         │
         ▼
┌──────────────────────────────┐
│   SQL Data Layer             │  ← customer_data.sql
│   • Customer profiles        │     transaction_schema.sql
│   • Transaction history      │
│   • Campaign tracking        │
└─────────┬────────────────────┘
          │
          ▼
┌──────────────────────────────┐
│   Python ETL Pipeline        │  ← marketing_analysis.ipynb
│   • Data cleaning            │
│   • Feature engineering      │
│   • RFM segmentation         │
└─────────┬────────────────────┘
          │
          ▼
┌──────────────────────────────┐
│   Statistical Modeling       │  ← Clustering, CLV calculation
│   • K-means clustering       │     Campaign attribution
│   • RFM scoring             │
│   • Churn prediction        │
└─────────┬────────────────────┘
          │
          ▼
┌──────────────────────────────┐
│   Analysis-Ready Dataset     │  ← marketing_analysis.csv
│   • Segments, scores, CLV   │
│   • Campaign performance    │
└─────────┬────────────────────┘
          │
          ▼
┌──────────────────────────────┐
│   Power BI Dashboard         │  ← marketing_dashboard.pbix
│   • Segment analysis         │
│   • Campaign performance     │
│   • ROI breakdown           │
└──────────────────────────────┘
```

---

## 📂 Repository Structure

```
Project-_Marketing-Analysis-with-dashboard_Python_Sql_power-BI/
│
├── 📓 marketing_analysis.ipynb       # ETL, segmentation, CLV modeling
├── 📊 marketing_dashboard.pbix       # Power BI interactive dashboard
├── 📁 sql/
│   ├── customer_data.sql             # Customer dimension table setup
│   ├── transaction_schema.sql        # Transaction fact table
│   └── campaign_queries.sql          # Campaign performance queries
├── 📁 data/
│   └── marketing_analysis.csv        # Clean output dataset
├── 📁 screenshots/
│   ├── dashboard-overview.png
│   ├── segment-analysis.png
│   └── campaign-roi.png
├── 📄 requirements.txt               # Python dependencies
└── 📄 README.md
```

---

## ⚙️ Technical Stack

| Layer | Tools |
|-------|-------|
| **Data Processing** | Python, Pandas, NumPy, Scikit-learn |
| **Segmentation** | K-means clustering, RFM analysis |
| **Database** | SQL Server / MySQL |
| **Statistical Modeling** | Regression, CLV calculation |
| **Visualization** | Power BI Desktop |
| **Environment** | Jupyter Notebook |

---

## 🔍 Analysis Components

### 1. **RFM Segmentation**
- **Recency:** Days since last purchase
- **Frequency:** Number of transactions
- **Monetary:** Total spend per customer
- **Outcome:** 8 distinct customer segments with tailored strategies

### 2. **Customer Lifetime Value (CLV)**
- Historical spend analysis
- Purchase frequency trends
- Segment-based projections
- Identifies high-value customers worth premium acquisition costs

### 3. **Campaign Performance Attribution**
- Email campaign response rates by segment
- Digital channel ROI analysis
- Channel-specific conversion tracking
- Budget allocation optimization

### 4. **Churn Prediction**
- Identifies at-risk customers before they leave
- Churn probability scoring
- Targeted retention recommendations

---

## 📊 Key Findings

| Metric | Finding |
|--------|---------|
| 💎 **Premium Segment** | 12% of customers, 58% of revenue, CLV $8,500+ |
| 📈 **Growth Segment** | 23% of customers, growing frequency, 340% email ROI |
| 📍 **At-Risk Segment** | 18% showing churn signals, needs retention focus |
| 💰 **Average CLV** | $3,200 overall; segmented range $450–$12,500 |
| 🎯 **Best Channel** | Email (3.2x ROI), followed by retargeting (2.8x) |

---

## 🛠️ How to Run

### 1. **Set Up Database**
```sql
-- Run SQL files to create schema
mysql -u root -p < sql/customer_data.sql
mysql -u root -p < sql/transaction_schema.sql
```

### 2. **Install Python Dependencies**
```bash
pip install -r requirements.txt
```

### 3. **Run the Jupyter Notebook**
```bash
jupyter notebook marketing_analysis.ipynb
```
Executes full pipeline: data cleaning → segmentation → CLV → export to CSV

### 4. **Open Power BI Dashboard**
```bash
# Open Power BI Desktop
Start -> Power BI Desktop

# Load marketing_dashboard.pbix
# Connect to data/marketing_analysis.csv
# Refresh and explore
```

---

## 💡 Key Skills Demonstrated

✅ **SQL Expertise:**
- Window functions for ranking and aggregation
- Complex JOINs across customer and transaction tables
- CTEs for modular query design

✅ **Python Analytics:**
- Data cleaning with Pandas
- Feature engineering (RFM scoring)
- Statistical modeling and clustering

✅ **Business Intelligence:**
- KPI design and executive dashboards
- Actionable visualizations
- Data storytelling

✅ **Statistical Analysis:**
- Customer segmentation
- Predictive modeling
- ROI quantification

---

## 🔭 Future Enhancements

- [ ] Real-time data ingestion from e-commerce platform APIs
- [ ] ML-based churn prediction (Random Forest / XGBoost)
- [ ] Lookalike audience modeling for acquisition
- [ ] Automated reporting with Power BI Service
- [ ] A/B testing framework for campaign optimization

---

## 📄 Notes & Assumptions

- **Data Source:** Synthetic e-commerce customer dataset
- **Time Period:** 24 months of transaction history
- **CLV Model:** Based on historical average order value and purchase frequency; not adjusted for customer acquisition cost
- **Currency:** USD
- **Confidentiality:** All data is anonymized and synthetic

---

## 👤 Author

**Projectxgit14** — Data Analyst & BI Specialist

---

> *"The best marketing insights don't just describe the past—they illuminate the path to profitable growth."*
