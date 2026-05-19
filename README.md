# Retail Demand Forecasting

## Project Overview
This project focuses on forecasting retail sales demand using historical time series data and machine learning techniques. The objective is to identify sales trends, seasonality patterns, and short-term demand behavior in order to improve future sales predictions.
The project demonstrates a complete machine learning workflow, including exploratory data analysis, time series feature engineering, forecasting model development, model evaluation, and business-focused recommendations.
This project was designed to strengthen practical machine learning and forecasting skills commonly used in retail, supply chain, and business analytics roles.
Retail businesses rely heavily on accurate demand forecasting to support:
* Inventory planning
* Staffing decisions
* Supply chain management
* Seasonal preparation
* Revenue forecasting
Poor forecasts can lead to:
* Stock shortages
* Overstocking
* Lost revenue opportunities
* Increased operational costs
The goal of this project is to build forecasting models capable of predicting future retail sales demand using historical sales behavior and time-based patterns.

---

**Dataset**

Store Sales - Time Series Forecasting (https://www.kaggle.com/competitions/store-sales-time-series-forecasting/data)

The dataset contains historical retail sales transactions across multiple stores and product categories.
Key files used:
* train.csv
* stores.csv
* oil.csv
* holidays_events.csv

---

## Business Objectives
- How long do customers remain active after their first purchase?
- Which customer segments generate the most revenue?
- Where should retention and marketing efforts be focused?

---

## Tools Used
- **Python** 
- **Pandas**: data manipulation and feature engineering
- **NumPy**: numerical operations
- **Matplotlib**: data visualizations
- **Scikit-learn**: machine learning models and evaluation
- **Gradient Boosting Regressor**: advanced forecasting model
- **Jupyter Notebook**: project development and experimentation
- **Github**: version control and project documentation

---

## Project Workflow

### 1) Data Loading & Exploration
Initial exploration included:
* Understanding dataset structure
* Inspecting missing values
* Reviewing sales behavior over time
* Aggregating daily sales data

---

### 2) Time Series Analysis
The project explored:
* Long-term sales trends
* Weekly seasonality
* Monthly seasonality
* Holiday-related sales behavior
Key observations:
* Retail sales increased consistently over time
* Weekends generated higher sales volumes
* December showed major seasonal sales spikes
* February consistently had lower sales activity

---

## Feature Engineering
Several forecasting-focused features were engineered to improve predictive performance.

**Lag Features**

Historical sales values were used as predictors:
* lag_1 -> previous day sales
* lag_7 -> sales from the same day the previous week
These features help the model learn short-term demand momentum and weekly behavioral patterns.

**Rolling Statistics**

* rolling_mean_7 -> a 7-day rolling average

This smooths short-term fluctuations and captures broader sales trends.

**Calendar Features**

Date-based features were extracted from the dataset:
* Day of the week
* Month
* Year
These features allow the model to capture seasonality and long-term growth patterns.

**Holiday Features:**

Holiday dates were merged into the dataset using **is_holiday**. 
This was used to help the model identify unusual demand behavior during holidays and special events.

---

## Machine Learning Models

**Baseline Model — Linear Regression**

A Linear Regression model was initially trained using lag and rolling features.
The model successfully captured:
* Overall sales trend
* Weekly demand patterns
* General movement in sales data
However, the model struggled with:
* Sudden spikes
* Nonlinear behavior
* Holiday anomalies

**Advanced Model — Gradient Boosting Regressor** 

A Gradient Boosting Regressor was later implemented to improve forecasting accuracy.
This model significantly improved:
* Prediction accuracy
* Nonlinear pattern recognition
* Adaptability to changing sales behavior

---

## Model Evaluation
Forecasting performance was evaluated using **Mean Absolut Error (MAE)**.
* **Model**: Linear Regression, **MAE**: ~84,245
* **Model**: Gradient Boosting Regressor, **MAE**: ~71,937

The Gradient Boosting model reduced forecasting error substantially and produced more realistic predictions overall.

---

## Key Insights
- Retail sales exhibit strong long-term upward growth trends.
- Weekend sales are consistently higher than weekday sales.
- December experiences the strongest sales demand due to seasonal shopping behavior.
- Lag-based features were among the strongest predictors of future demand.
- Forecasting models handled general trends effectively but still struggled with sudden anomalies and extreme spikes.
- Gradient Boosting significantly outperformed Linear Regression by learning more complex demand patterns.

---

## Business Recommendations
- Increase inventory and staffing during weekends and holiday seasons.
- Prepare early for December demand spikes to avoid stock shortages.
- Use forecasting models to support operational planning and purchasing decisions.
- Monitor unusual sales spikes separately, as anomalies remain difficult to predict accurately.
- Improve future forecasting performance by incorporating external factors such as promotions, marketing campaigns, and economic indicators.

---

## Repository Structure

```
retail_demand_forecasting/
│
├── data/
│   ├── train.csv
│   ├── stores.csv
│   ├── oil.csv
│   └── holiday_events.csv
│
├── python/
│   ├── retail_demand_forecasting.ipynb
│
├── visuals/
│   └── actual_predicted_lrv1.png
│   └── actual_predicted_lrv2.png
│   └── actual_predicted_lrv3.png
│   └── actual_predicted_xgb.png
│   └── av_weekday_sales.png
│   └── avg_monthly_sales.png
│   └── daily_sales.png
│   └── feature_importance.png
│
└── README.md
```

---

## Portfolio Value
This project demonstrates practical machine learning and forecasting skills relevant to data analytics and data science roles, including:
- Time series analysis
- Forecasting workflows
- Feature engineering
- Regression modeling
- Model evaluation
- Business interpretation of ML results
- Model comparison and experimentation
The project also reflects real-world ML development practices such as iterative improvement, debugging, and feature-driven model optimization.

---

## Author

**Ibrahim M. Hassan**
Data Analytics & Machine Learning Portfolio Project
