# Time_Series_forcasting_AR

Navigating the Future: A Quick Guide to Time Series Forecasting Theories

Predicting the future is often shrouded in mysticism, but when it comes to data with a temporal order, we can utilize powerful statistical tools called time series forecasting theories. These theories help us make informed guesses about what might happen next in a sequence, whether it's stock prices, weather patterns, or sales figures. Let's delve into some key concepts:

White Noise: Imagine a rainstorm where drops fall randomly, with no discernible pattern. White noise mimics this randomness in data. It has no predictable trends or relationships between past and future values. White noise forecasting is challenging as it's like throwing darts at a blank wall—pure guesswork!

ARMA & ARIMA: These acronyms stand for Autoregressive Moving Average (ARMA) and Autoregressive Integrated Moving Average (ARIMA). They're like detectives, analyzing past values to predict future behavior. ARMA models combine the influence of past errors (moving average) with the impact of past observations (autoregression). ARIMA takes things a step further by "differencing" the data, making it stationary (more on that later). These models are workhorses for many forecasting tasks.

Vector Autoregression (VAR): Imagine multiple time series dancing in synchrony. VAR models capture these intricate relationships. They consider the lagged effect of one series on another, allowing you to forecast, say, electricity demand based on both temperature and economic activity.

Seasonality: Like clockwork, some data exhibits predictable ups and downs within a cycle, like monthly sales figures. Seasonality models incorporate these recurring patterns into the forecasting process, leading to more accurate predictions, especially for short-term horizons.

Autoregression: Remember how ARMA uses past observations? This is autoregression in action. It analyzes how much past values "regress" (influence) future values. For example, knowing yesterday's temperature might help predict tomorrow's.

Partial Autoregression: Sometimes, only a few past values hold significant predictive power for the future. Partial autoregression identifies these "lag terms" with the most impact, focusing the model on the truly relevant historical data.

Stationarity: Imagine a seesaw constantly tilting left or right. Such non-stationary data poses challenges for forecasting. ARIMA models, for example, require stationarity—where the data's mean and variance remain stable over time. Stationarity models like differencing help achieve this before forecasting.

These are just some of the many time series forecasting theories out there. Choosing the right one depends on the nature of your data, the forecasting horizon, and the complexities you need to capture. By understanding these concepts, you can navigate the often-murky waters of the future with greater confidence, leveraging the power of data to make informed decisions in a world that's constantly changing.

 Here is a draft GitHub repository description for this time series forecasting auto-regression project:

# Daily Minimum Temperature Forecasting

This project performs time series forecasting to predict future daily minimum temperatures based on past temperature data. 

## Data
The daily minimum temperature data is loaded from a CSV file containing a date index and temperature column.

## Method
An autoregressive model is trained on the temperature data to forecast future values. The model regresses on 10 lagged values of the series. 

Key steps:
- Test for stationarity
- Plot ACF and PACF
- Train autoregressive model
- Make dynamic and future predictions

## Results
The model is used to forecast temperatures for 9 days. The RMSE between the predicted and actual values is calculated.

The future predicted temperatures for next 9 days are also output.

## Usage
The main script loads the data, trains the model, evaluates performance and outputs forecasts. 

The trained model can be reused to predict on new input data.

## Improvements
- Try different lag values
- Compare AR to other models (RNN, LSTM etc)
- Ensemble models
- Add external predictor variables  

