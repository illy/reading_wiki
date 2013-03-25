We collected Twitter feeds for 5 months obtaining a large set of emotional retweets originating from within the US, from which six public opinion time series containing the keywords “dollar%t ”, “$%t ”, “gold%t ”, “oil%t ”, “ job%t ” and “economy%t ” were extracted.

Except “$%t ”, all other five public opinion time series are identified by a Granger-causal relationship with certain market movements.

It is demonstrated that daily changes in the volume of economic topic retweeting seem to match the value shift occurring in the corresponding market next day.

Gayo-Avello et al. [1] clearly pointed out that following what people are blogging about or what they are searching about can give us some intuition on the collective psyche and lead us to understand what is currently happening in society before it is actually happening.

Furthermore, stock-related tweets with a specific hashtag “$” were collected and studied in detail in [13], where it was found that these tweets contain valuable information that is not fully incorporated in current market indicators.

In previous work [14], we also presented very preliminary results that the number of emotional tweets, which contain words such as “hope”, “fear” or “worry” correlated with stock market indicators.

We collected a large set of tweets submitted to Twitter in the period from November 15, 2010 to April 20, 2011.

In order to get a better picture of the opinion and emotional state of the US investors, we only filter for emotional retweets that come from the United States.

1. Retweets only.

2. Containing the emotion words “hope”, “fear” or “worry”.

3. Originating from the US.

It is generally believed that the more a topic is being picked up and retweeted by others, the more it is relevant and widely recognized.

When people are pessimistic or uncertain about their future, they will be more cautious to invest and trade.

For the purpose of better capturing the opinion and emotional state of the US population, we intentionally limit the targeted tweets to the ones originating from within the continental United States without Alaska.

Tweets were collected within four 2000-kilometers circles with centers in Pittsburg, Atlanta, Las Vegas and Boise respectively. As Figure 1 shows, these circles cover the contiguous United States and parts of Canada and Mexico.

Over the duration of five months, 3,809,437 retweets posted by approximately 961,000 users were collected and each tweet has a unique identifier, time of submission and the textual content.

As we can see, the daily retweet rate of each emotion word is highly variable, for example, the hope-retweets range from 6453 to 34805 per day.

Even more interestingly, the number of hope-retweets is much higher than the fear or worry ones, almost six times on average, which might suggest that people prefer using optimistic words when they express their feelings, even when they are worrying or in fear.

As twitter users can share only short textual messages with no more than 140 characters per post, there is always only one topic in one tweet.

Thus the main theme of the whole tweet can usually be subsumed by one or two keywords.

As the total number of retweets varies highly from day to day, a normalized number was chosen as a measurement of public opinion on day t.

To meet the requirement of stationarity in time series analysis, data are processed in the following way. Taking DJIA as an example, the stock movement at a day t is defined as the normalized change in stock close price from the past day, which can be expressed as Dt = DJIAt ! DJIAt!1 DJIAt!1 , (1) where DJIAt is the close price of day t. Similarly, we determine the other independent variables. Using these new relative variables, we not only can tell the change direction of the market which is indicated by the sign of the number, but also measure how much it changed compared to the previous day

In Table 2, we observe a relatively strong correlation between stock market return and “dollar%t!1 ” (r = 0.308**, 0.203 and 0.259*, p-value = 0.004, 0.058 and 0.015).

not only “oil%t!1 ” but also “economy%t!1 ” is strongly correlated with oil price changes of day t (r = 0.295** and 0.214*, p-value = 0.006 and 0.046).

we found that the correlation between “gold%t!1 ” and Gt is weak, but “gold%t!1 ” is significantly correlated with Ut (r = 0.213*, p-value = 0.016), indicating a relationship between the gold price and the strength of the US dollar.

It is worth noticing that all the correlation coefficients mentioned above are positive, which implies that an increase in economic topic retweeting seems to indicate an increase in the value of the corresponding asset on the next market day.

the relationships between market movement and time series “$% ” and “ job% ” are not that significant in this period.

the Twitter buzz of two or three days before seems to have less influence on the market movement of day t

Granger causality is a statistical concept of causality that is based on prediction. According to Granger causality, if a signal X “Granger-causes” (or “G-causes”) a signal Y, then past values of X should contain information that helps predict Y above and beyond the information contained in past values of Y alone.

Its mathematical formulation is based on linear regression modeling of stochastic processes (Granger 1969).

It is noteworthy that in spite of its name, Granger causality is not sufficient to imply true causality.

If both X and Y are driven by a common third process with different lags, X might erroneously be believed to “Granger-cause” Y. However, in our project, we are not testing the actual causation but simply whether one variable provides predictive information about the other one or not.

Granger causality requires that the time series have to be covariance stationary, so an Augmented Dickey-Fuller test has been done first, in which the null hypothesis H0 of non-stationarity was rejected at the 0.05 confidence level.

“dollar%t ” has the highest Granger causality relation with stock market return, especially with the DJIA return (p-value < 0.01 when n=1 and remains significant when n=2 and 3).

the “oil%t ” time series “Granger-causes” the changes in oil price (p-value is always less than 0.05 when lag varies from 1 to 3 days).

The other two predictive variables are “ gold%t ” and “ job%t ”, which have Granger causality relation with Ut and Gt separately

However, the most interesting aspect is that the “ gold%t ” time series failed in explaining the price change in the gold market, but could help predict the currency exchange rates (USD/CHF).

Our results statistically show that public opinion measured from large-scale collection of emotional retweets is correlated to and even predictive of the financial market movement.

Second, the analyzing methods we used in this paper, both the correlation and Granger causality analysis, are based on the assumption that the relation between variables is linear, which is hardly satisfied for financial market movement.

###Summary

Following their previous work (2010), Zhang, Fuehres, & Gloor's (2011) focus is much broader, not only the stock price, but also the gold price, crude oil price and currency exchange. Similar to Bollen, mao & Zeng (2011), they also use Granger-casual analysis to evaluate the relationship between twitter and market, but their also apply the correlation test to investigate. They only consider retweets from the continental United States with the keywords 'hope', 'fear' or 'worry' in a period from November, 2010 to April 2011, and the normilised data shows that the tweets containing 'hope' is far more frequent than others, which may indicate that people prefer using optimistic language on twitter. Also, they classify tweets into different topic according to the keywords, such as 'dollar', '$', 'gold', 'oil', 'job', 'economy', and the correlation and Ganger causality analysis shows that a certain number keywords correspond to the market trends respectively, especially the relationship between 'dollar' and stock market in correlation test, and between 'gold' and gold market or currency market in Ganger test. Also, he result shows that there is a significant corresponding to next day buying, but a less meaningful relationship from the two-or-three-day-before tweets. The main limitation of this investigation includes: 1. they assume the relationship between market movement and tweets is linear, but in reality, it is hardly to happen, so the correlation test and the Granger causality test limited the result; 2. they predesigned the keywords of tweets and restrict the data only in retweet form, which may ignore some useful information about other factors; 3. they have not use any sentiment analysis methods to help analysing, but only rely on the predesigned keyword analysis, which may also neglect or exaggerate the hidden relationship between market and tweets.
