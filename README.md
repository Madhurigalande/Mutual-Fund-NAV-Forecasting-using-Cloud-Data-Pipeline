# 📈 Mutual Fund NAV Forecasting – Streamlit App

This project is an **interactive web application** built with **Streamlit** to forecast the **Net Asset Value (NAV)** of mutual funds using multiple **time-series** and **machine learning algorithms**.  
It integrates with an **Azure SQL Database**, retrieves mutual fund data dynamically, and provides **visual analytics + forecasting**.

---

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
Project Interface-1.png

### 📊 Fund Metadata & Similar Funds  
Project Interface-2.png

### 📈 Forecasting with ARIMA  
Project interface-3.png

### 📉 Forecasting with Exponential Smoothing  
Project interface-4.png

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
├── Project Interface-1.png
├── Project Interface-2.png
├── Project Interface-3.png
├── Project Interface-4.png
└── /videos # Demo & walkthrough videos
