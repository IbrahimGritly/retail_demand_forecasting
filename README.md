# Retail Demand Forecasting

## Project Overview
This project focuses on forecasting retail sales demand using historical time series data and machine learning techniques. The objective is to identify sales trends, seasonality patterns, and short-term demand behavior in order to improve future sales predictions.
The project demonstrates a complete machine learning workflow, including exploratory data analysis, time series feature engineering, forecasting model development, model evaluation, and business-focused recommendations.
This project was designed to strengthen practical machine learning and forecasting skills commonly used in retail, supply chain, and business analytics roles.

**Data:** https://www.kaggle.com/competitions/store-sales-time-series-forecasting/data

---

## Business Objectives
- How long do customers remain active after their first purchase?
- Which customer segments generate the most revenue?
- Where should retention and marketing efforts be focused?

---

## Tools Used
- **Python**: pandas, matplotlib, seaborn  
- **Techniques**: Cohort Analysis, RFM Segmentation, Exploratory Data Analysis  

---

## Analysis Summary

### 1) Data Cleaning & Customer Classification
- Cleaned and prepared transactional data
- Created revenue metrics
- Classified customers into:
  - One-time buyers  
  - Repeat buyers (≤ 10 purchases)  
  - Loyal customers  

**Insight:**
- Most customers are repeat buyers, indicating moderate but consistent engagement.

---

### 2) Cohort Analysis (Customer Retention)
Customers were grouped by their **first purchase month** to track retention over time.

**Key Findings:**
- Retention drops sharply after the first month across all cohorts
- Most customers do not remain active beyond 3–4 months
- Newer cohorts show slightly improved retention
- Early churn presents a major opportunity for targeted retention campaigns

**Retention Heatmap**
![Cohort Retention Heatmap](assets/retention_p3.png)

---

### 3) Customer Geography & Seasonality
- **90% of total sales come from the UK**, followed by Germany and France
- Sales increase starting in **August** and peak in **October**, showing strong seasonality

---

### 4) RFM Analysis (Customer Value Segmentation)
Customers were segmented using **Recency, Frequency, and Monetary (RFM)** analysis.

**Segments Identified**
- Loyal Customers  
- Potential Loyalists  
- Others  
- At Risk  

**Key Insights**
- Loyal Customers contribute approximately **11.6M** in revenue
- Potential Loyalists represent growth opportunities
- At Risk customers contribute the least revenue (~1M)
- No “Champion” customers were identified, highlighting low high-frequency repeat behavior

---

## Business Recommendations
- Prioritize retention strategies for Loyal Customers to protect revenue
- Target Potential Loyalists with personalized campaigns to increase frequency
- Address early churn with incentives for first-time and repeat buyers
- Align marketing efforts with seasonal sales peaks (August–October)
- Focus geographic strategies on high-revenue regions (UK, Germany, France)

---

## Repository Structure

```
Healthcare-No-Shows-Analysis/
│
├── assets/
│   ├── monthly_revenue_p3.png
│   ├── retention_p3.png
│   ├── revenu_customer_ecommerce.png
│   └── revenue_segment_p3.png
│
├── python/
│   ├── commerce_data_cleaning.ipynb
│   ├── ecommerce_eda.ipynb
│   └── ecommerce_rfm.ipynb
│
├── report/
│   └── ecommerce project report.pdf
│
└── README.md
```

---

## Deliverables
- **Python** → [python/](python/)
- **Project Report** → [report/](report/)
- **Dashboard Screenshots** → [assets/](assets/)

---
