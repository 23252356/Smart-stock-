# Stock Forecasting and Machine Learning Analysis

This project performs a comprehensive analysis and prediction of Apple Inc. (AAPL) stock data using various data science and machine learning techniques. The project includes data collection, feature engineering, multiple machine learning models, deep learning (LSTM), visualization, and an interactive forecast application using Gradio.

---

## Overview

The goal is to predict future stock prices using historical stock data. The project includes:

1. Collecting 5 years of historical stock data from Yahoo Finance using `yfinance`.
2. Cleaning and preprocessing the dataset.
3. Performing exploratory data analysis and visualization.
4. Engineering new features such as daily percentage change and lag features.
5. Building and evaluating multiple machine learning models:
   - Linear Regression
   - Decision Tree
   - Random Forest
   - Support Vector Regressor (SVR)
   - Long Short-Term Memory (LSTM) neural network
6. Building a stock prediction web application using Gradio.

---

## Key Components

### 1. Data Collection

- Utilizes the `yfinance` library to download historical stock data for Apple Inc. (ticker: AAPL).
- Date range is from April 1, 2020 to April 1, 2025.
- Data is saved locally as `AAPL_5Y_data.csv`.

### 2. Data Preprocessing

- Removes invalid or non-numeric values in `Close` and `Volume`.
- Converts data types properly.
- Calculates:
  - Daily percentage change in closing price.
  - Daily percentage change in volume.
- Adds a next-day `Close_Next` column as the prediction target.

### 3. Data Visualization

- Plots include:
  - Closing price over time.
  - Trading volume over time.
  - Daily percentage changes in price and volume.
- Visualizations are built using `matplotlib` and `seaborn`.

### 4. Feature Engineering

- Constructs lag features.
- Simulates sentiment scores between -1 and 1 to demonstrate their potential impact.
- Includes current and previous day's sentiment in the feature set.

---

## Machine Learning Models

### Linear Regression

- Uses basic financial features and lag features.
- Trains and evaluates on time-split data.
- Evaluation metrics: Mean Squared Error (MSE) and R-squared (R²).

### Random Forest Regressor

- Captures non-linear relationships.
- Trained with the same features including sentiment.
- Evaluation with MSE and R².

### Decision Tree Regressor

- Rule-based model to model splits in stock behavior.
- Suitable for interpretability.

### Support Vector Regressor (SVR)

- Margin-based model.
- Suitable for datasets with noise.

---

## Deep Learning Model: LSTM

### Architecture

- Two-layer LSTM neural network using `Keras` and `TensorFlow`.
- Inputs are sequences of past time steps.
- Output is the next day’s predicted closing price.

### Training

- Data is normalized using `MinMaxScaler`.
- Sequence of 60 time steps (days) is used for each input sample.
- Training and test split is 80/20.

### Output

- Predicts future stock prices.
- Visualizations compare actual vs. predicted prices.
- Includes loss curves and residual error analysis.

---

## Evaluation Metrics

- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- R-squared Score (R²)
- Residual analysis plots

---

## Interactive Forecasting App (Gradio)

A simple interface built using `Gradio` allows the user to input a stock ticker (e.g., "AAPL") and receive a 7-day forecast based on linear regression.

### How it works:

- Downloads the past 180 days of stock data.
- Trains a linear regression model on the closing prices.
- Forecasts the next 7 days.
- Generates a forecast plot showing historical and predicted data.

### Running the App:

To run the app locally:

```bash
https://8ee71895c89eaba170.gradio.live/
