# Telecom Customer Churn Analytics Dashboard

**End-to-end data analytics project** | Python · SQL · Power BI · Machine Learning

---

## Project Overview

Built a full business intelligence solution to identify and predict customer churn in the telecom industry — framed around real-world ISP operations (Broadband, TV, Phone services). The project covers the complete data analyst workflow: raw data → Python pipeline → SQL KPIs → Power BI dashboard → ML churn prediction model.

**Business Problem:** A telecom company loses 26.6% of customers annually, putting £139,131/month in revenue at risk. This project identifies *who* churns, *when*, and *why* — and assigns each customer an ML-generated churn probability score.

---

## Key Findings

| Metric | Value |
|---|---|
| Overall churn rate | 26.6% |
| Revenue at risk | £139,131 / month |
| Month-to-month churn | 42.7% (vs 2.8% on 2-year contracts) |
| Fibre optic churn | 41.9% — highest risk service type |
| Early-life churn (0–6 months) | 53.3% of customers |
| ML model accuracy | 79.2% (Random Forest) |
| High-risk customers identified | 1,662 customers (avg 84.6% churn probability) |

---

## Tech Stack

| Layer | Tool |
|---|---|
| Data cleaning & EDA | Python (pandas, matplotlib, seaborn) |
| Database | SQLite via SQLAlchemy |
| KPI queries | SQL |
| Dashboard | Microsoft Power BI (DAX measures) |
| Machine Learning | scikit-learn (Random Forest Classifier) |
| Environment | Google Colab |

---

## Project Structure

```
telecom-churn-dashboard/
│
├── Telecom_Customer_Churn_Analytics_Dashboard.ipynb   # Full Python notebook (EDA + SQL + ML)
├── Telecom_Churn_Dashboard.pbix                       # Power BI dashboard file
│
├── customers_clean.csv      # Cleaned dataset (7,032 customers)
├── kpi_summary.csv          # Executive KPI summary
├── kpi_bundle.csv           # Churn by service bundle
├── kpi_tenure.csv           # Churn by tenure cohort
├── kpi_payment.csv          # Churn by payment method
├── churn_predictions.csv    # ML churn probability scores
│
└── README.md
```

---

## Dashboard Pages

### Page 1 — Executive Overview
- KPI cards: Total Customers, Total Churned, Churn Rate %, Revenue at Risk
- Churn rate by contract type (bar chart)
- Churn split donut (Yes vs No)

### Page 2 — Segment Analysis
- Churn by tenure cohort (when do customers leave?)
- Churn by internet service type
- Churn by payment method

### Page 3 — At-Risk Customers
- Revenue at risk card (£100.48K for highest-risk segment)
- Customer Risk Map scatter (tenure vs monthly spend, coloured by churn)
- Filtered table: Fibre optic + Month-to-month customers
- ML Risk Score Summary (High: 84.6% / Medium: 43.2% / Low: 16.6%)

---

## How to Run

### Python Notebook
1. Open [`Telecom_Customer_Churn_Analytics_Dashboard.ipynb`](Telecom_Customer_Churn_Analytics_Dashboard.ipynb) in Google Colab
2. Run all cells in order — dataset downloads automatically (no Kaggle account needed)
3. Outputs: cleaned CSV files + `churn_predictions.csv`

### Power BI Dashboard
1. Open `Telecom_Churn_Dashboard.pbix` in Power BI Desktop (free)
2. If data doesn't load, update the file paths under **Home → Transform data → Data source settings**
3. Point each CSV to your local copy of this repository

---

## Dataset

**IBM Telco Customer Churn** — publicly available dataset, 7,043 customers, 21 variables including services subscribed (phone, internet, TV), contract type, tenure, monthly charges, and churn label.

Source: [IBM Sample Data Sets](https://github.com/IBM/telco-customer-churn-on-icp4d/tree/master/data)

---

## About

Built as a portfolio project to demonstrate end-to-end data analytics skills — connecting domain knowledge from telecom technical support to real business insights.

**Author:** Rohith Suresh Raj  
**LinkedIn:** [linkedin.com/in/rohith-suresh-raj-186804263](https://www.linkedin.com/in/rohith-suresh-raj-186804263)  
**Email:** rohith.sureshraj@gmail.com
