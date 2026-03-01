# 🛒 Retail Chain Sales Data Analysis & Reporting

A complete end-to-end data analysis project built as part of the **Internship Studio Final Project**. Analyses 124,969 retail transactions across 2011–2015 using Python, SQL, pandas, and data visualisation tools.

---

## 📁 Project Structure

```
retail-sales-analysis/
│
├── data/
│   ├── MainData.csv               # Transaction records (124,969 rows)
│   └── AddAnlys.csv               # Customer RFM segments (6,884 rows)
│
├── retail_sales_dashboard.html    # Interactive analysis dashboard
├── retail_analysis.pptx           # Full project presentation (15 slides)
└── README.md
```

---

## 📊 Dataset

| Field | Description |
|---|---|
| `customer_id` | Unique customer identifier |
| `trans_date` | Transaction date |
| `response` | Campaign response (0 or 1) |
| `tran_amount` | Transaction value (₹) |
| `segment` | RFM segment — P0 (Premium) / P2 (Standard) |
| `frequency` | Total purchases per customer |
| `monetory` | Total lifetime spend per customer |

---

## 🔧 Tools & Technologies

- **Python** — pandas, matplotlib, seaborn
- **SQL** — schema design, DDL, data cleaning, aggregation queries
- **Excel** — summary tables and reporting
- **HTML / CSS / JS + Chart.js** — interactive dashboard

---

## 🚀 Project Phases

### Phase 1 — Data Collection & Database Setup
- Loaded CSV data into a relational SQL database
- Designed schema with two tables: `transactions` and `customer_segments`
- Created indexes on `customer_id` and `trans_date` for query performance
- Established foreign key relationship between tables

### Phase 2 — Data Cleaning & Preparation
- Checked for null values → **zero nulls found**
- Checked for duplicate rows → **zero duplicates found**
- Outlier detection using IQR method (Q1=₹47, Q3=₹83) → **no extreme outliers**
- Parsed dates correctly using `pd.to_datetime(..., dayfirst=True)`
- Added derived columns: `year`, `quarter`, `day_of_week`
- Flagged partial years at 2011/2015 edges and February dip (fewer days)

### Phase 3 — Data Analysis
- Annual and monthly revenue trend analysis
- RFM segmentation comparison (P0 Premium vs P2 Standard)
- Purchase frequency distribution across customer base
- Campaign response rate trend (2011–2014)
- Customer cohort analysis by first purchase year
- Advanced SQL queries: top customers, monthly trends, segment revenue

### Phase 4 — Reporting & Findings
- Annual sales summary table with YoY comparisons
- Segment performance report (P0 vs P2)
- Customer journey map across 5 stages
- 6 key findings with actionable recommendations
- Interactive HTML dashboard + PowerPoint presentation (15 slides)

---

## 📈 Key Results

| Metric | Value |
|---|---|
| Total Revenue | ₹8.12M |
| Total Transactions | 124,969 |
| Unique Customers | 6,884 |
| Average Basket Size | ₹65.00 |
| Campaign Response Rate | 11.1% (peak 12.6% in 2014) |
| Customer Retention | **100%** — all customers are repeat buyers |
| P0 Revenue Share | **80%** of total revenue from 64% of customers |

---

## 🔍 Key Findings

1. **Revenue Stability** — Annual revenue steady at ~₹2.1M (2012–2014) with no seasonal spikes. Future growth must come from new customer acquisition.
2. **P0 Segment Dominance** — Premium customers spend 39% more per transaction (₹70 vs ₹50). A P2→P0 migration program could unlock ₹200K+ annually.
3. **Exceptional Retention** — 100% repeat buyer rate across all 6,884 customers — extraordinary for a retail chain.
4. **Acquisition Cliff** — 94.4% of customers first purchased in 2011. Only 386 new customers since 2012 — the #1 growth risk.
5. **Improving Campaign ROI** — Response rate grew from 9.8% → 12.6% over 4 years (+28% improvement).
6. **High Frequency Base** — Average customer buys 18.2 times. 561 ultra-loyal customers (26+ purchases) are strong VIP program candidates.

---

## 📊 Live Dashboard 

👉 [Live Demo](https://sales-analysis-omkar.netlify.app)

---

## 💡 How to Run

1. Clone the repo
   ```bash
   git clone https://github.com/YOUR-USERNAME/retail-sales-analysis.git
   cd retail-sales-analysis
   ```

2. Open the interactive dashboard
   ```bash
   # Just open in any browser
   retail_sales_dashboard.html
   ```

3. Open `retail_analysis.pptx` in PowerPoint or Google Slides for the full presentation

---

## 🙏 Acknowledgements

- Dataset sourced via [Kaggle](https://www.kaggle.com/datasets/regivm/retailtransactiondata)
- Project structure and guidance by [Internship Studio](https://www.internshipstudio.com)

---

*Built as part of the Internship Studio Data Analysis Final Project*
