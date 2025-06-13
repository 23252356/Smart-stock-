

# Stock Market Forecasting Using Sentiment Analysis and Trading Volume Trends

 Project Overview

This project focuses on forecasting stock prices using historical stock market data, trading volume trends, and integrating sentiment analysis. It implements various machine learning models (Linear Regression, Decision Tree, Random Forest, Support Vector Regressor, LSTM) to predict stock prices based on historical patterns. Additionally, it provides an interactive Gradio web interface that allows users to input a stock ticker symbol (e.g., AAPL, GOOGL) and get a 7-day stock price forecast along with a visualization.

---

Features

*  Fetches real-time historical stock data from Yahoo Finance
*  Implements multiple regression models:

  * Linear Regression
  * Decision Tree
  * Random Forest
  * Support Vector Regressor (SVR)
  * LSTM (Long Short-Term Memory)
*  Computes performance metrics:

  * MAE (Mean Absolute Error)
  * MSE (Mean Squared Error)
  * RMSE (Root Mean Squared Error)
* Generates separate performance plots and residual visualizations for each model
*  Gradio-based UI for user input and instant forecast:

  * Accepts stock ticker
  * Displays historical vs. predicted trends
*  Data preprocessing: handles missing values, date parsing, feature normalization
*  Forecast output includes a line chart showing future trend
*  Easily extendable for sentiment analysis using social media/news APIs

---

 Models and Results Summary

| Model                    | MAE    | MSE      | RMSE   |
| ------------------------ | ------ | -------- | ------ |
| Linear Regression        | 0.93   | 1.61     | 1.27   |
| Decision Tree            | 25.48  | 900.18   | 30.00  |
| Random Forest            | 25.95  | 934.57   | 30.57  |
| Support Vector Regressor | 57.30  | 4402.05  | 66.35  |
| LSTM                     | 186.14 | 35167.86 | 187.53 |

>  Observation: Linear regression gives the most stable and interpretable results for short-term trends, while LSTM shows poor performance on limited data without tuning.

---

 Requirements

Install dependencies with:

```bash
pip install -r requirements.txt
```

requirements.txt:

```
pandas
numpy
scikit-learn
matplotlib
seaborn
yfinance
gradio
tensorflow
```

---

 How to Run

1. Clone the repository or copy the Python script.
2. Run the following command to launch the Gradio interface:

```bash
python app.py
```

3. Enter a stock ticker (e.g., `AAPL`, `MSFT`, `TSLA`) into the input box.
4. View the historical trend and 7-day forecast generated using linear regression.

---

 Example Forecast

* Input: `AAPL`
* Output: A line chart showing the past 180 days of Apple stock prices and a 7-day future prediction.

---

 Future Enhancements

* Integrate sentiment analysis using news APIs (e.g., NewsAPI, Twitter API)
* Extend forecast duration with more robust deep learning models (LSTM + attention)
* Add user option to choose model (e.g., dropdown in UI)
* Export forecast results as CSV
* Use Reinforcement Learning for trading strategy simulation

---

 Data Sources

* [Yahoo Finance](https://finance.yahoo.com/)
* [Apple AAPL Kaggle Dataset](https://www.kaggle.com/datasets/tarunpaparaju/apple-aapl-historical-stock-data)

---

 Author & Contributions

This project was developed as part of a machine learning and finance research initiative. Contributions and feedback are welcome!

---
