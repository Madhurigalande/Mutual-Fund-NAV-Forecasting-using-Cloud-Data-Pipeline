

# 📈 Mutual Fund NAV Forecasting – Streamlit App

This project is an **interactive web application** built with **Streamlit** to forecast the **Net Asset Value (NAV)** of mutual funds using multiple **time-series** and **machine learning algorithms**.  
It integrates with an **Azure SQL Database**, retrieves mutual fund data dynamically, and provides **visual analytics + forecasting**.

---Built end-to-end NAV forecasting pipeline using Azure services and time-series ML models Automated data ingestion from APIs using Python and Apache Airflow Developed ETL workflows in Azure Data Factory and
Databricks Delivered predictions and insights through Power BI dashboards.

## 🎯 Project Overview

The app allows users to:  
- 🔎 Search and select mutual funds from a predefined list (via `scheme_codes.json`)  
- 📊 View **historical NAV trends** with interactive Plotly charts  
- 🏦 Access **fund metadata** such as fund house, category, returns (1Y/3Y/5Y), CRISIL rating, expense ratio, and manager  
- 🔗 Explore similar funds and external detailed links  
- 📈 Forecast future NAV values (1–30 days) using various algorithms  

---

## 🔧 Forecasting Models Implemented

1. **Linear Regression** – Trend-based simple prediction  
2. **ARIMA (2,1,2)** – Rolling time-series forecasting  
3. **Exponential Smoothing** – Captures level & trend of NAV data  
4. **LSTM Neural Network** – Deep learning model for sequential NAV forecasting  

---

## 🖥️ App Features

- **Interactive Dashboard:**  
  - Fund selection dropdown  
  - Line chart of NAV over time  
  - Metrics for fund details (fund house, manager, returns, CRISIL rating, etc.)  
  - Similar fund navigation buttons  

- **Forecasting Section:**  
  - Select forecast horizon (1–30 days)  
  - Choose prediction algorithm  
  - Compare historical vs forecasted NAVs in interactive charts  

- **Visualization:**  
  - Built with **Plotly Express** (dark theme)  
  - Side-by-side comparison of history vs forecast  

---

## 🛠️ Tech Stack

- **Frontend/UI:** Streamlit, Plotly  
- **Database:** Azure SQL Database (PyODBC)  
- **Data Processing:** Python, Pandas, NumPy  
- **Models:**  
  - Scikit-learn (Linear Regression)  
  - Statsmodels (ARIMA, Exponential Smoothing)  
  - TensorFlow/Keras (LSTM)  
- **Other Tools:** JSON for scheme mapping, Matplotlib for support  

---

## 📂 Repository Structure
├── main.py # Streamlit app entry point
├── scheme_codes.json # Mutual fund scheme codes and names
├── README.md # Project documentation
└── /videos # Demo & walkthrough videos


