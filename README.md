# Q18 Machine Learning on a Rolling Basis

This trading strategy is designed for the [Quantiacs](https://quantiacs.com/contest) platform, which hosts competitions
for trading algorithms. Detailed information about the competitions is available on
the [official Quantiacs website](https://quantiacs.com/contest).

## How to Run the Strategy

### In an Online Environment

The strategy can be executed in an online environment using Jupiter or JupiterLab on
the [Quantiacs personal dashboard](https://quantiacs.com/personalpage/homepage). To do this, clone the template in your
personal account.

### In a Local Environment

To run the strategy locally, you need to install the [Quantiacs Toolbox](https://github.com/quantiacs/toolbox).

## Strategy Overview
This strategy leverages supervised learning, specifically Bayesian Ridge Regression, to predict the rise or fall of stock prices in the NASDAQ-100 index. The strategy is divided into two main parts:

1. **Global Training**:
   - Utilizes all available time series data for training.
   - Disregards the sequential nature of data, leading to potential forward-looking bias.

2. **Rolling Training and Prediction**:
   - Implements a rolling window approach for training and prediction, ensuring no forward-looking bias.
   - Employs a specialized Quantiacs backtester to optimize performance.

#### Features for Learning:
- The strategy incorporates various technical indicators such as MACD, RSI, stochastic oscillators, and volatility measures to capture market trends and patterns.
