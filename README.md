# 📈 Mutual Fund NAV Forecasting using Cloud Data Pipeline

This project is an **interactive web application** built with **Streamlit** to forecast the **Net Asset Value (NAV)** of mutual funds using multiple **time-series** and **machine learning algorithms**.  
It integrates with an **Azure SQL Database**, retrieves mutual fund data dynamically, and provides **visual analytics + forecasting**.
Built end-to-end NAV forecasting pipeline using Azure services and time-series ML models.Automated data ingestion from APIs using Python and Apache Airflow. Developed ETL workflows in Azure
Data Factory and Databricks.Delivered predictions and insights through Power BI dashboards.

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

## 🖥️ App Interface

Here are some screenshots of the working application:
### 🔍 Fund Selection & NAV Trend  

<img width="1907" height="832" alt="Project Interface-1" src="https://github.com/user-attachments/assets/45db1975-4ebc-46d6-961d-2f841c6ff519" />

### 📊 Fund Metadata & Similar Funds 

<img width="1912" height="817" alt="Project Interface-2" src="https://github.com/user-attachments/assets/6cff7993-be21-4848-8780-45bee2a12095" />

### 📈 Forecasting with ARIMA  

<img width="1902" height="817" alt="Project interface-3" src="https://github.com/user-attachments/assets/7e103039-b684-4cd2-915e-4ac9378b8530" />

### 📉 Forecasting with Exponential Smoothing  

<img width="1878" height="832" alt="Project interface-4" src="https://github.com/user-attachments/assets/fa7a1bba-792a-4abf-b2f4-d7d8ed2f7820" />


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
 Google Drive link - https://drive.google.com/drive/folders/1nxX3hH59f3mEMsrFdXE4nyrPqTmehDT3
## 📂 Repository Structure
├── main.py # Streamlit app entry point
├── scheme_codes.json # Mutual fund scheme codes and names
├── README.md # Project documentation
├── Project Interface-1.png
├── Project Interface-2.png
├── Project Interface-3.png
├── Project Interface-4.png
└── /videos # Demo & walkthrough videos


