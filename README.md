# Time-Series
#### Time-Series Forecasting

In this notebook, we will load historical Dollar-Yen exchange rate futures data and apply time series analysis and modeling to determine whether there is any predictable behavior.

Follow the steps outlined in the time-series starter notebook to complete the following:

1. Decomposition using a Hodrick-Prescott Filter (Decompose the Settle price into trend and noise).
2. Forecasting Returns using an ARMA Model.
3. Forecasting the Settle Price using an ARIMA Model.
4. Forecasting Volatility with GARCH.

Use the results of the time series analysis and modeling to answer the following questions:

1. Based on your time series analysis, would you buy the yen now?
2. Is the risk of the yen expected to increase or decrease?
3. Based on the model evaluation, would you feel confident in using these models for trading?

#### Linear Regression Forecasting -Second Notebook using scikit-Learn

In this notebook, we will build a Scikit-Learn linear regression model to predict Yen futures ("settle") returns with *lagged* Yen futures returns and categorical calendar seasonal effects (e.g., day-of-week or week-of-year seasonal effects).

Follow the steps outlined in the regression_analysis starter notebook to complete the following:

1. Data Preparation (Creating Returns and Lagged Returns and splitting the data into training and testing data)
2. Fitting a Linear Regression Model.
3. Making predictions using the testing data.
4. Out-of-sample performance.
5. In-sample performance.

Use the results of the linear regression analysis and modeling to answer the following question:

* Does this model perform better or worse on out-of-sample data compared to in-sample data?

## Report Summary

In this assignment, we were tasked to test the many time-series tools that we have learned in order to predict future movements in the value of the Japanese yen versus the U.S. dollar. To do taht, I used Time Series analysis and regression methods. From the time series standpoint analysis, I utilized ARMA and ARIMA models to forecast the return price for Japannese Yen and the GARCH method to visualize the currency volatility. The first two models, ARMA and ARIMA have p-values over 0.05, which makes the model not significant. The 5 day forecast reveals an up trend on the Japannese Yen return, while predicting the volatility to increase as well.

Key Points of Time Series Analysis

The volatility for yen is supposed to increase. And when there is high volatility, there is increase of risk as well. Risk averse investor should not buy Yen right now. Risk is expected to increase. The Arma model wasnt significant because p-value exceedd 0.05. But overall, I would feel confident using these models for trading, as they give me predictions of future trends based on past returns.

In addition, we computed a regression Analysis with the SKLearn linear regression model to predict Yen futures ("settle") returns with lagged Yen futures returns and plotted the predicted returns vs the real/true values. In addition, we computed in sample and out of sample performance metrics. We can see that the model shows a root mean square error of 0.396% on out-of-sample data and 0.5657% on in-sample data. Usually, there is no correct value of MSE. However, the lowest its value the better, as it shows that the data are dispersed closely to the mean.

Key Points Regression Analysis

We can see that the model shows a root mean square error of 0.396% on out-of-sample data and 0.5657% on in-sample data. Usually, there is no correct value of MSE. However, the lowest its value the better, as it shows that the data are dispersed closely to the mean.

Also, in sample error is the one obtained using the same dataset of the model. Because of the over-fitting , out of sample rate is the one we usually care about, as we used new data set to get the error rate.
