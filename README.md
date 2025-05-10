# 📘 Forecasting Retail Book Sales for a Global Publishing Data Provider

## Overview
This project was conducted in collaboration with a **leading global data and analytics provider for the publishing industry**, renowned for supplying real-time sales intelligence across international book markets. The objective was to develop scalable, high-impact forecasting solutions that enable **independent publishers** to make data-driven decisions regarding print runs, stock levels, and commercial investments.

Leveraging real-world weekly retail sales data, this project applied a comprehensive range of time series modeling techniques—including classical statistical methods, machine learning, deep learning, and hybrid approaches. Two prominent book titles were selected to represent distinct sales archetypes: one with stable, long-tail demand and another with high seasonal and promotional variability.

---

## 🎯 Objectives
- Transform multi-tab Excel-based commercial sales data into model-ready weekly time series.
- Detect seasonal patterns, structural trends, and data stationarity.
- Benchmark forecasting methods: SARIMAX, XGBoost, and LSTM.
- Develop hybrid models combining traditional and modern forecasting paradigms.
- Generate monthly forecasts to support strategic inventory and print planning.
- Quantify revenue opportunities using forecasted unit sales and historical pricing (ASP).

---

## 📊 Dataset
The dataset provided by the client captures **weekly point-of-sale transactions** from across the UK’s major book retailers. Each record includes:
- ISBN (book identifier)
- End Date (week-ending date)
- Volume (units sold)
- ASP (average selling price)

A companion dataset provides bibliographic metadata such as author, format, RRP, imprint, and publication date. The project uses two anonymised titles to illustrate the forecasting methods.

> ⚠️ Note: Data has been anonymised for confidentiality. Titles and identifying details have been masked.

---

## 🧠 Methods Used
- **Data Engineering**: Multi-tab ingestion, resampling, alignment, missing week imputation
- **Exploratory Analysis**: Time-based plots, STL decomposition, seasonality inspection
- **Modeling**:
  - SARIMAX with auto-ARIMA selection
  - XGBoost with lag feature engineering and early stopping
  - LSTM using sliding windows and KerasTuner optimization
  - Hybrid (parallel & sequential) combining SARIMA + ML/DL residuals
- **Validation**: 32-week rolling holdout, MAE/MAPE benchmarking
- **Strategic Layer**: Revenue impact analysis using forecasted volume × ASP
- **Monthly Forecasting**: Resampled data to support medium-term business planning

---

## ✅ Key Findings
- **XGBoost outperformed all other approaches**, delivering the lowest forecasting error for both titles.
- **SARIMAX remains a robust, interpretable baseline** for stable, seasonal patterns.
- **LSTM underperformed** due to high variance and limited training sequences.
- **Hybrid models** did not consistently outperform base methods in this context.

### 💰 Estimated 8-Month Revenue Opportunity
| Title   | Forecasted Revenue |
|---------|--------------------|
| Title A | £561,148.51        |
| Title B | £2,771,211.21      |

These projections represent revenue that could be unlocked through more accurate reprint scheduling and inventory alignment.

---

## 🧾 Business Impact
- Enabled the client to prototype a **predictive forecasting tool** aimed at independent publishers lacking internal analytics resources.
- Provided a foundation for smarter title acquisition, supply chain management, and demand-driven marketing strategy.
- Demonstrated how ASP and volume forecasting can translate directly into actionable financial forecasts.

---


