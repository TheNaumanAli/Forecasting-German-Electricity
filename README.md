# German Electricity Demand Forecasting (2015–2020)

## Project Overview

This project focuses on forecasting German electricity demand using historical time-series data from 2015 to 2020. The aim of this study is to compare different forecasting approaches and identify the most effective model for predicting future electricity consumption.

I developed and evaluated multiple forecasting models, including statistical forecasting methods, machine learning algorithms, and deep learning approaches.

The models implemented in this project are:

- Benchmark models:
  - Mean Forecast
  - Naive Forecast
  - Seasonal Naive Forecast
  - Drift Forecast

- Statistical models:
  - SARIMA (Seasonal Autoregressive Integrated Moving Average)
  - SARIMAX with temperature as an external variable

- Machine Learning models:
  - Random Forest Regression
  - Gradient Boosting Regression

- Deep Learning model:
  - LSTM (Long Short-Term Memory Neural Network)


## Dataset

The electricity demand data was obtained from:

Open Power System Data (OPSD)
https://data.open-power-system-data.org/time_series/

The dataset contains hourly electricity demand data for European countries. This project focuses specifically on Germany (`DE`).

The data processing steps included:

- Selecting German electricity demand values
- Filtering data from January 2015 to October 2020
- Handling missing values
- Resampling hourly data into daily and weekly observations


## Project Workflow

The project follows a complete time-series forecasting pipeline:

1. Data collection and preprocessing
2. Exploratory Data Analysis (EDA)
3. Stationarity testing using:
   - Augmented Dickey-Fuller (ADF)
   - KPSS test
4. Seasonal analysis using ACF and PACF plots
5. Benchmark forecasting models
6. SARIMA modelling and forecasting
7. SARIMAX forecasting with temperature features
8. Feature engineering and machine learning forecasting
9. Hourly electricity forecasting using LSTM
10. Model comparison and evaluation


## External Variables

To improve forecasting accuracy, temperature data from Berlin was collected using:

Open-Meteo Historical Weather API

Temperature was included as an exogenous variable in the SARIMAX model and as a feature in machine learning models.


## Evaluation Metrics

The models were evaluated using:

- RMSE (Root Mean Squared Error)
- MAE (Mean Absolute Error)
- MAPE (Mean Absolute Percentage Error)


## Results Summary

The experiments showed that advanced models improved forecasting accuracy compared with traditional benchmark approaches.

Key observations:

- Seasonal Naive provided a strong baseline due to yearly electricity demand patterns.
- SARIMA successfully captured seasonal behaviour.
- SARIMAX demonstrated the effect of temperature on electricity consumption.
- Random Forest improved weekly forecasting by learning nonlinear relationships.
- LSTM achieved the best accuracy by modelling high-frequency hourly patterns.


## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Statsmodels
- Pmdarima
- Scikit-learn
- TensorFlow / Keras


## Repository Structure
