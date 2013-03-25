##Abstract

> Microblogging forums have become a vibrant online platform to exchange trading ideas and other stock- related information. Using methods from computational linguistics, we analyze roughly 250,000 stock- related microblogging messages, so-called tweets, on a daily basis for the first 6 months of 2010. Our study compares the tweets’ sentiment, message volume, and level of agreement with the corresponding market features return, trading volume, volatility, and spread. We find the bullishness of tweets to be associated with abnormal stock returns. However, new information, reflected in the tweets, is incorporated into market prices quickly and market inefficiencies are difficult to exploit with the inclusion of reasonable trading costs. An event study of buy and sell signals shows that microbloggers follow __a contrarian strategy__. Message volume can predict next-day trading volume. Next to the analysis of tweet and market features, our results offer an explanation for the efficient aggregation of information in microblogging forums. Users who provide above average investment advice are retweeted (i.e., quoted) more often, have more followers and are thus given a greater share of voice in microblogging forums. In sum, we find that stock microblogs contain valuable information that is not yet fully incorporated in current market indicators.


##Background

There are many examples of investors who attribute their trading success to the information they find on social media websites and Twitter-based trading systems have been developed by financial professionals to alert users of sentiment-based investment opportunities (StreamBase, 2009) and by academic researchers to predict break-points in financial time-series (Vincent & Armstrong, 2010).

Stock microblogs have not yet been the subject of scholarly research. This is a troubling oversight because the unique characteristics of stock microblogging forums, first, do not allow us to transfer results from previous studies of internet message boards and, second, permit researchers to observe aspects of information diffusion in an online investment community, which are unavailable in other settings

Since all of these studies have explored internet stock message boards, we know very little about the information content of stock microblogs with respect to financial markets:

1. First, unlike Twitter's public timeline, message boards categorize postings into separate bulletin boards for each company, which may lead to significant attention to outdated information as long as there are no more recent entries. 

2. Second, while bulleting boards require users to actively enter the forum for a particular stock, Twitter represents a live conversation. 

3. Third, unlike anonymous message board users who can be indifferent to their reputation in the forum, microbloggers have a strong incentive to publish valuable information to maintain or increase mentions, the rate of retweets and their followership – these incentives provide the Twittersphere with a mechanism to weigh information.

The nature of microblogging forums makes previously unavailable aspects of information diffusion _partially observable_ (e.g., retweets and followership relationships).

##Research Purpose

It remains _unclear_ whether, on a large scale, stock microbloggers produce valuable information or simply represent the online equivalent of uninformed noise traders. Therefore, __the purpose of our study__ is to explore whether and to what extent stock microblogs reflect and affect financial market developments.

In particular, for comparison with related research (Antweiler & M. Z. Frank, 2004), our study compares the most important and heavily studied market features return, trading volume, volatility, and spreads with the corresponding tweet features message sentiment (i.e., bullishness), message volume, and the level of agreement among postings. In addition, we empirically explore possible explanations for __the efficient aggregation of information in microblogging forums__.

The overarching questions are:

1. whether bullishness can predict returns

2. second, whether message volume is related to returns, trading volume, or volatility, 

3. whether the level of disagreement among messages correlates with the trading volume, volatility or bid- ask-spreads.

4. In addition, to explore whether microblogging forums weigh information effectively and establish a link between information and returns, we compare the quality of investment advice with the level of mentions, the rate of retweets and the author's followership.

##Research perspectives

1. this study is not limited to crude measures of online activity (e.g., message volume or simple word counts), but leverages sophisticated methods from computational linguistics to evaluate the actual message content and sentiment.

2. Second, our study is not limited to the correlation of online message content with financial market indicators, but offers an explanation for the efficient aggregation of information in stock microblogging forums.

3. Third, this study replicates and extends similar research in the context of internet message boards without previous limitations (e.g., sample selection, timeframe).

4. In addition, we examine the economic exploitability of trading schemes based on signals embedded in stock microblogs.

As illustrated in the previous section, the message board literature has focused on three primary features: message sentiment (i.e., bullishness), message volume, and the level of agreement among postings.

__Our study compares these tweet features with the corresponding market features return, trading volume, volatility, and spread__.

The focus of our study is on the market features return, trading volume, volatility, and spread and the corresponding tweet features bullishness, message volume and agreement.

##Main findings

__We find bullishness to be associated with abnormal returns__.

