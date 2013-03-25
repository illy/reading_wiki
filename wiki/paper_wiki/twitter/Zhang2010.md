There are several streams of research investigating the role of Twitter. One stream of research focuses on understanding its usage and community structure.

Another stream of research concentrates on influence of Twitter users and information propagation.

Besides the general understanding of Twitter, other researchers are interested in its prediction power and potential application to other areas.

There is also prior work on analyzing correlation between web buzz and stock market.

We collected the twitter feeds from one whitelisted IP for six months from March 30, 2009 to Sept 7, 2009, ranging from 8100 to 43040 tweets per day. According to Twitter, this corresponds to a randomized subsample of about one hundredth of the full volume of all tweets, as the total volume in 2009 was about 2.5 million tweets per day.

As is well known, emotional state can influence our decisions, and no doubt such choice includes stock market investment decision (Gilbert et. al 2010).

This implies that most of the tweets have simple meaning, and even just one or two key words may capture the main topic. Inspired by this property, we decided to use mood words, for example “fear”, “worry”, “hope” etc., as emotional tags of a tweet. Then we measured collective emotion each day by simply counting all tweets containing such words.

When people are pessimistic or uncertain about the future, they will be more cautious to invest and trade.

More interestingly, we also find that the number of positive tweets is much higher than that of negative ones, more than double on average, which might suggest that people prefer optimistic to pessimistic words.

In our own data sample we were using the Twitter “public timeline” function, implemented in such a way to deliver a more or less constant stream of messages per day. This stream allowed us to measure the percentage of emotional tweets among all the tweets.

Using “hope” as an example, we defined hope%t as the ratio between the number of “hope” tweets on day t and the amount of tweets we collected that day, comparing it with the stock market indicators on day t+1.

Initially we expected that the correlation between optimistic mood and stock market indicators would be positive, and the pessimistic mood would negatively correlate.

Surprisingly, we found positive correlation for all of them with VIX, and negative correlation with Dow, NASDAQ and S&P500.

This implies that people start using more emotional words such as hope, fear and worry in times of economic uncertainty, independent of whether they have a positive or negative context.

Follower is a key concept in Twitter, it is commonly seen as a measure of popularity. It is likely that the more followers a user has, the more people s/he can affect.

The correlation coefficients are 0.143, 0.149 and 0.146 separately, which are relatively lower than we expected. As can be seen in Table 3, this index is therefore not a good predictor of stock market indices.

We also found that there were about 40% less retweets at weekends (the nodes underneath the black line in figure 2 are weekends).

We speculate that on weekends, active tweeters have the time to send more original tweets, while during the week they pick up tweets from others they find worthwhile retweeting.

This means, however, that they “stake their reputation” on others' tweets during the weekdays.

Obviosly, number of retweets is a better baseline than number of followers, but simply taking the total number of tweets gives the best results.

This is not surprising, however, because the number of retweets containing “hope” is much lower than the number of tweets containing “hope”, which means that the fluctuation in the results is much higher, therefore leading to smaller sample size and less significant correlations.

All analysis in Section 3.2 focused on the Twitter buzz one day before the trading day. However, this way, a considerable portion of information has been wasted.

Among all the emotional words, hope, fear and worry work best in this analysis.

###Summary

Zhang, Fuehres & Gloor (2010) conclude that there are three mainstream researches focusing on social media: 1. its usage and community structure, 2. influence of Twitter users and information propagation, 3. prediction power and potential application to other areas. One typical example is the hybrid study of above: using social media to predict market trend. Based on Gilbert et al.'s work (2010) that people will be cautious if they are in a pessimistic or uncertain circumstance, they assume that mood will affect people's determinations. Moreover, they hypothesise that most tweets can be captured by few words, so they simply classify tweets into positive and negative by keywords. According to this, they find that different keywords perform differently to the market trend. Thus, they found that people use optimistic words more often. By comparing different stock indies, such as VIX, DJIA, S&P500 and NASDAQ, they found that the predictions based on the amount of tweet posted per day and the retweets of each day are better than that on the number of follower. They also found a 40% decrease of retweets in weekends, and they speculate this as that Twitter users may post more original contents in weekend. This is less meaningful because they have not checked the total tweets in weekend. Intuitionally, there is a sharp drop of total tweets in weekends. Finally, they also evaluated the difference of reaction time of market, among them, the next-day performance is best.
