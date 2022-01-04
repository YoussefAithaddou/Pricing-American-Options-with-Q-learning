# Pricing-American-Options-with-Q-learning
This project aims to price auto-callable options using least squares policy iteration (LSPI) and fitted Q-iteration (FQI) as opposed to the usual least squares Monte Carlo (LSM) approach.

* Used 1 year of Apple Inc. (AAPL) stock data from Yahoo finance.
* Produced 20000 Monte Carlo simulation paths using Black-Scholes and Heston models.
* Coded least squares policy iteration, fitted Q-iteration and least squares Monte Carlo algorithms with Numpy and Scipy libraries.
* Backtested the three strategies in pricing an Autocallable option.
* Calculated Price, Delta and Profit and Loss of each method.

# Resources Used
* Python Version: 3.7
* Packages and Libraries: pandas, numpy, matplotlib, scipy, seaborn, matplotlib, prettytable.
# Data used
* More than 1 year (2020-01-02 to 2021-05-17) of Apple Inc. (AAPL) stock data from Yahoo finance (https://finance.yahoo.com/quote/AAPL).
* Used only the daily adjusted closing price.

# Monte Carlo Simulation:

* Monte-Carlo grid with Brownian motion (Black-Scholes model) and a stochastic volatility (Heston Model):
* For the rest of the project, we use Heston Model as it emphasizes on the randomness of the volatility.

![image 1](https://github.com/YoussefAithaddou/Pricing-American-Options-with-Q-learning/blob/main/Monte_carlo%20grids.png)

# Autocallable note:

* We consider the expiry of the payoff to be 1 year, with 4 quarterly observations.
* (T1 = 3 Month, T2 =6 Month,T3 = 9 Month and T4 := T = 1 Year). 
* At each Ti if the observed stock price is above the barrier 120% x S0 the holder pays c and the structure continue.
* Otherwise the the holder receives the stock performance Sti/S0.
* Finally at last expiry T if the structure is still alive, the holder unconditionally receives the performance ST/S0.
# BackTest:
### Option Prices:
* LSPI and FQI descover better strategies to execute the option, thus we except a higher return and therefore a higher option prices than LSM.

![image 2](https://github.com/YoussefAithaddou/Pricing-American-Options-with-Q-learning/blob/main/Option_prices.png)

* Epochs: 3
# Model Evaluation:
* Accuracy on training set is 98.28 %
* Accuracy on testing set is 93.50 %
# Sample visualization:
* I used a batch of test data (4 images from each location) to asses how the model predict the location of each frame:

![image 2](https://github.com/YoussefAithaddou/CNN-to-predict-locations-of-my-previous-trips/blob/main/result%20sample.png)

* This model achieved a high accuracy rate with a small training sets due to the fact that all pictures are relatively similar to each other (frames of the same video). In this particular sample, the model manages to accurately identify each location the frames belong to. That is, on average we can accurately identify pictures at a ratio of 14.96 frames in each batch of 16.
