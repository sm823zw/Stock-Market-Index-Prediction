# Stock-Market-Index-Prediction

This repo deals with time series prediction using LSTMs. An encoder-decoder architecture was used for the purpose. A dual-stage attention mechanism (DA-RNN) has been used in addition to it. In the encoder, an input attention mechanism that can adaptively select the relevant driving series has been used. In the decoder, a temporal attention mechanism is used to automatically select relevant encoder hidden states across all time steps. For the objective, a square loss is used. With these two attention mechanisms, the DA-RNN can adaptively select the most relevant input features and capture the long-term temporal dependencies of a time series.

![image](https://user-images.githubusercontent.com/49569284/134814505-f78113d7-2d78-407c-976d-0d57b17b2206.png)

This architecture has been introduced in [this paper.](https://arxiv.org/abs/1704.02971)

The NASDAQ-100 dataset has been used for training the encoder-decoder model. In the NASDAQ 100 Stock dataset, the stock prices of 81 major corporations under NASDAQ 100 are used as the driving time series. The index value of the NASDAQ 100 is used as the target series. The frequency of the data collection is minute-by-minute. This data covers the period from July 26, 2016 to December 22, 2016, 105 days in total. Each day contains 390 data points from the opening to closing of the market except that there are 210 data points on November 25 and 180 data points on December 22. In our experiments, we use the first 35,100 data points as the training set and the following 2,730 data points as the validation set. The last 2,730 data points are used as the test set.

There have been various architectural changes made like introducing multi-head attention instead of just one head. Another change involves using scaled dot product attention. The project is on going.
