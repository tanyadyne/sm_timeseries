# Stock Price Forecasting using ARIMA models
To view the main project, please click [here](https://nbviewer.jupyter.org/github/tanyadyne/sm_timeseries/blob/main/Stock_Market_TS_Analysis.ipynb).

## Situation
Whilst I've had experience using time series analysis in an economic setting, I was curious about whether stock prices could be forecasted using time series models such as the ARIMA (autoregressive integrated moving average). Because of the recent global chip/gpu shortage, I chose to analyse two semiconductor stocks: NVDA and AMD.

## Task
To begin the project, I would have to first retrieve data on the stock prices. Once I preprocessed the data, I then need to perform exploratory data analysis to get a general idea of what I'm working with. Next I would need to build the ARIMA model (which entails the use of diagnostic tests and the need to choose the parameters of the model). After that, I can use my specified model to forecast both in-sample and out-of-sample forecasts.

## Action
To create my dataframe of stock prices, I use pandas and the yahoo-finance library. For this use-case, I decided on a time-frame of 4 years from January 2017 to present. I then


## Result

