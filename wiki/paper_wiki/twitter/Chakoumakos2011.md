Identical SVM models built on this combination set of features showed an average improvement of 35.4 percentage-points over economic analysis features alone, enough to make an options-straddling strategy profitable for some stocks in the portfolio.

Most public trading strategies use economic models of individual stocks to predict days when a stock will have a “major price difference” (MPD) event (i.e., when the opening price of a stock changes by >= 2% of its previous opening value).

We expand this work to focus on a specific small portfolio of stocks; we further expand it to become more directly applicable to an options-straddling strategy by predicting when MPD events will occur for all stocks in our portfolio, instead of predicting their future closing direction.

We chose a portfolio of 10 stocks from the NASDAQ stock exchange to test our classification. Based on previous work [11], which suggests that quantitative analysis of public sentiment is most useful with a large corpus of Tweets, we selected consumer technology manufacturers and consumer retailers - the types of companies that we thought would be frequently discussed on Twitter: ATVI, ADBE, AAPL, DELL, ERTS, GRMN, MAT, NFLX, RIMM, and URBN.

Because an options-straddle trading strategy necessitates trading only on days when there will be a MPD event, accuracy is not a meaningful statistic — we only need high precision when predicting MPD events.

For that reason, our primary metric of success was high precision and reasonable recall when predicting MPD events.

These results are within a 10% margin of error of the results found in Bollen, which used a self-organizing fuzzy neural network.

This result suggested the applicability of non-linear SVMs to the problem of predicting stock events, a heartening first step.

We constructed 149 features based on standard technical analysis methods [8] in an attempt to provide as much information as possible based on the simple data available to us.

We found that back-propagation neural networks did not result in good fits in general, with high bias on the training dataset. Based on the success with SVM modeling, the rest of the models we built and tested used these choices of parameters.

The results show that none of the features are particularly predictive of MPD events, and those that are primarily rely upon long-term trends (such as a stock's price opening above its 10-day average).

We hypothesize that these results show that a baseline classifier is good at predicting the sorts of long-term gains that might not be reflected in Twitter sentiment, which could form the basis for an excellent supporting classifier.

The average precision in predicting MPD events is 0.297 (max 0.500), much too low to create an effective trading strategy alone.

We started by only considering those tweets that contained the stock ticker symbol of the company (the “TICKER” datasets), but found that most of the stocks in our portfolio had < 100 tweets/day using that criterion (Table 2)

We then tokenized each tweet using Potts' sentiment and twitter aware tokenizer since it is better suited than other tokenizers for the type of content that appears on Twitter [3].

Unfortunately, GPOMS is not publicly available, so we attempted to recreate it based on available literature.

As with GPOMS, we built upon the Profile of Mood States (POMS) psychological rating scale to measure 6 mood dimensions: Calm, Alert, Sure, Vital, Kind, & Happy.

The original lexicon for POMS uses 65 adjectives to measure mood [6]. We expanded the lexicon to 626 terms using Wordnet by mapping each adjective to parent synsets that reflect the sentiment of the adjective [7].

All words in the synset families were stemmed and included in the POMS-Expanded set.

We hypothesized that the public mood was less indicative of individual stock performance than it is of the market as a whole; for that reason, we sought a more general method that could utilize a larger lexicon to predict MPD events.

Our portfolio showed unfortunately low average results of 0.211 precision and 0.238 recall.

Data further indicated that the classifier had high variance, as testing on the training set resulted in an average of 0.9956 precision and 0.5492 recall. We therefore elected to add more training data, increasing the corpus to the “terms” datasets.

We determined seven categories of words and manually generated example words in each category (Table 4). We then counted the frequency of these words occurring in the previous day. This method performed poorly when classified by our tuned SVM.

SVM classifiers using a combination of economic data and features gleaned from Twitter feeds predict MPD events with higher precision than classifiers based on economic data alone.

Over a portfolio of 10 consumer-technology companies, combination classifiers improved the precision of MPD prediction by an average of 35.32 percentage points.

While the average precision is 0.402, too low to create a profitable options-straddle trading strategy over the entire portfolio, the two stocks with the highest Twitter comment volume show precisions of 0.630 and 0.778;

###Summary

Chakoumakos, Trusheim and Yendluri (2012) use an Identical SVM model to detect the sentimental information in "a specific small portfolio of stocks". Based on the "major price difference" (MPD) options-straddle trading strategy, the precision overweigh accuracy and recall. Also they mention that if only the tweets containing the ticker symbol are considered, then the data will be very sparse, so they include tweet contains more related information, for example, main products, and names of main figures. Using Potts' sentiment and twitter aware tokenizer to process the data brings the best result. Derived from the unpolished GPOMS, they build a similar sentiment system POMS consist of six dimensions: calm, alert, sure, vital, kind and happy, which is based on a lexicon of 626 words from Wordnet. However, the result of the POMS is not optimised due to the scale of the object, and the following results show that expanding data can improve the classifier performance. Some companies are more discussed on Twitter, so the prediction on them are more accurate. Moreover, with more relevant information such as "features gleaned from Twitter feeds" the prediction can achieve a better result than that with market data alone.
