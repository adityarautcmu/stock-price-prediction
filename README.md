# Estimating the Volatility of Returns

The provided data set contains prices of $6$ stocks named $a-f$, sampled over the course of one year
at $1$-minute intervals. Our goal in this exercise is to estimate the volatility of these stocks over the month
following given data, in the metric of “annualized percent returns”. 

## Data processing alternatives
There are a multitude of choices to be made on how the data is processed, e.g.
- cleaning noisy data, simplifying highly fluctuating prices (e.g. front-filling missing stock prices)
- the metrics chosen for returns calculation (e.g. holding period or logarithmic returns)
- sub-sampling or aggregating with a different frequency for training (e.g. daily/hourly prices, moving averages)
- addition of statistical or time series features
- choice of model and validation criteria

## Features considered 
1. Square of past returns
2. Absolute value of past returns
3. Range of past return values ($\max-\min$)
4. Past values of volatility (lag)
5. Daily range of prices
6. Realized daily power (sum of absolute returns)

Multiple combinations of these features were considered for cross-sectional linear regression models, finding the best set of predictors for each stock. 

## Training parameters
Linear regressor with 20-fold cross validation. Details mentioned in the Jupyter notebook and methodology, results summarized in the report PDF. 



