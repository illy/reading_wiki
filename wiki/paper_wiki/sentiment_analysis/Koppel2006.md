But in most cases, we require human judges to provide an assessment of a document's sentiment. As a result, one of the main research bottlenecks in sentiment analysis has been the procurement of large reliably labeled corpora.

The case of business news concerning a publicly-traded company is a special one, though, because price movements of the company's stock can serve as an objective measure of the valence of a news item (although, not every movement in price is a direct consequence of a given news story).

Thus the use of price movements correlated with the appearance of news items is a promising method for automatically generating a labeled corpus without directly invoking individual human judgments (though, of course, stock movements themselves are a product of collective human judgment).

1. In this paper, we classify news stories about a company according to its apparent impact on the performance of the company's stock.

2. We will check the extent to which a learned model can be used to classify out-of-sample texts in accordance with market reaction.

3. That is, we will determine how much of the information in a news story that drives market reaction can be gleaned from textual features alone.

4. We will also test the degree to which such learned models can be used to turn a profit.

In this work, we avoid such assumptions by making no judgment regarding a story itself. **We are interested only in the market's reaction to the story**. A similar approach was previously considered by Lavrenko et al (2000).

The total number of stories in our database is just over 12,000 – an average of 24 stories per stock. The average length of a story is just over 100 words – short enough to be focused but long enough to permit harvesting of statistics.

1.In the first approach, we matched each story with the change in price of the relevant stock from the market close the day preceding the publication of the story to the market open the day following the story.

2.A different approach, which we did not try, would be to assume that the time-stamp on the story accurately reflects the precise hour when the news became public and to check price changes during a narrower time band around that hour. Unfortunately, such an assumption would be unduly optimistic.

 >In the second approach, we matched each story with the change in price of the relevant stock from the market open the day following the publication of the story and the market open the day following that one.

Although, the first approach provides a more reliable assessment of the story's impact, the second offers a more exploitable one since, if the story is published after market close, the next day's open is the first price at which an investor might be able to purchase the stock.

In both cases, we defined a story as **positive** if the stock in question rose 10% or more and as negative if the stock declined 7.8% or more.

We used these rather high thresholds because such dramatic price moves can be safely assumed to be reactions to news stories and not mere reflections of general market moves or random fluctuation.

The lower threshold for downward moves was chosen so as to provide an equal number of negative examples as positive examples.

We also considered a subset of these stories that satisfied two **additional conditions**:

1.The base price of the stock was at least $10.

2.The percentage change in the stock price is in excess to the percentage change in the S&P.

Such stories can be more reliably linked to the price change of the stock than those that do not satisfy these conditions. Approximately half the stories satisfied both conditions.

We used as our feature set all words that appeared at least 60 times in the corpus, eliminating function words (with the exception of some obviously relevant words such as above, below, up and down). Since the texts are quite short, we represented each text as a binary vector reflecting whether or not a feature is present in the story, but ignoring frequency

Using our first labeling approach, 10-fold cross-validation experiments yielded accuracy of 70.3% using a linear SVM. Training on the entire 2000-2002 corpus, while testing on the 2003 corpus, yielded accuracy of 65.9%. Other learners, including Naïve Bayes and decision trees, yielded essentially the same results. Boosting and selection of other kernels for the SVM also had little effect on results.

In addition, use of the narrower set of more reliable examples yielded essentially the same results despite the fact that the number of training examples was considerably smaller.

1. There are a number of features that are clear markers of negative documents.

2. There are no markers of positive stories; positive stories are characterized only by the absence of negative markers.

In fact, of the twenty words in the corpus with highest information gain, all are negative markers. The honest investor interested in exploiting published news to select an investment vehicle, must use our second labeling approach which reflects price moves subsequent to the publication of the story.

Unfortunately, 10-fold cross-validation experiments using this labeling approach yield much more modest results of just above 52% – probably too small a margin to overcome the cost of trading. **This bears out the so-called Efficient Markets Hypothesis (Fama 1970): "prices fully reflect all available information"**.

Having assembled a modest corpus in this way, w have found that we can learn to automatically characterize news stories about stocks according to their market impact with moderate success. At the very least, we can reliably identify certain stories as negative. More sophisticated features, such as word collocation (Wiebe et al 2001b), might improve matters, but other learning methods are unlikely to improve results significantly.

It is very likely, though, that labeling news stories according to their price impact in **a period of several seconds or minutes following first publication of the story** would yield more promising results. This should be the main direction of future research in this area.

###Summary

Koppel and Shtrimberg's research (2009) tries using the market price to evaluate the polarity of the relavant news, which redirects the research question: the market performance deteremins the news trend as they define "a story as positive if the stock in question rose 10% or more and as negative if the stock declined 7.8% or more. Their result by SVM, NB and decision trees reaches a similar accuracy of about 70%, and they found there are a number of obvious markers in the negative news samples, but not in the positive samples. In addtition, their two labelling strategies brought different results: the one-day approach outperformances the hourly appraoch in general, and they suggest that . Moreover, the experiment also shows that SVM, NB and decision trees perform similarly in terms of classifying the data based on the bigram feature. This method can be used to train the data, providing a reliable training dataset for further analysis by the suggestion of shortening the reaction time.
