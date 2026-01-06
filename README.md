# Time Series Analysis on DJIA 30 – IBM

## Project Overview

This project analyzes and predicts IBM stock prices using time series models. The goal is to evaluate deep learning algorithms (LSTM, GRU, RNN) for forecasting stock prices from historical data. The study highlights challenges and limitations of relying solely on historical data and emphasizes the need to incorporate external factors (e.g., news sentiment, correlated assets) for improved forecasts.

## Key Components

### Data Collection and Preprocessing
- **Data source:** Kaggle dataset containing IBM stock prices (Jan 2006 – Dec 2018, 3,020 rows).
- **Preprocessing steps:**
  - Removed rows with missing values.
  - Dropped redundant columns (e.g., `Name`).
  - Engineered features: Moving Averages (MA-10, MA-50), Relative Strength Index (RSI), Bollinger Bands, Volume moving averages, Daily returns.

### Seasonal Decomposition
- Performed seasonal decomposition to analyze trend, seasonality, and residuals.
- Identified significant market events (e.g., 2008 financial crisis) that materially impacted price dynamics.

### Model Training and Evaluation
- **Models tested:** LSTM, GRU, RNN.
- **Evaluation metrics:** RMSE, MAE, MAPE.
- **Training parameters:**
  - Optimizer: Adam (lr = 0.001)
  - Loss: Mean Squared Error (MSE)
  - Batch size: 32
  - Epochs: 50 (with early stopping, patience=10)

- **Results (test set):**
  - LSTM — MAE: $2.21 (MAPE: 1.4%)
  - GRU  — MAE: $1.49 (MAPE: 0.97%) — best performer
  - RNN  — MAE: $2.83 (MAPE: 1.79%) — weakest performer

## Key Findings
- GRU outperformed LSTM and RNN in both accuracy and generalization on the test set.
- Models struggle to predict abrupt market regime changes or reversals when trained solely on historical price-based features.
- Integrating external signals (news sentiment, macro indicators, correlated securities) is necessary to improve prediction of abrupt moves.

## Conclusion
The project demonstrates deep learning models’ strengths and limitations for financial time series forecasting. While GRU provided the best results among the tested architectures, historical data alone is insufficient for robust stock-price prediction. This work is a foundation for future research that enriches datasets with external market influences.

## References
- Dataset: Kaggle (IBM historical prices)
- Implementation: TensorFlow / Keras

---

*Note:* the same approach and analysis were applied to another file/project as well.
