# LSTM Stock Prediction for AAPL

This project demonstrates how to use a Long Short-Term Memory (LSTM) neural network to predict future stock prices, specifically for Apple Inc. (AAPL), based on historical data. LSTMs are powerful for time series data, as they capture temporal dependencies essential for predicting stock trends.

## Overview

This project builds and trains an LSTM model to predict future prices based on the last 60 days of AAPL stock data. The dataset is sourced from Yahoo Finance via the `pandas_datareader` library, and the model is created using Keras in TensorFlow.

## Dataset

The dataset consists of daily historical closing prices of AAPL from 2018 to 2023, fetched directly from Yahoo Finance. The closing price data is scaled between 0 and 1 for efficient LSTM training. 


