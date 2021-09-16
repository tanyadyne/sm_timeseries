# Stock Price Forecasting using ARIMA models
To view the main project, please click [here](https://nbviewer.jupyter.org/github/tanyadyne/sm_timeseries/blob/main/Stock_Market_TS_Analysis.ipynb).

## Situation
Whilst I've had experience using time series analysis in an economic setting, I was curious about whether stock prices could be forecasted using time series models such as the ARIMA (autoregressive integrated moving average). Because of the recent global chip/gpu shortage, I chose to analyse two semiconductor stocks: NVDA and AMD.

## Task
To begin the project, I would have to first retrieve data on the stock prices. Once I preprocessed the data, I then need to perform exploratory data analysis to get a general idea of what I'm working with. Next I would need to build the ARIMA model (which entails the use of diagnostic tests and the need to choose the parameters of the model). After that, I can use my specified model to forecast both in-sample and out-of-sample forecasts.

## Action
To create my dataframe of stock prices, I use pandas and the yahoo-finance library. (And for this use-case, I decided on a time-frame of 4 years from January 2017 to the present). I then run some basic exploratory analysis (including visualisation in matplotlib) and I test the skewness and kurtosis of the returns to characterise the risk involved with the respective stocks. I also find that the returns from AMD and NVDA have a correlation coefficient of about 0.63 (i.e. moderately positive correlation) which is to be expected (given they are both semiconductor stocks). Before building the ARIMA models, I carry out the augmented dickey fuller (ADF) test to ensure stationarity in the variables. To build the ARIMA models, I use scipy and statsmodels. This involved choosing the number of AR terms and MA terms for each model (using the Partial Autocorrelation (PACF) plot and Autocorrelation (ACF) plot, respectively). I then fit the model to my data and perform both in-sample and out-of-sample forecasting.

## Result
Whilst this project taught me a lot about ARIMA modelling and how to implement it in python, the results clearly show that stock price prediction using ARIMA models is not a feasible method. Why? The answer simply lies in its definition. The ARIMA model is essentially based on the idea that information hidden in past values of a time series can *alone* predict future values; so we can see how such a definition could not be compatible with the stock market (a highly volatile environment with plenty of factors affecting future prices). Not to mention, many (including Nobel prize winner Eugene Fama) have argued that stock price movements are simply impossible to predict in the short-term. In the future, I hope to explore this area of stock price prediction further by potentially looking into Support Vector Machines and Neural Networks. I also believe that it would prove more beneficial for me to focus more on predicting trend direction rather than short-term price movement.


