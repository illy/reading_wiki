Investors’ emotions can affect the way they process and react to new information which explains why their decisions in some circumstances can depart from the rational behavior that is generally assumed.

If emotions can affect decisions at the individual level it can be argued that investors’ collective sentiment can affect market returns and their dynamics.

While a short time period is considered (32 days), we found scarce evidence that sentiment indicators can explain these stock returns.

However, interesting results were obtained when measuring the value of using posting volume for fitting trading volume and, in particular, volatility.

The community of users that utilizes these services to communicate and share information about stock market issues has grown and is potentially more representative of all investors.

Microblogging data is readily available at low cost permitting a faster and less expensive creation of indicators, compared to traditional sources (e.g. large-scale surveys) and can also contain new information that is not present in historical quantitative financial data.

The small size of the message (maximum 140 characters) and the usage of cashtags (a hashtag identifier for financial stocks) can make it a less noisy source of data.

Users post very frequently, reacting to events in realtime.

Our study aims at testing whether Twitter data sentiment variables have any correlation with stock market variables and if they are related to stock market dynamics.

Five different popular lexical resources are compared and two novel lexicons are proposed for extracting a sentiment indicator, emoticon based (e.g. “:)”) and ALL, which merges all six previous lexicons.

Cashtags are composed by the company ticker preceded by the “$” symbol. These symbols are commonly used by the investor community in discussions related to the respective company. Concentrating on only these messages reduces the amount of irrelevant messages, resulting in a less noisy data set.

We also explore the use of posting volume and their value in modeling the volume and volatility financial indicators.

Adjusted close price is the official closing price adjusted for capital actions and dividends.

Volatility (σt, for day t) is a measure of total risk associated with a given investment.

5. SentiWordNet (SWN) 3.0 [2] – a lexical resource that assigns, to each synset of WordNet, a positivity and a negativity score, varying from 0 to 1. A synset is a group of word or expressions that are semantically equivalent in some context. Each word may appear multiple times with different scores in this lexical resource because it can belong to various synsets of Wordnet.

The former is based on the simpler analysis of positive (”:-)’ or “:)”) and negative (”:-(” or “:(” ) emoticons. If a positive emoticon is present in the text, then we add 1 to the positivity score and similarly we increase (+1) the negative score if a negative emoticon is detected.

1. Harvard General Inquirer (GI) [17] – This resource comprise 11788 words classified in 182 categories.

The latter lexicon merges all 6 previous lexicons (GI, OL, MSOL, MPQA, SWN, Emoticons) by producing a union of all positive, negative and neutral score rules.

These categories come from four sources: the Harvard IV-4 dictionary; the Lasswell value dictionary; categories recently constructed, and "marker" categories containing syntactic and semantic markers.

in this paper we propose and explore two simple and global sentiment analysis approaches. The rational for this choice is that the proposed approaches are very easy to implement and test.

2. Opinion Lexicon (OL) [8] – This lexicon contains two lists of positive and negative opinion words for English, including misspelled words that appear frequently in social media contents.

3. Macquarie Semantic Orientation Lexicon (MSOL) [10]. – classifies more than 75 thousand n-grams, as positive or negative.

4. MPQA Subjectivity Lexicon (MPQA) [20] – this lexicon is part of OpinionFinder, a system that identifies various aspects of subjectivity (e.g. sources of opinion, sentiment expressions) in text. MPQA Subjectivity Lexicon has more than 8000 entries with the following attributes:

In the first approach (S1), we count the daily total number of words that are considered positive and negative by each lexical resource (total of two sentiment variables).

Regarding the second sentiment approach (S2), we classify each individual tweet, by considering the “positive” and “negative” words that it contains. A message is considered: positive, if the number of “positive” words is higher than the number of “negative” words; negative, if the number of “negative” words is higher than the number of “positive” words; and neutral, if the number of both word polarity types is equal.


However, interesting results were obtained when measuring the value of using posting volume for fitting trading volume and, in particular, volatility.

The community of users that utilizes these services to communicate and share information about stock market issues has grown and is potentially more representative of all investors.

Microblogging data is readily available at low cost permitting a faster and less expensive creation of indicators, compared to traditional sources (

The small size of the message (

Users post very frequently, reacting to events in realtime.

Our study aims at testing whether Twitter data sentiment variables have any correlation with stock market variables and if they are related to stock market dynamics.

Five different popular lexical resources are compared and two novel lexicons are proposed for extracting a sentiment indicator, emoticon based (

Cashtags are composed by the company ticker preceded by the “$” symbol. These symbols are commonly used by the investor community in discussions related to the respective company. Concentrating on only these messages reduces the amount of irrelevant messages, resulting in a less noisy data set.

We also explore the use of posting volume and their value in modeling the volume and volatility financial indicators.

Adjusted close price is the official closing price adjusted for capital actions and dividends.

Volatility (

5. SentiWordNet (

The former is based on the simpler analysis of positive (

1. Harvard General Inquirer ())

The latter lexicon merges all 6 previous lexicons ())

These categories come from four sources: the Harvard IV-4 dictionary; the Lasswell value dictionary; categories recently constructed, and "))

in this paper we propose and explore two simple and global sentiment analysis approaches. The rational for this choice is that the proposed approaches are very easy to implement and test.

2. Opinion Lexicon ())

3. Macquarie Semantic Orientation Lexicon ())

4. MPQA Subjectivity Lexicon ())

In the first approach ())

Regarding the second sentiment approach ())

Overall, the baseline method shows an almost null effect in estimating the next day returns, with R2 values close to zero.

Also, there is no added value when joining the baseline input to the best sentiment method result ())

Given that, in general, better results were achieved when compared with the trading volume and returns regressions, we highlight the results that are better than the 0.5 threshold, for both R2 and RAE metrics.

Confirming the scarce evidence of return predictability [))

However, we found some evidence that Twitter posting volume is relevant for modeling the next day trading volume.

Moreover, the same source of data can substantially improve the modeling of volatility, provided it is used in conjunction with the previous day volatility.

C. Oh and O. Sheng. Investigating predictive power of stock micro blog sentiment in forecasting future stock price directional movement. ICIS 2011 Proceedings, 2011.

R. Peterson. Affect and financial decision-making: How neuroscience can inform market participants. The Journal of Behavioral Finance, 8())

R. Schumaker and H. Chen. Textual analysis of stock market prediction using breaking financial news: The azfin text system. ACM Transactions on Information Systems ())
Overall, the baseline method shows an almost null effect in estimating the next day returns, with R2 values close to zero.

Also, there is no added value when joining the baseline input to the best sentiment method result (best ⊕rt−1).

Given that, in general, better results were achieved when compared with the trading volume and returns regressions, we highlight the results that are better than the 0.5 threshold, for both R2 and RAE metrics.

Confirming the scarce evidence of return predictability [18], the explored sentiment indicators did not, in general, provide significant information about the following day return.

However, we found some evidence that Twitter posting volume is relevant for modeling the next day trading volume.

Moreover, the same source of data can substantially improve the modeling of volatility, provided it is used in conjunction with the previous day volatility.
