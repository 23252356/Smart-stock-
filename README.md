# 📈 Stock Price Forecast App

Welcome to the **Stock Price Forecasting App**, an AI-powered web application that allows users to predict the future price trends of selected stocks using time series forecasting models and deep learning (LSTM). Built using Python and Gradio, this tool is user-friendly and ready for both casual and advanced users.

> 🚀 The app remains **online 24/7**, hosted on **Hugging Face Spaces**, so you can access it anytime — even if the code is not running locally!

---

## 🌐 Live Demo

- **Main App (via Hugging Face, 24/7):**  
  [https://huggingface.co/spaces/sarb-o-jit/stock-price-forecast](https://huggingface.co/spaces/sarb-o-jit/stock-price-forecast)

- **Temporary Session Link (Gradio):**  
  [https://5cde09f43750214444.gradio.live/](https://5cde09f43750214444.gradio.live/)

---

## 🔍 Features

- 🔎 **Stock Ticker Input:** Enter any valid stock ticker (e.g., AAPL, GOOG, TSLA)  
- 📊 **Visualization:** Historical stock price plots using Plotly  
- 🧠 **LSTM Forecasting Model:** Deep learning model trained for future price prediction  
- 🕒 **Custom Forecasting Period:** Choose the number of days to forecast into the future  
- 📉 **Normalized vs Actual Data Comparison:** Evaluate model performance visually  
- 🎛️ **Interactive UI:** Built with Gradio for smooth and intuitive user experience  
- 🌍 **Cloud Hosted:** Accessible 24/7 using Hugging Face Spaces

---

## 🛠️ Tech Stack

- **Python**  
- **Pandas, NumPy**  
- **Matplotlib, Plotly**  
- **Scikit-learn**  
- **TensorFlow / Keras (LSTM)**  
- **Gradio**  
- **Hugging Face Spaces**

---

## 📌 How to Use the App

1. Open the app using one of the provided links  
2. Enter the stock ticker (e.g., `AAPL`)  
3. Set the number of days for prediction  
4. Click the **Submit** button  
5. View:
   - Raw historical stock data
   - Model performance charts
   - Predicted vs Actual plots

---

## 🧑‍💻 Local Development (Optional)

To run locally:

```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
pip install -r requirements.txt
python app.py
