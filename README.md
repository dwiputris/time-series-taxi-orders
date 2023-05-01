# time-series-taxi-orders

Number of taxi orders made in an airport of a big city might show both seasonality and trend.
A taxi company wishes to build a time series model that will help it to attract more taxi drivers and anticipate demands during peak hours. 
Linear regression is used to build the model for the time series.
Special algorithm for time series ARIMA is also used.
And because of the seasonality, SARIMA is alo used.
Lastly, one of the most popular libraries Prophet is also used.

Data analysis is done by plotting the data.
Further more, ACF and PACF plot are done to observe for stationarity and autocorrelation.
Seasonal decompose helps to attend to the presence of trend and seasonality.
In addition to that, adfuller test measures the probability of the stationarity.

The data analysis found that the time series has daily seasonality.
It also has a upward trend, with more noticeable pick up points around the end of the data points.
Lastly, because of the non-stationarity of the data, the time series is best differenced by 1 and 24 lag to achieve state of stationarity.

After data analysis, feature engineering is done to establish independent features of the basic regression model.

This project found that SARIMA with non-seasonal order: (0,1,2), seasonal_order:(0,1,2,24) is the most stable model.
It has got the loswet AIC and BIC scores, and quality of residues showing enough normal distribution and almost no autocorrelation.

However, Prophet also shows similar robust performance, with error score of RMSE just slightly above the SARIMA model.
The fact that it is easy to tune and well interpretable is an advantage.

The ARIMA model is able to past the maximal error score required by the taxi company (RMSE 48).
Yet it fails to cover for the presence of the seasonality.

The Linear Regression is able to make a good generalization of the time series.
The feature engineering that corresponds with the characteristics of the data helps increase the model performance.
However it is not enough to catch the peaking points in time where the number of orders increases abruptly.

In conlusion Prophet and SARIMA offers the best model for the taxi order time series.
