Project Title
Time Series Analysis on DJIA 30 – IBM

Date
11 April 2025

Project Overview
This project focuses on analyzing and predicting IBM stock prices using time series models. The goal is to evaluate the effectiveness of deep learning algorithms—LSTM, GRU, and RNN—in forecasting stock prices based on historical data. The study highlights the challenges and limitations of relying solely on historical data for stock price prediction and emphasizes the need for incorporating external factors for more accurate forecasts.

Key Components
1. Data Collection and Preprocessing
Data Source: Kaggle dataset containing IBM stock prices from January 2006 to December 2018 (3,020 rows).

Preprocessing:

Removed rows with missing values.

Dropped redundant columns (e.g., "Name").

Engineered new features:

Moving Averages (MA-10, MA-50).

Relative Strength Index (RSI).

Bollinger Bands.

Volume Moving Averages and Daily Returns.

2. Seasonal Decomposition
Analyzed trends, seasonality, and residuals in IBM stock prices.

Identified significant events (e.g., the 2008 financial crisis) impacting stock prices.

3. Model Training and Evaluation
Models:

LSTM: Achieved test MAE of $2.21 (MAPE: 1.4%).

GRU: Best performer with test MAE of $1.49 (MAPE: 0.97%).

RNN: Least effective, with test MAE of $2.83 (MAPE: 1.79%).

Evaluation Metrics: RMSE, MAE, and MAPE.

Training Parameters:

Optimizer: Adam (learning rate = 0.001).

Loss Function: Mean Squared Error (MSE).

Batch Size: 32.

Epochs: 50 (early stopping with patience=10).

4. Key Findings
GRU outperformed LSTM and RNN in accuracy and generalization.

Limitations: Models struggled to predict abrupt market changes (e.g., reversals) without external data (e.g., news sentiment, correlated stocks).

Insight: Historical data alone is insufficient for reliable stock price prediction; integrating external factors is crucial.

Conclusion
The project demonstrated the capabilities and limitations of deep learning models in time series forecasting for financial data. While GRU showed promising results, the study underscores the importance of enriching datasets with external market influences to improve predictive accuracy. This work serves as a foundation for future research in financial time series analysis.

References
Dataset sourced from Kaggle.

Models implemented using TensorFlow/Keras.

For detailed code and visualizations, refer to the attached Python scripts and figures in the report.