However, new information, reflected in the tweets, is incorporated in market prices quickly and market inefficiencies are difficult to exploit with the inclusion of reasonable trading costs. An event study of buy and sell signals shows that microbloggers follow __a contrarian strategy__.

__we conclude that stock microblogs contain valuable information that is not yet fully incorporated in current market indicators__.

###EMH

The widely accepted semi-strong version of the EMH claims that prices aggregate all publicly available information and instantly reflect new public information. Therefore, according to the EMH, investors cannot earn excess profits from trading strategies based on publicly available information (Fama, 1970; 1991). However, a growing body of research suggests that financial markets do not always comply with the EMH (for a comprehensive overview see (Malkiel, 2003)).

According to the EMH, stock prices should not be affected by this type of information (inside information). The research on stock message boards confirms this hypothesis. (Tumarkin & Whitelaw, 2001) have found no evidence that any information is embedded in voluntary disclosed user ratings (from strong buy to strong sell).

###WoM

In particular, empirical studies have shown that investors are often influenced by word of mouth (e.g., (Ng & Wu, 2006); (Hong, Kubik, & Stein, 2005)).

##Data source

Sources of qualitative data, such as those mentioned above, have been largely ignored in the financial literature, possibly because computational linguistic methods, as applied in this study, are necessary to process the information and have only recently been recognized by scholars in the financial literature.

(Das & M. Chen, 2007) have illustrated the use of natural language processing algorithms to classify stock messages based on input from human coders.

The massive amount of digital content creates specific challenges for the analysis of these data sets.

1. On one hand, many studies with a background in computer science put an emphasis on natural language processing and text classification.

2. On the other hand, studies from the finance community are mostly limited to quantitative input data (such as ratings provided by users of online communities).

During this period, we have collected 249,533 English-language, stock-related microblogging messages containing the dollar-tagged ticker symbol of an S&P 100 company.14

We focus on the S&P 100 to adequately reflect the entire spectrum of US equities, including a wide range of industries, while limiting our study to well-known companies that trigger a substantial number of stock microblogs.1

In order to compare the signals from stock microblogs to market movements, we had to classify messages as either buy, hold or sell signals.

Compared to more advanced methods in computational linguistics, this method is relatively simple (e.g., high replicability and few arbitrary fine-tuning parameters), but has consistently shown robust results while providing a high degree of transparency into the underlying data structure

We use the multinomial Naïve Bayesian implementation of the Weka machine learning package (Hall, E. Frank, Holmes, & Pfahringer, 2009). This conditional probability illustrates the algorithm's “naïve” assumption that all words, or features, are independent of each other.

The dictionary can be pruned by choosing the most representative set of words in terms of the information gain criterion (IG). IG measures the entropy difference between the unconditioned class variable and the class variable conditioned on the presence or absence of the word.

Our classification method uses individual words as input variables (a so-called “bag of words” approach).

We apply the widely used Porter stemmer in order to remove the morphological endings from words (e.g., “buys” and “buying” are reduced to “buy”; (Porter, 1980)).

Input for the Naïve Bayesian model comes from a training set of 2,500 tweets, which we manually classified as either buy, hold, or sell signals.

###Message board

One of the most intriguing sources of unofficial and qualitative information is the vast amount of user-generated content online.

Prior literature shows that the information exchange in online financial communities includes the dissemination of public information, speculation regarding private and forthcoming information, analysis of data, and personal commentary (see (Lerman, 2010); (Felton & J. Kim, 2002); (Das, Martinez-Jerez, & Tufano, 2005); (Campbell, 2001)).

While it is fairly obvious why traders would consult these forums for information, _it is less clear what motivates them to share private information_.

Consistent with the EMH, message board activity _did not_ predict industry-adjusted returns and postings followed the stock market.

All of these studies are limited to readily available quantitative information (e.g., message volume, user ratings).

Evidence from stock message boards has shown that self-disclosed ratings are often biased.

“Hold” sentiments, for example, are systematically optimistic and significantly differ from neutral (Yc Zhang & Swanson, 2010).

However, buy and sell signals may carry very different information with respect to subsequent stock returns and the true information value of online messages becomes apparent only when measured against market-adjusted abnormal returns.

Empirical evidence shows a __significant increase__ in daily trading volumes, lower returns, and higher volatility after a firm's message board was established.

Whereas all of these studies have explored internet stock message boards, we know very little about the information content of stock microblogs with respect to financial markets.6

