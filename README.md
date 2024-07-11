# Time Series Analysis and Forecasting of Stock Prices

## Project Overview

The aim of this project is to analyse and forecast the closing price time series for a given stock using different time series models. We attempt to implement a robust forecasting model that can predict future stock prices accurately.

## Tools and Libraries Used

- **Programming Languages:** Python
- **Libraries:** pandas, yfinance, matplotlib, statsmodels, scikit-learn

## Project Structure

- `data/`: Directory containing the raw and processed data files.
- `notebooks/`: Jupyter notebooks with the code and analysis.
- `src/`: Python scripts for data processing, model training, and evaluation.
- `README.md`: Project overview and instructions.

## Steps and Methodology

### 1. Data Collection and Preprocessing

- **Objective:** Fetch historical stock price data.
- **Tools:** `yfinance`, `pandas`
- **Code:**
  ```python
  import yfinance as yf
  import pandas as pd

  # Fetch historical data
  stock_data = yf.download('AAPL', start='2010-01-01', end='2023-01-01')
  # Keep only the closing prices
  stock_data = stock_data[['Close']]
  stock_data.to_csv('data/AAPL.csv')
