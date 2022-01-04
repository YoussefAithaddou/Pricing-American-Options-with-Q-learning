# Pricing-American-Options-with-Q-learning
This project aims to price auto-callable options using least squares policy iteration (LSPI) and fitted Q-iteration (FQI) as opposed to the usual least squares Monte Carlo (LSM) approach.

* Used 1 year of Apple Inc. (AAPL) stock data from Yahoo finance (https://finance.yahoo.com/quote/AAPL).
* Produced 20000 Monte Carlo simulation paths using Black_Scholes and Heston models.
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
* Model information using torchinfo:

![image 1](https://github.com/YoussefAithaddou/CNN-to-predict-locations-of-my-previous-trips/blob/main/model%20info.PNG)

###### Model layers:
* 2x CNNs
* 2x Pooling layers
* 3x Linear neurons
###### Hyper parameters:
* Batch size: 16
* Epochs: 3
# Model Evaluation:
* Accuracy on training set is 98.28 %
* Accuracy on testing set is 93.50 %
# Sample visualization:
* I used a batch of test data (4 images from each location) to asses how the model predict the location of each frame:

![image 2](https://github.com/YoussefAithaddou/CNN-to-predict-locations-of-my-previous-trips/blob/main/result%20sample.png)

* This model achieved a high accuracy rate with a small training sets due to the fact that all pictures are relatively similar to each other (frames of the same video). In this particular sample, the model manages to accurately identify each location the frames belong to. That is, on average we can accurately identify pictures at a ratio of 14.96 frames in each batch of 16.
