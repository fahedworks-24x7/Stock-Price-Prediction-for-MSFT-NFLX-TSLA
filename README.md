# A-Forecasting-Study-on-Stock-Prices
This paper analyzes different forecasting models on stock price datasets of Microsoft, Netflix, and Tesla. Stock price datasets
are highly nonlinear and nonstationary. Daily close prices of Microsoft Corporation ( MSFT), Tesla Inc. (TSLA) and Netflix
Inc (NFLX) from Yahoo Finance for the time period of 2011 to 2021 are collected. Datasets from 2011 to 2020 are used to build
the models and testing is done on the 2021 dataset.<br/>
We have used five traditional univariate forecasting models, one global
forecasting model and five deep learning models. We used five error metrics for evaluation: the Mean Absolute Scaled Error
(MASE), Symmetric Mean Absolute Percentage Error (sMAPE), Mean Absolute Error (MAE), Root Mean Squared Error
(RMSE) and Modified Symmetric Mean Absolute Percentage Error (msMAPE).<br/>
Cross-Validation is done for all forecasting models on the test set using rolling windows. We have also ensembled some
models by taking simple averages. This helps to check whether the ensembled model performed better than individuals for
these stock price datasets or not.<br/>
Here is the final [Report](https://github.com/Pratik-ahirrao/A-Forecasting-Study-on-Stock-Prices/blob/main/REPORT.pdf).

# Models Used:
We have used five traditional univariate forecasting models and one global forecasting model:<br/>
* Exponential Smoothing (ETS)
* Auto-Regressive Integrated Moving Average (ARIMA)
* Simple Exponential Smoothing (SES)
* Theta
* Trignometric Box-Cox ARMA Trend Seasonal (TBATS)
* Pooled Regression (PR)

We have also used five deep learning models:<br/>
* Simple Feed Forward Estimator (SFFE)
* DeepAR Estimator (DE)
* NBeats Estimator (NBE)
* WaveNet Estimator (WNE)
* Transformer Estimator (TE)

The five traditional univariate forecasting models and one global forecasting model are also applied to M3 Forecasting Dataset. Dataset can be obtained fron this [link](https://forecasters.org/resources/time-series-data/m3-competition/). 

## Parameters used in Models common to all datasets:
1. For SES, we have used auto-optimization (alpha value is not passed).
2. ETS model is applied with the seasonal_periods parameter as 7.
3. For Arima order chosen is (10,1,1) for (p,d,q). Here p is the number of lagged terms, d is the differencing factor, and q is
the no. of differentials of the lagged terms.
4. For Pooled Regression model, we used simple linear formula with lag terms to be considered as 3.
5. For Theta Model, we considered the period of 7.
6. For TBATS, Default parameters were considered.
7. Cross-validation is done on the test set using rolling windows. We have used sklearn TimeSeriesSplit() function with
the number of splits as 10.

## TEAM MEMBERS:
Pratik Ratnadeep Ahirrao (IMT2019064)<br/>
Pratyush Upadhyay (IMT2019066)<br/>
Rohan Thakkar (IMT2019071)<br/>
Fahed Shaikh (IMT2019079)<br/>
