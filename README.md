# Medilytics — Healthcare Revenue Intelligence Dashboard

A multi-role, interactive healthcare revenue analytics dashboard built with Streamlit, Plotly, and Pandas. Provides real-time insights into revenue leakage, claim denial risk, billing anomalies, and financial forecasting across hospital departments.

---

## Table of Contents

* Overview
* Features
* Project Structure
* Installation
* Running the App
* User Roles & Login Credentials
* Dashboard Pages
* Data Files
* Tech Stack
* Key Business Insights

---

## Overview

Medilytics is a healthcare revenue cycle management (RCM) intelligence platform designed for hospital finance teams.

It provides role-based access to CFOs, RCM analysts, department heads, and insurance teams so each user sees only relevant data.

The platform analyzes 60,000+ claim records across departments (Cardiology, Neurology, Orthopedics, Emergency Medicine) and multiple insurance types.

### Key Insights Generated:

* Revenue leakage points
* High-risk claim denial patterns
* Billing anomalies in the system
* Revenue forecast for next 6 months

---

## Features

* Role-Based Access Control (4 user roles)
* 7 Analytics Pages (end-to-end workflow)
* Executive Overview Dashboard
* Revenue Leakage Analysis
* Claim Denial Prediction (Logistic Regression)
* Billing Anomaly Detection (Z-score method)
* Revenue Forecasting (ARIMA model)
* Insurance Analytics Dashboard
* PDF Export functionality

---

## Project Structure

```
medilytics/
│── app.py                  # Entry point
│── login.py                # Authentication system
│── sidebar.py             # Navigation UI
│── chart_config.py        # Chart settings
│── pdf_export.py          # Export reports

│── Executive_Dashboard.py
│── Revenue_Leakage_Analysis.py
│── Claim_Denial_main.py
│── billing_anomaly.py
│── forecast_dashboard.py
│── cfo_strategic.py
│── insurance_view.py

│── style.css

│── data/
│   ├── modified_dataset.csv
│   ├── pre_processed_data.csv
│   ├── denial_model_predictions.csv
│   ├── monthly_revenue_history.csv
│   └── revenue_forecast.csv
```

---

## Installation

### Prerequisites

* Python 3.9+
* pip

### Steps

```bash
git clone https://github.com/RagzTechie/Medilytics_dashboard.git
cd Medilytics_dashboard
pip install -r requirements.txt
```

---

## Running the App

```bash
streamlit run app.py
```

Open in browser:
http://localhost:8501

---

## User Roles & Login Credentials

| Username       | Role      | Access          |
| -------------- | --------- | --------------- |
| Rahul Sharma   | CFO       | Full Access     |
| Anita Verma    | RCM       | Analytics Pages |
| Dr Kiran Reddy | Dept Head | Department Only |

---

## Dashboard Pages

### Executive Overview

* High-level revenue summary
* KPIs: Total Revenue, Leakage, Approval Rate

### Revenue Leakage Analysis

* Gap between expected vs actual revenue
* Leakage Index and Risk metrics

### Claim Denial Prediction

* Logistic Regression model
* ROC-AUC: 0.66

### Billing Anomaly Detection

* Z-score anomaly detection
* Flags abnormal claims

### Revenue Forecasting

* ARIMA model
* 6-month prediction

### Insurance Analytics

* Payer performance comparison
* Denial rates & revenue contribution

---

## Data Files

| File                         | Description        |
| ---------------------------- | ------------------ |
| modified_dataset.csv         | Raw claim data     |
| pre_processed_data.csv       | Cleaned data       |
| denial_model_predictions.csv | ML predictions     |
| monthly_revenue_history.csv  | Historical revenue |
| revenue_forecast.csv         | Forecast output    |

---

## Tech Stack

| Layer       | Technology          |
| ----------- | ------------------- |
| Frontend    | Streamlit           |
| Charts      | Plotly              |
| Data        | Pandas, NumPy       |
| ML Model    | Scikit-learn        |
| Forecasting | Statsmodels (ARIMA) |

---

## Key Business Insights

* ₹46.85 Cr revenue leakage detected
* 98.4% collection rate
* Government insurance has highest denial rate (26.7%)
* Self-pay has lowest denial rate

---

## Notes

* Runs fully offline (no APIs)
* Demo login system (CSV-based)
* Data is pre-processed (no real-time updates)

---

## Objective

To leverage machine learning and analytics for improving healthcare revenue efficiency.

---

## Outcome

* Reduced claim denial risk
* Improved revenue transparency
* Enabled data-driven decisions
