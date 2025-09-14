# 📈 Mutual Fund NAV Forecasting using Cloud Data Pipeline

[![Streamlit](https://img.shields.io/badge/UI-Streamlit-red)](https://streamlit.io/)  
[![Azure](https://img.shields.io/badge/Cloud-Azure-blue)](https://azure.microsoft.com/)  
[![Python](https://img.shields.io/badge/Language-Python-green)](https://www.python.org/)  

This project is an **interactive web application** built with **Streamlit** to forecast the **Net Asset Value (NAV)** of mutual funds using multiple **time-series** and **machine learning algorithms**.  

It integrates with an **Azure SQL Database**, retrieves mutual fund data dynamically, and provides **visual analytics + forecasting**.  
A complete **data pipeline** is developed using **Azure Data Factory, Databricks, SQL DB, and Apache Airflow** for automated ingestion, transformation, and forecasting.  
Insights are visualized through **Power BI dashboards**.  

---

## 🎯 Features

- 🔎 Search and select mutual funds from a predefined list (`scheme_codes.json`)  
- 📊 View **historical NAV trends** with interactive Plotly charts  
- 🏦 Access **fund metadata** such as fund house, category, returns (1Y/3Y/5Y), CRISIL rating, expense ratio, and manager  
- 🔗 Explore **similar funds** and external resources  
- 📈 Forecast future NAV values (1–30 days) using multiple forecasting algorithms  

---

## 🔧 Forecasting Models Implemented

### 1. **Linear Regression (Baseline Model)**
- Models NAV trend as a linear function of time.  
- Provides a **benchmark prediction**.  
- ✅ Pros: Simple, fast, interpretable  
- ❌ Cons: Cannot capture seasonality or non-linearity  

---

### 2. **ARIMA (Auto-Regressive Integrated Moving Average)**
- Statistical time-series model defined by `(p, d, q)`.  
- Example: **ARIMA(2,1,2)** used here.  
- ✅ Pros: Captures trend + short-term dependencies  
- ❌ Cons: Needs careful tuning, assumes stationarity  

---

### 3. **Exponential Smoothing (Holt-Winters)**
- Assigns **exponentially decreasing weights** to past observations.  
- Handles **trend + seasonality**.  
- ✅ Pros: Great for seasonal NAV data  
- ❌ Cons: Struggles with sudden market shocks  

---

### 4. **LSTM Neural Network (Deep Learning)**
- A **Recurrent Neural Network (RNN)** for sequential data.  
- Learns long-term dependencies in NAV series.  
- ✅ Pros: Captures non-linear + complex patterns  
- ❌ Cons: Requires large datasets, high computation  

---

## 🖥️ Application Interface

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
- **Data Pipeline:**  
  - Apache Airflow → Automated API ingestion  
  - Azure Data Factory → ETL orchestration  
  - Azure Databricks → Feature engineering + transformation  
- **Models:**  
  - Scikit-learn (Linear Regression)  
  - Statsmodels (ARIMA, Exponential Smoothing)  
  - TensorFlow/Keras (LSTM)  
- **Visualization:** Plotly, Matplotlib, Power BI  

---

## ⚙️ Installation & Setup

Clone this repository:

```bash
git clone https://github.com/your-username/mutual-fund-nav-forecasting.git
cd mutual-fund-nav-forecasting

├── main.py                 # Streamlit app entry point
├── scheme_codes.json       # Mutual fund scheme codes and names
├── README.md               # Project documentation
├── Project Interface-1.png # UI screenshots
├── Project Interface-2.png
├── Project Interface-3.png
├── Project Interface-4.png
└── /videos                 # Demo & walkthrough videos


# 📊 Key Outcomes & Future Improvements  

## ✅ Key Outcomes  

- **Automated Data Pipeline**  
  - Built end-to-end NAV ingestion pipeline using **Apache Airflow + Azure Data Factory + Databricks**.  
  - Data ingestion from APIs is fully automated → **no manual updates required**.  

- **Cloud Integration**  
  - Implemented **Azure SQL Database** for scalable storage and retrieval.  
  - Seamless integration with **Streamlit app** for real-time data visualization.  

- **Forecasting Models**  
  - Implemented **Linear Regression, ARIMA, Exponential Smoothing, and LSTM** models.  
  - Compared models using **MAE, RMSE, and MAPE** for performance benchmarking.  
  - LSTM captured **complex non-linear NAV patterns**, while ARIMA provided strong **short-term forecasts**.  

- **Visualization & Insights**  
  - Developed **interactive dashboards** using **Streamlit + Plotly**.  
  - Built **Power BI dashboards** for business reporting.  
  - Provided fund-specific insights: historical NAV, metadata (returns, CRISIL ratings, expense ratio), and fund manager details.  

- **Business Value**  
  - Improved **NAV forecasting accuracy** → helps investors/fund managers in decision-making.  
  - Delivered **scalable, cloud-ready solution** adaptable for financial institutions.  

---

## 🚀 Future Improvements  

- **Deployment & Scalability**  
  - Deploy application on **Azure App Service** or **Docker + Kubernetes** for production use.  
  - Enable **CI/CD pipelines** for automated testing and deployment.  

- **Advanced Models**  
  - Integrate **Facebook Prophet** for trend + seasonality forecasting.  
  - Explore **XGBoost/LightGBM** for hybrid ML approaches.  
  - Train on **longer historical NAV datasets** to improve accuracy.  

- **Real-Time Processing**  
  - Enable **real-time NAV streaming** using **Kafka or Azure Event Hubs**.  
  - Integrate with **Azure Synapse Analytics** for large-scale query performance.  

- **Enhanced User Experience**  
  - Add **search filters & fund comparisons** in the Streamlit app.  
  - Enable **downloadable reports (PDF/Excel)** for investors.  
  - Expand coverage to **all Indian mutual funds across categories**.  

- **Explainability & Monitoring**  
  - Implement **SHAP/Explainable AI** for model interpretability.  
  - Add **monitoring dashboards** to track model drift and retrain automatically.  

---

📌 This roadmap ensures the solution is **scalable, production-ready, and investor-friendly** while continuously improving forecast accuracy and usability.  


