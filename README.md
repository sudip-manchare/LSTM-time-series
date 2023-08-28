# LSTM-time-series
## Reliance Stock Price Prediction with LSTM

This project demonstrates time-series data analysis by predicting stock prices using LSTM (Long Short-Term Memory) layers in a neural network. LSTM is a recurrent neural network (RNN) capable of learning sequence patterns and making predictions accordingly.

## Problem Statement

Given a historical stock price series, we aim to predict the stock prices for the next few days using a sliding window approach. For instance:

Given historical stock prices for 7 days:

given_series = `[1, 2, 3, 4, 5, 6, 7]`

We want to predict the stock prices for the next 3 days:

output_expected = `[8, 9, 10]`


We use a sliding window concept with a window size of 3 to train our model:

- For input `[1, 2, 3]`, the output is `[4]`
- For input `[2, 3, 4]`, the output is `[5]`
- For input `[3, 4, 5]`, the output is `[6]`
- For input `[4, 5, 6]`, the output is `[7]`

Once we have a prediction for `[5, 6, 7]`, say `o1`, we use this prediction as a part of the input for the next predictions:

- For input `[5, 6, 7]`, the output is `o1`
- For input `[6, 7, o1]`, the output is `o2`
- For input `[7, o1, o2]`, the output is `o3`

We then compare these predicted values `[o1, o2, o3]` to the actual values `[8, 9, 10]` to assess the performance of our model.


