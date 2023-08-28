# LSTM-time-series
Reliance stock price prediction using LSTM layered neural network
This is my attempt to learn time-series data analysis by predicting stock prices using LSTM layers in a neural network.
LSTM stands for long-short-term memory and is a type of recurrent neural network(RNN) capable of learning sequence patterns and predicting accordingly.
Example:
given_series = [1, 2, 3, 4, 5, 6, 7] for 7 days of a week
output_expected = [8, 9, 10] for 3 days following the above week
sliding window concept is used. Let us say window size is 3
model is trained using the following method:
if
for input = [1, 2, 3] , output = [4]
for input = [2, 3, 4] , output = [5]
for input = [3, 4, 5] , output = [6]
for input = [4, 5, 6] , output = [7]
for input = [4, 5, 6] , output = [7]
then 
for input = [5, 6, 7] , output = ?
Let us say we get as o1
for next 2,
for input = [6, 7, o1] , output = o2
for input = [7, o1, o2], output = o3
Then I have compared analogous equivalents of [8, 9, 10] vs [o1, o2, o3] in the notebook.
