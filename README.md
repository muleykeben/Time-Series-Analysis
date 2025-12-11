# Time-Series-Analysis

## Project Overview

This repository contains the final project for the **İST 489 Time Series Analysis** course. The project involves analyzing a given time series, achieving stationarity, identifying an appropriate Seasonal Autoregressive Integrated Moving Average (SARIMA) model, and generating a forecast.

## Methodology

The analysis followed a systematic approach to model identification and selection:

### 1. Initial Analysis
* The initial time series plot, Autocorrelation Function (ACF), and Partial Autocorrelation Function (PACF) plots indicated the presence of both **trend** and **seasonality** in the series.

### 2. Achieving Stationarity
* **Trend Removal (Differencing):** A **first-order difference ($d=1$)** was applied to remove the trend.
* **Seasonality Removal (Seasonal Differencing):** The periodicity was determined to be **$s=9$**. A **first-order seasonal difference ($D=1$)** with period 9 was then applied.
* After both trend and seasonal differencing, the series was confirmed to be **stationary**.

### 3. Model Identification and Selection
* The ACF and PACF plots of the stationary series were examined. Since the **ACF was observed to decrease faster** than the PACF, the initial focus was on Moving Average (MA) models.
* Based on the non-seasonal lags, initial parameters were set as $p=1$ and $q=1$.
* Multiple SARIMA models were tested for the best fit.

## Results

### Selected Final Model

The model selected for forecasting is the one with the lowest Bayesian Information Criterion (BIC) value:

$$\text{SARIMA}(0,1,1)(0,1,1)_9$$

* **BIC Value:** 3.137
* **Model Significance:** The model was found to be statistically **significant**.
* **Residual Analysis:** The residual series was confirmed to be **White Noise**  because all lags in its ACF plot were within the confidence limits.

### Forecasting
The selected model was used to generate 5 forecast values along with their confidence intervals.

## Software Used

The time series analysis, modeling, and forecasting were performed using **SPSS** software.
