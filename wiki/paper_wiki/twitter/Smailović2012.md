Three common approaches to sentiment analysis are: machine learning, lexicon-based methods and linguistic analysis.

For our training set we used a collection of 1,600,000 (800,000 positive and 800,000 negative) tweets collected by the Stanford University [10], where positive and negative emoticons were used as labels. For testing we used a set of manually labelled 177 negative and 182 positive tweets from the same source [10]. The SVMperf classifier [11] was used for training and testing.

As it can be seen from the table, the best classifier is obtained by using both unigrams and bigrams, using words which appear at least two times in the corpus, with replacing links with a token and with removal of repeated letters.

We employed the algorithm based on Jaccard similarity [12] to discard tweets that were detected as near duplicates.

The Granger causality test (results shown in Table 2) indicates that positive sentiment probability could predict stock price movements, as we got a significant result (p-value < 0.1 in our dataset for a two day lag.>)
