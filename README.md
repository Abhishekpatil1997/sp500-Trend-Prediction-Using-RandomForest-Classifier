# Project: SP500 Trend Prediction using Random-Forest Classifier

## Overview

This project involved developing a machine learning model to predict the daily up or down trend of the S&P 500 stock index. The goal was to forecast whether the next trading day's closing price would be higher or lower than the current day's closing price.

Please refer to the [project report](sp500_Trend_Prediction_Project_Report(Final).pdf) for full details on the data, modeling approach, results and analysis.

## Data

- Historical daily open, high, low, close prices for S&P 500 index obtained from Yahoo Finance 
- Data from 1990 - present
- Target variable engineered to indicate up/down trend compared to previous day

## Modeling

- Random forest classifier selected as ML algorithm
- Rolling expanding window backtesting methodology used
  - Model repeatedly trained on growing time window, validated on next unseen year 
- Parameters tuned to balance overfitting vs accuracy
  - `n_estimators` and `min_samples_split` optimized through experiments
- Rigorous train/test split evaluation

## Results

- Initial model achieved 52.8% precision on backtest 
- Model improved by adding engineered features and tuning parameters
  - Additional price averages, ratios and trends added
  - `n_estimators` increased to 200, `min_samples_split` to 50
- Enhanced model achieved 56.2% precision, improving accuracy by 3.4%
- Outperformed baseline predictor
- Prediction threshold tuning improved precision further

## Conclusion

This project demonstrated an end-to-end machine learning workflow for a time series forecasting problem, from data collection and cleaning to model development, parameter tuning and rigorous backtesting. 

The enhanced random forest model successfully improved accuracy over the baseline by 3.4% through feature engineering and hyperparameter optimization. It provides a solid foundation, with opportunities to further improve to production monitoring, decaying outdated data, and alternative data sources.

