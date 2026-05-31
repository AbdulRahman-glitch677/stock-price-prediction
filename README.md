# Stock Price Prediction Using LSTM Deep Learning

## Project Overview

This project focuses on predicting stock closing prices using a Long Short-Term Memory (LSTM) neural network. Historical stock market data was analyzed and processed to build a deep learning model capable of learning temporal patterns and forecasting future stock prices.

The project demonstrates the application of time-series analysis, technical indicators, and deep learning techniques in financial forecasting.

---

## Dataset

Dataset Used:

Price Volume Data for All US Stocks & ETFs

Source:

https://www.kaggle.com/datasets/borismarjanovic/price-volume-data-for-all-us-stocks-etfs

Selected Stock:

```text
SOHU (sohu.us.txt)
```

Dataset Size:

```text
3201 rows × 7 columns
```

Features:

* Date
* Open
* High
* Low
* Close
* Volume
* OpenInt

Sample Data:

| Date       | Open  | High  | Low   | Close | Volume  |
| ---------- | ----- | ----- | ----- | ----- | ------- |
| 2005-02-25 | 16.46 | 16.89 | 16.46 | 16.83 | 874643  |
| 2005-02-28 | 16.75 | 18.30 | 16.75 | 17.92 | 3676074 |
| 2005-03-01 | 17.87 | 19.23 | 17.86 | 18.80 | 3574093 |

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-Learn
* TensorFlow
* Keras
* Kaggle Notebook

---

## Project Workflow

### 1. Data Collection

Historical stock price data was loaded from the Kaggle dataset.

### 2. Technical Indicators

The following indicators were calculated:

#### Moving Average (MA20)

20-Day Moving Average used for short-term trend analysis.

#### Moving Average (MA50)

50-Day Moving Average used for long-term trend analysis.

#### Relative Strength Index (RSI)

RSI was calculated to identify overbought and oversold market conditions.

---

## Data Preprocessing

The following preprocessing steps were performed:

* Date conversion
* Sorting by date
* Missing value removal
* Feature scaling using MinMaxScaler
* Time-series sequence generation

Sequence Length:

```text
60 previous trading days
```

Generated Dataset Shape:

```text
X Shape: (3092, 60, 1)
y Shape: (3092,)
```

---

## LSTM Model Architecture

Model Summary:

| Layer           | Output Shape | Parameters |
| --------------- | ------------ | ---------: |
| LSTM (50 Units) | (None, 50)   |     10,400 |
| Dense (1 Unit)  | (None, 1)    |         51 |

Total Parameters:

```text
10,451
```

Trainable Parameters:

```text
10,451
```

---

## Train-Test Split

Training Data:

```text
80%
```

Testing Data:

```text
20%
```

---

## Model Performance

Evaluation Metric:

### Root Mean Squared Error (RMSE)

```text
RMSE = 1.913
```

Interpretation:

The model's predicted stock prices differ from the actual stock prices by approximately 1.91 units on average, indicating good predictive performance for the selected stock.

---

## Visualization

The following visualizations were generated:

* Historical Stock Price Trend
* Actual vs Predicted Stock Prices
* Moving Average Analysis

---

## Key Findings

* LSTM successfully captured temporal dependencies in stock price data.
* Moving averages helped identify market trends.
* RSI provided additional market momentum information.
* The model achieved a low prediction error with an RMSE of 1.913.

---

## Limitations

* Stock prices are influenced by external factors such as news, market sentiment, and economic events.
* Historical price data alone cannot guarantee future performance.
* Prediction accuracy may vary across different stocks and market conditions.

---

## Future Improvements

Possible enhancements include:

* Using multiple features (Open, High, Low, Volume)
* Implementing GRU networks
* Hyperparameter tuning
* Using Attention-based models
* Integrating financial news sentiment analysis

---

## Kaggle Notebook

Complete implementation available on Kaggle:

https://www.kaggle.com/code/sabdulrahman/stock-price-prediction

---

## Repository Structure

```text
stock-price-prediction/
│
├── README.md

```

---

## Conclusion

An LSTM-based stock price prediction model was developed using historical stock market data. Technical indicators such as Moving Averages and RSI were incorporated to analyze market behavior. After preprocessing and sequence generation, the model was trained to predict future closing prices.

The model achieved an RMSE of 1.913, demonstrating its ability to capture underlying trends in stock price movements. This project highlights the effectiveness of deep learning techniques for time-series forecasting in financial markets.

---

## Author

Syed Abdul Rahman

Bachelor of Engineering (Artificial Intelligence & Machine Learning)
