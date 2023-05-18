

# Stock Market Prediction using Numerical and Textual Analysis

## Objective
Our goal is to create a hybrid model for stock price/performance prediction using both numerical analysis of historical stock prices and sentimental analysis of news headlines. By combining these two sources of information, we aim to improve the accuracy of our predictions.

## Approach
- We start by extracting sentiment scores from newspaper headlines data using the `SentimentIntensityAnalyzer` from the `nltk` library. This allows us to quantify the overall sentiment expressed in the news on a given day.
- Next, we use a Multivariate Time Series Forecasting approach inspired by [this paper](https://www.sciencedirect.com/science/article/pii/S2405452620302476). We utilize Keras' LSTM (Long Short-Term Memory) to model the temporal effects of past events (both textual sentiment scores and historical stock data) on opening prices. LSTM is a type of recurrent neural network that is well-suited for modeling time series data.
- Our model achieved a training loss of 0.0472 and a validation loss of 0.0256, indicating that it was able to accurately predict stock prices on both the training and validation datasets. Additionally, our model achieved an RMSE (root mean squared error) of 475.102 on the test data, providing further evidence of its predictive power.

## Data
We used the following data sources for our analysis and prediction:
- Historical stock prices for SENSEX (S&P BSE SENSEX) from [Yahoo Finance](https://finance.yahoo.com/). This data provides us with information on past stock prices and performance.
- Textual news data from [Times of India](https://bit.ly/36fFPI6). This data provides us with information on news events that may impact stock prices.
- Data can found here [data](https://drive.google.com/drive/folders/1_LX8eJG9Zq_1p0VxA5eVFoAweSEJm7Ks?usp=share_link)

## References
- [Deep learning for stock prediction using numerical and textual information](https://www.sciencedirect.com/science/article/pii/S2405452620302476) by Ryo Akita, Akira Yoshihara, Takashi Matsubara, Kuniaki Uehara. This paper provided the inspiration for our approach and methodology.

