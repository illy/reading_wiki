In this paper, we test a hypothesis based on the premise of behavioral economics, that the emotions and moods of individuals affect their decison making process, thus, lead-ing to a direct correlation between ” public sentiment” and ” market sentiment”

We perform sentiment analysis on pub-licly available Twitter data to find the public mood and the degree of membership into 4 classes - Calm, Happy, Alert and Kind (somewhat like fuzzy membership).

Publicly available Twitter data containing more than 476 million tweets corresponding to more than 17 mil-lion users from June 2009 to December 2009.

The data includes the timestamp, username and tweet text for every tweet during that period.

Since we perform our prediction and analysis on a daily basis, we split the tweets by days using the timestamp information.

the DJIA values obtained using Yahoo! Finance was (understandably) absent for weekends and other holidays when the market is closed. In order to complete this data, we approxi-mated the missing values using a concave function.

So, if the DJIA value on a given day is x and the next avail-able data point is y with n days missing in between, we approximate the missing data by estimating the first day after x to be (y +x)/2 and then following the same method recursively till all gaps are filled.

Moreover, as we know the public memory is very short and even though the market may be trading at a much higher level than the previous year, that does not mean that calmness will be much higher than previous year; public mood is a very local metric.

Therefore, we adjusted our stock values by shifting up/down for steep falls/jumps, re-spectively; making sure that we do not disturb the daily directional trend (up/down movement of stock prices).

While there has been a lot of research go-ing on in classifying a piece of text as either positive or nega-tive, there has been little work on multi-class classification.

POMS is an established psychometric questionnaire which asks a person to rate his/her current mood by answering 65 different questions on a scale of 1 to 5 (For example, rate on a scale of 1 to 5 how tensed you feel today?).

These 65 words are then mapped on to 6 standard POMS moods- Tension, Depression, Anger, Vigour, Fatigue and Confusion. In order to do automate this analysis for tweets, the word list needs to be appro-priately extended.

Therefore, we filtered and considered only those tweets which are more likely to express a feeling, i.e. we con-sider only those tweets which contain the words ” feel” , ” makes me” , ” I'm” or ” I am” in them.

It is important to note that, given our formulation, it does not make much sense to compare the value of one mood against another; they should only be used to compare mood trends across days.

For SVM we used the LIBSVM [2] library, but we implemented the other three in MATLAB ourselves as we could not find good working libraries for them.

Therefore, after finding a causality relation between the past 3 days moods and current day stock prices, we tried 4 dif-ferent learning algorithms (Linear Regression, Logistic Re-gression, SVMs, Self Organizing Fuzzy Neural Networks) to learn and study the actual correlation.

The Self Organizing Fuzzy Neural Net-work (SOFNN) is a five layer fuzzy neural network which uses ellipsoidal basis function (EBF) neurons consisting of a center vector and a width vector.

Neural networks have been considered to be a very effective learning algorithm for de-coding nonlinear time series data [4], and financial markets often follow nonlinear trends.

our results also in-dicate that SOFFNs do the best among all other algorithms, giving nearly 75.56% accuracy.

Our Granger Causality analysis indicates that Calm and Happy are causative of the DJIA values.

When using classification algorithms, we used the up/down trends as class inputs and used the algorithm to directly predict trends whereas when using regression algorithms, we fed the normalized stock val-ues as input and used the predicted stock values to obtain direction (up/down) trends.

Firstly SVMs and Logistic Regression perform badly on this dataset, giving the same percentage values for Direction Accuracy for all mood combinations.

Linear Regression performs pretty good, which is in conjunction with the Granger Causality re-sults, whereas SOFNN performs the best.

This shows that by adding more features we would essentially be overfit-ting the data.

As mentioned ear-lier, this technique makes more sense for stock data because the usual cross validation would essentially be using future stock values to predict the past ones, which is an incorrect technique when financial data is concerned.

We develop a naive greedy strategy based on a simple assumption that we can hold at most one stock at any given time (or s stocks if all stocks are always bought and sold together)

Secondly, among the observed dimensions of moods, only calmness and happiness are Granger causative of the DJIA by 3-4 days.

Finally a naive implementation of portfolio management using our strategy indicates a decent profit over a range of 40 days.

Firstly our results show a better correlation between the calm and happy mood dimen-sions with the DJIA values, unlike their result, which showed high correlation with only calm mood dimension.

Secondly, we haven't been able to obtain high percentage result of 87%, but our 75.56% result using k-fold sequential cross val-idation gives stronger evidence that the correlation is over the entire range of data.

Firstly, our dataset doesn't really map the real public sentiment, it only considers the twit-ter using, english speaking people.

###Summary

Another similar work by Mittal and Goel (2012) is also based on Bollen et al's work (2010), in which they classify the sentiment into four dimensions: calm, happy , alert and kind, and they also only consider the tweets containing patters such as "feel", "makes me", "I'm" and "I am". The split the tweets into a daily category according to the timestamp. They estimate the missing data in stock index (basically the weekend data) by a concave function. Moreover, they indicate that "public mood is a very local metric", so they modify the sudden changes in the stock trend. They suggest that different mood curves should not be compared together, but they only show the daily changes. Comparing different learning algorithms: linear regression, logistic regression, SVMs, Self Organising Fuzzy Neutral Networks(SOFNN), they find that the SOFNN performs best, followed by linear regression, but SVMs and logistic regression cannot reach the expectation. Their experiment confirms that different moods reflect differently to the market (Bollen et al. 2010): the calmness and happiness can be considered as Granger causative of the index by 3-4 days.
