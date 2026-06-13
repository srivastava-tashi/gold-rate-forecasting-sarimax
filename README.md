# Gold Rate Forecasting in INR

Forecasted future gold prices with macroeconomic indicators to understand how the factors influence the gold prices. 
Achieving a MAPE of 17.69%.

## Overview
This project forecasts the future gold prices in India using historical gold data along with **NIFTY50, USD/INR exchange rate,
Inflation rate and Repo rate** as exogenous variables.

The forecasting model is built using the SARIMAX(Seasonal AutoRegressive Integrated Moving Average with Exogenous Variables) algorithm,
which captures both time series patterns and influence of external variables.

## Problem Statement
Gold prices are influenced by various economic and market factors. Accurate forecasting of gold rates can help investors, traders
or financial analysts make informed decisions.

## Dataset
Historical data of Gold Price, USD/INR exchange rate and NIFTY50 (Indian stock market index) was collected using 
Yahoo Finance API (yfinance) and for Inflation and Repo rates: [RBI Database](https://data.rbi.org.in/DBIE/#/dbie/home)

NOTE: Each gold price represents 100 troy ounces of gold.

### Data Period:
 • April 2019 - April 2026

## Project Workflow
### 1. Data Collection

 Downloaded the historical data 

### 2. Data Preprocessing

 • Date indexing

 • Handling missing values

 • Data Transformation

 • Feature selection

### 3. Exploratory Data Analysis

 • Distribution Analysis

 • Trend Analysis

 • Correlation Analysis

 • Time Series Decomposition

### 4. Stationarity Testing

  Applied Augmented Dickey-fuller (ADF) Test to verify stationarity.

### 5. Feature Engineering

 • Log Transformation

 • Differencing

 • Creation of exogenous variables

### 6. Model Building

 Implemented a SARIMAX model with:

 Order = (2,0,1)

 Seasonal Order = (2,1,1,7)

### 7. Evaluation

#### Performance Metrics and Results
Root Mean Squared Error: 78080.45

Mean Absolute Error: 58524.94

Mean Absolute Percentage Error(MAPE): 17.69%

### 8. Future Forecasting

 Forecasted the gold prices for next 60 days using predicted exogenous variables.

## Tools and Technologies 
 • Python

 • Yahoo Finance API
 
 • Numpy

 • Pandas

 • Matplotlib
 
 • Seaborn

 • Statsmodel

 • Scikit-learn

 • Jupyter Notebook

## Visualizations
  ### Gold Price Trend
 ![Alt Text](images/gold_rateoveryears.png)

### Correlation Heatmap
 ![Alt Text](images/correlation.png)

### STL Decomposition Before and After Transformation
 ![Alt Text](images/stl_before.png)
 ![Alt Text](images/stl_after.png)

### Actual vs Predicted data
 ![Alt Text](images/predicted.png)

### Future Gold Price Forecast
 ![Alt Text](images/gold_forecast.png)

## Future Improvements
 • Augmenting additional economic indicators
 
 • Build real time forecasting dashboard