Consistent with the EMH, message board activity did not predict industry-adjusted returns and postings followed the stock market.

###Microblog

A few recent studies suggest that the information content of microblogs may help predict macroeconomic market indicators. (O'Connor, Balasubramanyan, Routledge, & Smith, 2010) have found Twitter messages to be a leading indicator for the Index of Consumer Sentiment (ICS), a measure of US consumer confidence.

Both (X. Zhang, Fuehres, & Gloor, 2010) and (Bollen, Mao, & Zeng, 2010) find that a random subsample of messages from Twitter's public timeline can be used to predict market indices such as the Dow Jones Industrial Average (DJIA) or the S&P 500. However, all of these studies are concerned with broadly defined data sets (e.g., all available messages or blog posts in the sample period, most without a specific reference to the stock market) and derive aggregate sentiment measures.

__While the correlation of these aggregate measures with macroeconomic indicators is encouraging, it does not allow us to draw conclusions about the information content of stock microblogs with respect to individual stocks__.

##Research questions

Therefore, our study focuses on the specific domain of stock microblogs and investigates their relationship with market prices of publicly traded companies.

1. we derive our hypotheses for the study of tweet and market features (H1-H3b) and, 

2. for the study of information diffusion in stock microblogging forums (H4a-H4b).

While empirical findings suggest that online information networks may change market behavior and are not just an indicator of otherwise motivated investor behavior (A. L. Jones, 2006), we will adopt this more conservative interpretation of our results and understand the relationship between the two as the reflection of information in the tweets.

1. Hypothesis 1: Increased bullishness of stock microblogs is associated with higher returns.

2. Hypothesis 2a: Increased message volume in stock microblogging forums is associated with an increase in trading volume.

    Cao, Coval, & D Hirshleifer, 2002) have suggested that conversation among market participants induces trading from all kinds of so-called “sidelined investors” who decide to trade as they learn that other traders share a similar signal.

    While (Antweiler & M. Z. Frank, 2004) report that the effect of message volume on stock returns was negative and, although statistically significant, economically small, there is empirical

3. Hypothesis 2b: Increases in message volume in stock microblogging forums are associated with higher returns.

4. Hypothesis 2c: Increased message volume in stock microblogging forums is associated with higher volatility. evidence from message boards supporting this notion

    (Danthine & Moresi, 1993) suggest that more information reduces volatility because it increases the chances of rational agents to counteract the actions of noise traders.

    (Antweiler & M. Z. Frank, 2004) show that, on internet message boards, message volume is a predictive factor of volatility.

5. Hypothesis 2d: Increased message volume in stock microblogging forums reduces information asymmetry indicated by lower spreads.

6. Hypothesis 3a: Increased disagreement among stock microblogs is associated with higher volatility.11

    In line with (Danthine & Moresi, 1993) more information should reduce volatility. However, intuition suggests that disagreement and volatility should be positively correlated.

7. Hypothesis 3b: Increased disagreement among stock microblogs is associated with an increase in trading volume.

    “no-trade-theorem” suggesting that disagreement can reduce trading as the risk-averse participants of a trade are aware that the other party would only enter the trade to their advantage and any attempt to speculate on new, private information will impound this information in market prices. However, this theory is based on the assumption that “new information is never small” and would instantly move market prices.

8. Hypothesis 4a: Users who consistently provide high quality investment advice have more influence in the microblogging forum (through retweets, mentions, or followers).

    In addition, there is empirical evidence that, despite the abundance of available information and considerable noise, Twitter users follow the accounts to which they subscribe closely and are highly attentive to their content: A working paper studying a single Twitter account making directional forecasts of the stock market indicates that the number of followers may be correlated with the accuracy of the published information (i.e., the forecasts of the stock market; (Giller, 2009)12).

9. Hypothesis 4b: High quality pieces of microblogging investment advice attract greater attention and are spread more widely than low quality pieces of advice (through retweets).

    (Yang & Counts, 2010) illustrate that, next to the properties of Twitter users, some properties of their messages (such as the inclusion of a link), can predict greater information propagation.

    On the other hand, (Romero, Galuba, Asur, & Huberman, 2010) claim that the majority of users act as passive information consumers and do not forward the content to the network.

    Both studies were conducted with large, randomly sampled data sets and do not capture a specific domain such as stock microblogging. Therefore, next to high quality advisors, we examine whether high quality pieces of investment information (i.e., individual messages) are weighted more heavily and spread through retweets.

