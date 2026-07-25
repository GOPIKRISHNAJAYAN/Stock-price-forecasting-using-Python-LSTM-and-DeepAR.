# 📈 Stock Price Forecasting using LSTM and DeepAR

A comparative deep learning and probabilistic forecasting study on **Cipla Ltd. (CIPLA.NS)** using historical stock market data from Yahoo Finance.

---

## 📖 Overview

This project forecasts the short-term stock price of **Cipla Ltd.** using two advanced time-series forecasting models:

- **Stacked Long Short-Term Memory (LSTM)**
- **DeepAR (Deep AutoRegressive Model)**

The objective is to compare the performance of both models in predicting the next **7 trading days** and evaluate their forecasting accuracy using standard performance metrics.

---

## 🎯 Objectives

- Forecast future stock prices using Stacked LSTM.
- Forecast future daily log returns using DeepAR.
- Compare the forecasting performance of both models.
- Evaluate prediction accuracy using RMSE, MAE, MAPE, and R².

---

## 📊 Dataset

- **Source:** Yahoo Finance
- **Company:** Cipla Ltd. (CIPLA.NS)
- **Period:** January 2018 – June 2026
- **Total Trading Days:** 2,096

---

## 🛠️ Technologies Used

- Python
- Google Colab
- TensorFlow / Keras
- PyTorch
- GluonTS
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- yFinance

---

## 🧠 Models Used

### 1. Stacked LSTM

- Lookback Window: 120 Days
- LSTM Layers: 2
- Hidden Units: 50
- Dropout: 0.20
- Optimizer: Adam
- Learning Rate: 0.0005
- Epochs: 20

### Performance

| Metric | Value |
|--------|-------|
| RMSE | 36.94 |
| MAE | 28.33 |
| MAPE | 2.00% |
| R² | 0.8650 |

---

### 2. DeepAR

- Framework: PyTorch (GluonTS)
- Context Length: 120 Days
- Prediction Length: 7 Days
- Hidden Size: 50
- Recurrent Layers: 2
- Dropout: 0.20
- Learning Rate: 0.001
- Distribution: Student-T
- Epochs: 100

### Performance

| Metric | Value |
|--------|-------|
| RMSE | 0.0225 |
| MAE | 0.0156 |
| MAPE | 1.98% |
| R² | -0.568 |

> **Note:** DeepAR predicts daily log returns, so its metrics are not directly comparable with LSTM's price-scale metrics.

---

## 📅 7-Day Forecast

| Date | LSTM (₹) | DeepAR (₹) |
|------|---------:|-----------:|
| 26-Jun-2026 | 1399.12 | 1446.78 |
| 29-Jun-2026 | 1403.99 | 1428.72 |
| 30-Jun-2026 | 1407.83 | 1427.80 |
| 01-Jul-2026 | 1410.94 | 1419.04 |
| 02-Jul-2026 | 1413.56 | 1445.08 |
| 03-Jul-2026 | 1415.83 | 1441.08 |
| 06-Jul-2026 | 1417.86 | 1451.46 |

---

## 📂 Repository Structure

```
Stock-Price-Forecasting-LSTM-DeepAR/
│
├── Stock_Price_Forecasting.ipynb
├── Cipla_Stock_Forecasting_Report.docx
├── Cipla_Forecasting.pptx
├── README.md
└── Images/
```

---

## 📈 Key Findings

- Both models successfully forecasted the next 7 trading days.
- LSTM demonstrated strong historical prediction accuracy with an **R² of 0.8650**.
- DeepAR provided probabilistic forecasts by predicting daily log returns.
- Both models indicated a relatively stable to slightly increasing short-term trend for Cipla Ltd.

---

## 🚀 Future Improvements

- Integrate technical indicators such as RSI, MACD, and Moving Averages.
- Include trading volume and financial news sentiment.
- Compare with GRU and Transformer-based forecasting models.
- Deploy the model as a web application using Streamlit or Flask.

---

## 👨‍💻 Author

**Gopikrishna Jayan**

M.Sc. Statistics

Interested in Data Analytics, Machine Learning, Time Series Forecasting, and Financial Data Analysis.

---

## ⭐ If you found this project useful, please consider giving it a Star!
