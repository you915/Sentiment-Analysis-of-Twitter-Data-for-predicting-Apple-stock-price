# Project 2 - Group # 4

## Sentiment Analysis of Twitter Data for predicting movement in stock price.

![Twitter Sentiment](Images/twitter-stock-market.jpg)

*Source: https://devpost.com/software/tweetpredict*

### Project Description:

This project is about analyzing social media data about Apple Inc. and predicting its future stock trend with sentiment classification.
We applied sentiment analysis and machine learning principles to discover the correlation between " public sentiment " and " market sentiment ". 

Prediction of stock price is an extremely  complex and  very  challenging task  because there are  too  many  factors  involved  such  as  economic circumstances,  political  events,  and  other  environmental factors which may impact the stock price. Due to these factors, it is difficult to find out the dependence of future on past price.

The popularity  and importance  of numerous social  media platforms has risen  to new levels over the past few years,  as more people  spend time online. One such social media platform that has seen an explosive rise in popularity is Twitter. Twitter is a rich source of real-time  information  regarding  current  societal  trends  and opinions. 

Some [statistics](
    https://blog.hootsuite.com/twitter-statistics/) regarding Twitter:

* Twitter has 145 million monetizable daily active users.

* 30 million (or 20%) of Twitter’s daily users are American.

* 92% of the U.S. population is familiar with Twitter (even if they don’t use it).

* According to a recent survey by [Pew Research Center](https://www.pewresearch.org/fact-tank/2019/08/02/10-facts-about-americans-and-twitter/), around one-in-five U.S. adults (22%) say they use Twitter.

* Twitter stands out as one of the social media sites with the most news-focused users.

Behavioural economics tell us that people are  not rational consumers and individual behaviours and decisions are greatly affected by emotions and indeed  by the opinions of others. Twitter  sentiment  analysis  can  be  extremely  helpful  for predicting  emotions  or  opinion  on a certain  stock.  So examining  the trending mood on Twitter  and observing its relationship to the movement in stock price can help predict the future trend in the market.

### Data Preprocessing

1. Twitter data from [Kaggle](https://www.kaggle.com/)  for Apple stock was used for sentiment analysis. The time frame chosen to analyze data is `January 01, 2016` to `August 31, 2019`.   
    
2. We collected daily Apple stock data for the same time period from [Yahoo Finance](https://finance.yahoo.com/quote/AAPL/history?p=AAPL) for historical data analysis and stock trend prediction.

3. Twitter information was processed to use only data for the dates the stock market was open.

### Model training and evaluation

Different machine learning techniques were used to train and evaluate models to analyze and determine the correlation between twitter sentiment and Apple stock price. 

Two approaches for analyses were used:

1. **Classification:** In this approach the twitter polarity scores were used to classify tweets into positive, negative and neutral. The adjusted closing prices of Apple stock were converted to a binary form (0 and 1), where 0 means that the value of the company stock price is less that the day before, and 1 means that the value is greater than the day before. This provided a trend for stock price movement. 

    Algorithms used for analysis:

    **Random Forest Classifier**

    Random Forest Classifier is an ensemble method, meaning that a random forest model is made up of a large number of small decision trees, called estimators, which each produce their own predictions. The random forest model combines the predictions of the estimators to produce a more accurate prediction.

    **Gradient Boosting Classifier**

    Gradient Booster algorithm builds trees one at a time, where each new tree helps to correct errors made by previously trained tree. With each tree added, the model becomes even more expressive. There are typically three parameters - number of trees, depth of trees and learning rate, and the each tree built is generally shallow.

2. **Regression:** In this approach the twitter polarity scores, twitter volume and the adjusted closing prices were used to predict the future movement in Apple stock price. The adjusted closing prices data was stuctured such that previous time steps were used as input variables and the next time step as the output variable.

    Algorithms used for analysis:

    **Random Forest Regressor**

    Random Forest Regression is a supervised learning algorithm that uses ensemble learning method for regression. Ensemble learning method is a technique that combines predictions from multiple machine learning algorithms to make a more accurate prediction than a single model.


    **LSTM RNN**

    Long short-term memory (LSTM) is an artificial recurrent neural network (RNN) architecture used in the field of deep learning. LSTM networks are well-suited for making predictions based on time series data, since there can be lags of unknown duration between important events in a time series.

    **XGBoost Regressor**

    XGBoost is short for Extreme Gradient Boosting and is an efficient implementation of the gradient boosting machine learning algorithm.

### Conclusion/Predictions

### Limitations

1. Twitter API has limitations on the amount of data that can be accessed. Therefore, a document with Twitter information regarding Apple stock from Kaggle was used.

2. NewsAPI headlines besides Twitter could also have been used for sentiment analysis.




### References:

https://arxiv.org/pdf/1610.09225.pdf

https://www.researchgate.net/publication/315562673_Twitter_Data_Predicting_Stock_Price_Using_Data_Mining_Techniques

https://blog.hootsuite.com/twitter-statistics/