##Analysis

Roughly half of these messages were considered to be hold signals (49.6%). Among the remainder, buy signals were more than twice as likely (35.2%) as sell signals (15.2%).

This indicates that stock microblogs appear to be more balanced in terms of bullishness than internet message boards where the ratio of buy vs. sell signals ranges from 7:1 (Dewally, 2003) to 5:1 (Antweiler & M. Z. Frank, 2004).

As Table 2 shows, overall in-sample classification accuracy was 81.2%. Even a more conservative 10-fold cross validation of the model within the training set correctly classifies 64.2% of all messages.

###Sentiments

__False positives are less likely among buy and sell signals than among hold messages. For our purposes, falsely labeling a buy or sell signal as hold is more acceptable than falsely interpreting messages as buy or sell signals__.

1. Positive emotions, for example, are much more likely among buy signals. In addition, buy signals often contain bullish words with an origin in technical analysis (e.g., “moving average”, “resistance”, “up”, or “high”), operations (e.g., “acquire”), financials (e.g., “beat”, “earn”), or trading (e.g., “buy”, “long”, “call”).

2. Sell signals contain many corresponding bearish words in the areas of technical analysis (e.g., “support” and “cross”), financials (e.g., “loss”) or trading (e.g., “short” and “put”).

3. As a results of the frequent occurrence of negative adjectives (e.g., “weak”, “low”) and verbs (e.g., “decline”, “fall”), negative emotions are among the most common features in sell signals confirming the finding of (Tetlock, Saar-Tsechansky, & Macskassy, 2008).

4. Positive and negative emotions are much more equally balanced in hold messages, which also contain more neutral words such as product names (e.g., “ipad”, “iphone”) and make fewer references to specific price targets (i.e., dollar values).

Even after the aggregation of individual messages to daily indicators, there are days for some stocks without any tweets. In the absence of messages, we define all three tweet features for these silent periods as zero. However, since our data set contains a full set of both tweet and market features for more than 80% of all company-day-combinations, the influence of silent periods on our results is limited.

Thus, messages posted after the markets close are included in the calculation of tweet features for the following day because these messages can only have an effect on the market indicators of that day or be affected by other factors that are not apparent in the market indicators until the next day.

__In line with common practice (e.g., (Dyckman, Philbrick, & Stephan, 1984), we use a 120-day estimation period starting 130 days prior to the relevant date to not overlap with the event-window of our event study__.

Because Twitter does not provide information regarding the relationship of individual tweets, we identified retweets in our data set by filtering all retweets and matching the 40 characters following the retweet token and the name of the original author with all other tweets in the data set. This allows us to separate retweets from non-retweets and identify the originals alongside the frequency with which they were retweeted.

The majority of tweets are posted during the trading hours between 9:30 am and 4:00 pm. This provides further evidence that stock microblogs are used by financial professionals to exchange relevant trading ideas in real time.

###Correlation of tweets and the market

Figure 2 provides us with a first indication of the overall relationships between trading and message volume. The two measures show a strong correlation (r = 0.46, p = 0.016).

The comparison of market returns and a market-cap weighted bullishness index (see Figure 3) exhibits a slightly weaker, but statistically significant correlation between the two indicators (r = 0.41, p = 0.038).

(O'Connor, Balasubramanyan, Routledge, & Smith, 2010) have found that the correlation of their Twitter-based measure of consumer confidence and the Index of Consumer Sentiment (ICS) increased up to a window of 60-day moving averages.

We observe the contrary with the correlation of a moving-average bullishness index and the market losing statistical significance when we increase the window beyond 10 days. This indicates that the bullishness of stock microblogs accurately captures market movements fairly quickly.

The summary statistics by company (Table 5) illustrate that there are some stocks, especially high-tech companies and to a lesser extent financial institutions, that trigger a majority of the conversation.

Contemporaneous pairwise correlations provide a first indication with respect to the relationships between market and tweet features (Table 6). We observe a relatively strong correlation between bullishness and returns (r = 0.166, p-value = 0.0).

The sentiment in microblogs clearly picks up on absolute market movements.

But even simple, market-index-adjusted returns (0.156, p-value = 0.0) and market-model-adjusted returns (0.147, p-value = 0.0) are among the strongest correlations between market and tweet features.

It is interesting that, despite the growth of microblogging and potential variations in crawling efficacy, the normalized relative message volume shows a much weaker correlation with the trading volume.

Already on the level of pairwise correlations we need to reject our hypothesis that an increase in message volume is associated with a reduction in spreads (H2d). To the contrary, an increase in message volume seems to indicate an increase in information asymmetry (0.152, p-value = 0.0).

As hypothesized (H3a), trading volume decreases as agreement rises (-0.113, p-value = 0.0). While the pairwise correlation indicates that agreement among investors also coincides with lower volatility (-0.014, p-value = 0.13), this correlation is not statistically significant (H3b).

Overall, it is worth noting that many correlations between tweet and market features are stronger than closely studied relationships among market features, such as the relationship between volatility and trading volume (0.046, p-value = 0.0).

While the pairwise correlations have suggested some interesting relationships between tweet features and market features, they do not address the independence of these relationships. It remains unclear whether these relationships remain significant when all tweet features are controlled for.

Due to significant cross-sectional differences in message volume (see Table 3), we use fixed-effects for each stock. The regressions confirm the strong relationship between bullishness and all three return measures (H1). Thus, increased bullishness can serve as a proxy for positive investor sentiment indicated by rising stock prices.

Since both volume measures were log transformed, we can interpret the coefficients as elasticities. A 1% increase in the message volume is associated with a more than 10% increase in trading volume (c = 10.798).

In line with H2c, we observe an increase in volatility as the message volume rises (1.391). While disagreement does no longer explain volatility (H3a) the negative correlation of agreement and trading volume (H3b) survives the inclusion of other tweet features (-4.644).

We conclude that the contemporaneous relationships between bullishness and returns, message volume and trading volume, as well as agreement and trading volume appear to be the most robust.

__If microblogs contain new information not yet reflected in market prices, tweet features should anticipate changes in market features__.

We regress one and two day lags of every tweet feature on every market feature separately (and vice versa). Similar to the contemporaneous regressions, we use panel regressions with company fixed effects and the market index as a control.

Because market returns have been repeatedly found to be negative on the first trading day of the week (e.g., (Lakonishok & Levi, 1982)), we also include a dummy variable for this day (NWK) in line with (Antweiler & M. Z. Frank, 2004)

__The most obvious question in time-series analysis of microblogs and the market is whether message sentiment can help predict returns (H1)__.

Table 8 shows that, while there is almost no effect of bullishness on next day returns, bullishness two days ago is, contrary to our hypothesis, associated with negative returns (c = -0.057). On the other hand, previous day returns have a positive effect on bullishness (0.035)

The standardized coefficient shows that, in addition to higher statistical significance, the effect of returns on bullishness is about four times as strong as the inverse (0.091 vs. -0.022). Thus, bullishness in stock microblogs is affected more strongly by returns than vice versa.

Message volume one and two days ago seems to predict current day trading volume (H2a). At the same time, high trading volume triggers increased message volume over the next two days. Autocorrelation of trading volumes may explain parts of this effect, which warrants a closer analysis of the relationship in the next section.

However, similar to the relationship between bullishness and returns, the standardized coefficients illustrate that the stronger effect is in the direction from trading volume to message volume. High volatility also leads to increased message volume, confirming that uncertainty causes investors to exchange information and consult their peers.

The opposite relationship, however, does not hold (H2c). While changes in spreads are not related to message volume, there is a weak indication that an increase in message volume is followed by a decrease in spreads (-0.001). This provides evidence in support of our hypothesis that increased information exchange indicated by a rise in message volume can lead to a decrease in information asymmetry (H2d).

It is worth noting that, in contrast to (Antweiler & M. Z. Frank, 2004), we do not find message volume to be related to stock returns (H2b). This indicates that investors may take a more nuanced approach in processing information content of stock microblogs compared to message boards.

In line with the contemporaneous regressions, disagreement is not associated with higher volatility (H3a). However, we find some confirmatory evidence for H3b that agreement among traders does lead to lower trading volumes (-2.022 for X-2).

In summary, we conclude that while some tweet features appear to contain predictive information with respect to market features (especially bullishness for returns and message volume for trading volume), the standardized coefficients show a much stronger effect of market features on tweet features.

In contrast to all other analyses, where we assign messages posted after 4:00 pm to the next trading day, we define message volume and agreement as the respective tweet features for the 24 hours prior to the market open. We take this approach for the purposes of this analysis because it more closely represents the information that is available to predict trading volume.

Next to message volume and agreement, we add the control variables following (Antweiler & M. Z. Frank, 2004). These include previous changes in the stock price, the market index, and market volatility as well as the federal funds rate (FFR), the quality spread (between corporate BB bond yields and the treasury rate), and the term spread between the FFR and the 10-year treasury bill rate.

1. First, while the direction of the coefficients is consistent with previous analyses for both tweet features, only message volume survives the inclusion of the above-mentioned control variables. 

2. Second, a comparison of standardized coefficients shows that message volume explains trading volume better than some of these accepted control variables.

We conclude that message volume contains valuable information with respect to next-day trading volume (H2a). To explore the information contained in these sentiments, we conduct an event study of returns around the day of particular strong buy and sell signals. The development of returns around the event day can inform us about traders' motivation to recommend a stock.

In line with (Tumarkin & Whitelaw, 2001), we define an event-day as a day when the bullishness index of a particular stock exceeds the previous 5-day average by at least two standard deviations. Event days with less than 5 messages for a stock were excluded from the sample.

One day before the event day, returns bottom out. Following this sustained decrease, we notice a reversal in abnormal returns.

More importantly, the return reversal allows us to earn statistically significant abnormal returns on the day following the recommendation.

In addition, abnormal returns on the day following the recommendation are a conservative measure since many traders may pick up the signal on the event day and capture some of the abnormal returns on that day (0.45%).

We find a similar pattern with respect to sell recommendation. Returns of the recommended securities have risen steadily from days -6 to -2 until they reach a peak on t-1. Microbloggers then recommend selling the stock, which, indeed, shows statistically significant negative returns on that day. Even though the stock continues to fall for 3 more days, abnormal returns are no longer statistically significant.

In summary, our event study shows that microbloggers follow a contrarian strategy with strong buy signals being followed by abnormal next-day returns (H1). This finding is contrary to previous research of stock message boards, where users followed a naïve momentum strategy and no new information was contained in their recommendations (Dewally, 2003; Mizrach & Weerts, 2009; Tumarkin & Whitelaw, 2001).

To more thoroughly test the ability to earn abnormal profits based on message bullishness, we design a market-neutral trading strategy in line with (W. Zhang & Skiena, 2010).

On every trading day, we buy (and sell) the stocks with the highest (and lowest) level of bullishness. We distribute our investment equally across the selected stocks. As usual in this type of analysis, we initially ignore transaction costs (W. Zhang & Skiena, 2010).

There are three key parameters, which may influence our trading result. 

1. the number of previous days we use to calculate bullishness (i.e., sentiment history). 

2. the number of stocks we select from the top and bottom of our bullishness ranking (number of stock picks), 

3. the number of days for which we will hold these stocks (holding period).32

In order to better understand the impact of these parameters on our trading results, we conducted a sensitivity analysis backtesting the performance of our strategy. In this analysis, we alter one of the three parameters while leaving the other two constant.

Due to the negative correlation of returns and more than 1-day lags of bullishness found in our predictive regression, we choose a short 1 day default value for the sentiment history.

Assuming that new information reflected in the tweets is incorporated into prices quickly, we choose a default holding period of one day.

Generally, short sentiment signals produce higher returns. Longer sentiment signals even produce negative returns, confirming the contrarian strategy embedded in message bullishness (e.g., a few days prior to strong sell signals, stocks prices are actually rising sharply, explaining the loss from the short end of the trading strategy with 3-day-old sentiment signals).

Except for some benefits of noise reduction with up to 3 stocks, increasing the number of stock picks generally decreases returns. This indicates that the ranking identified the top performers fairly accurately.

In the short term, only a one-day holding period is associated with positive returns for both the long and short position.

The fact that our strategy performs even better with long holding periods (of between 6 and 9 days) is in line with the drift in cumulative returns found in our event-study. However, we would be cautious to interpret these returns as the reaction to information contained in the news.

(Tetlock, Saar-Tsechansky, & Macskassy, 2008), who found a trading strategy based on negative words in firm specific news articles to earn abnormal annualized returns of more than 20%33, showed that these returns evaporated with the inclusion of reasonable transaction costs.

We can see that the strategy starts losing money with transaction costs of more than 7 bps, roughly in line with the threshold determined by (Tetlock, Saar-Tsechansky, & Macskassy, 2008). In addition, our analysis shows a slightly better performance of the short end of the trading scheme. However, even this side supports transaction costs only up to 8 bps.

__In conclusion, we find that a strategy based on bullishness signals can earn substantial abnormal returns__.

Strategies based on short-term signals and short holding periods produce higher returns, indicating that new information, reflected in the tweets, is incorporated in market prices quickly.

However, market inefficiencies are difficult to exploit with the inclusion of reasonable trading costs.

One possible answer is that information is aggregated and weighted efficiently.

We investigate two aspects: First, we examine whether high quality pieces of information (i.e., individual messages) may be weighted more heavily and spread through retweets (H4a). Second, we investigate whether we can identify above average advisors (i.e., market mavens or investment gurus) and whether these users have a greater share of voice in the online community through higher levels of retweets, mentions or followers (H4b).

Greater weight given to high quality pieces of investment advice could explain efficient information aggregation in stock microblogging forums.

While the average quality across all messages is 55.8%, the difference between retweets (55.9%) and non-retweets (55.1%) is miniscule and statistically not significant.

1. many authors only forward parts of the message and add their own commentary. This may change the bullishness of the message and no longer correspond to the original market movement. 

2. if a message is retweeted a day after the original message, the signal may no longer correspond with same-day returns.

(Yang & Counts, 2010) have shown that the properties of users are stronger predictors of information propagation than properties of the tweets.

Users have an interest to subscribe to the content of high quality investment advisors. While they may not constantly identify high quality pieces of information in the message stream, they may notice and pay more attention to market mavens who consistently provide good investment advice. If these investment gurus had more followers, their contributions would get greater attention.

Even among users with hundreds of messages, we can identify some that seem to consistently provide higher quality investment advice than others.

The followers are the most immediate recipients of an authors tweets and a larger audience should increase the chances of a message being retweeted.

In addition, (Y Zhang, 2009) reports that the average sentiment affected a user's reputation with more bullish users gaining higher reputation scores. We therefore compute the average sentiment for a user's messages coding buy, hold, and sell signals as 1, 0 and -1, respectively.

(Y Zhang, 2009) has shown that, while accuracy with respect to same-day returns did not affect a users reputation, one- day follow opinions has a positive effect (i.e., buy recommendations for stocks that had risen the day before).

As a result, the number of stock followers is only weakly correlated with retweets (0.05) and mentions (0.1) and shows no significant correlation with the total number of followers (0.01).

Obviously and as hypothesized, message volume and followership are positively related to retweets and mentions.

However, more importantly and beyond the natural volume effect, users who provide higher quality investment advice are retweeted more frequently (c = 0.777).

In contrast to message boards, where a one-day follow up lead to greater reputation, appreciation of information quality in stock microblogs appears to be more short-lived.

While the number of retweets can be explained by the quality of the investment advice, the coefficients are not significant in the case of user mentions (albeit the direction of the coefficients indicates a similar relationship).

Followership increases with higher quality same day investment advice (2.514). Again, a one-day follow-up representing a momentum strategy hurts followership (-2.386).

The determinants of followership among serious stock microbloggers are not significant. This may have to do with the difficulty to clearly define this group, as indicated above.

We find, 

1. that stock microblogs contain valuable information that is not yet fully incorporated in current market indicators and, 

2. that retweets and followership relationships provide microblogging forums with an efficient mechanism to aggregate information.

Buy signals are accompanied and followed by abnormal returns, which exceed frequently assumed levels of transaction costs. Sell signals have no predictive power for returns.

The predictive power of message volume even survives the inclusion of numerous accepted control variables. However, the empirical evidence shows no consistent relationship between changes in message volume and spreads.

However, we note that while some tweet features appear to contain predictive information with respect to market features, the standardized coefficients show a much stronger effect of market features on tweet features.

Our analysis of information diffusion in the form of retweets, mentions, and followership shows that users who provide above average investment advice are given credit and a greater share of voice in microblogging forums through higher levels of retweets and followers. However, the analysis of individual messages shows that higher quality pieces of information are not retweeted more frequently.

1. we use only daily granularity of analysis.

    This restriction limited us to daily data because there are only a handful of stocks that attract sufficient message volume for daily analysis.

    As a result, bullish messages toward the afternoon may merely reflect market developments over the course of the trading day, which are unlikely to reverse.

2. in line with previous research, we have considered microbloggers to be day traders.

    However, in the case of trading volume, one could replace volume with the number of trades of different size categories to distinguish between small and institutional investors. We favored a more simple approach because the insights gained from this distinction in previous research of internet message boards (Antweiler & M. Z. Frank, 2004) were limited

3. as is the case in most large-scale studies of financial market data, many conclusions need to be interpreted with caution.

    Even though the aggregate conclusions are correct, we cannot expect significant relationships, such as the one between message and trading volume, to hold for each and every individual stock.

5. we have explored the information content of stock microblogs in terms of sentiment (i.e., bullishness), arguably the most critical piece of information value contained in these postings. However, the definition of information could be expanded to include other dimensions such as the topic or type of news that is discussed.

6. we study the reflection of market developments in stock microblogs. While we find some notable relationships, our results do not allow us to determine whether these forums are merely reflecting investor behavior or have changed market behavior.

We observe a more balanced ratio of buy and sell signals and traders no longer follower a naïve momentum strategy, but seem to recommend contrarian trading positions.

Quality and content appear to be more important than quantity, since bullishness is related to returns more strongly than message volume.

Increased bullishness can serve as a proxy for positive investor sentiment indicated by rising stock prices.

Users primarily post messages concerning stocks that are traded more heavily.

One of the most critical aspects of further research will be to better understand the mechanism by which information is weighted and diffused in microblogging forums.

###Reading summary

There are many online sources discussing market-related topics, but previous studies might not be very satisfied due to some limitations, for example, lacking of sufficient data of the online communication. As Sprenger & Welpe (2011) point out that, because of the massive information available, the research on this topic mainly divides into two backgrounds: one from computer science may ignore the financial aspects of this problem, but focus on "message sentiment, message volume, and the level of agreement among postings", while the other from finance may be limited in their knowledge of dealing with textual data, particularly the NLP approaches. Thus, they attempt to balance the gaps between these two fields, and provide a comprehensive and detailed empirical study on "whether and to what extent stock microblogs reflect and affect financial market development" on both index level and company level: this study applies Naive Bayes algorithm with the "bag of words" approach to categorise the tweet data into "buy, hold and sell" groups, and by this, then they achieved an 81.2% overall in-sample accuracy, and found that the tweet data is more balanced in respect of bullishness than other online domains. They confirm that the next-day effect exists in such a circumstance, in particular, this effect is apparent in abnormal returns, so "short sentiment signals produce higher returns" while "longer sentiment signals even produce negative returns". Also, they find that the window for tweets with the moving-average bullishness index correlation is about 10 days, which is much shorter than other market indices. Moreover, they suggest there are some "certain valuable information" that are not recognised by traders in practice. The research reveals that twitter is a perfect real time financial information source, for example, it would provide prompt bullishness signal, in relation with that the majority of market-related tweets were posted in trading time, and the p-value of the overall correlation between is 0.016, which is statistically significant. Specially, both p-value of the relationship between market-index-adjusted returns and market-model-adjusted returns are 0.0, which suggests the certainty of these relationships, and a 1% increase in the message volume will bring a more than 10% increase in trading volume, also the bullishness in the market will be reflected correspondingly in tweets. As shown in the result, most discussions on Twitter focus on "high-tech companies and to a lesser extent financial institutions". Furthermore, the research also confirmed several features of market itself. For instance, there is a strong correlation between bullishness and returns, the trading volume will drop if more agreements are reached.

Although they indicate that retweets would help increase user's influence on Twitter environment; these pieces of information will not directly improve the performance of trading, because people usually retweet high-profile users' tweets instead of high quality tweets. And contrary to the study by Tonkin, Pfeiffer & Tourte (2012), this study emphasises the effect of message volume, particularly the retweets, whose increase would formulate the growth in information asymmetry (p-value = 0.0), especially the next-day trading volume, but it will not trigger the growth of the returns consequently. Despite the effect of retweets, the study also discloses the contribution of fellowship and mention to the user's influence. More importantly, they demonstrate that market influences twitter discussion than vice versa.

They conclude five limitations of their study, such as only focusing on daily granularity, considering Twitter as a host of day-traders, the influence of high variance on the large-scale data, dealing sentimental information in a very limited way, and no in-depth analysis of the influence of microblogs to individual investors or to the whole market. However, the most critical limitation is their sentiment analysis is only based on bag-of-words feature.
