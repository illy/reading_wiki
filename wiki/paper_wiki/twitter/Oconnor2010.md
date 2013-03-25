We find that temporal smoothing is a critically important issue to support a successful model.

This comprises a roughly uniform sample of public messages, in the range of 100,000 to 7 million messages per day. (The primary source of variation is growth of Twitter itself; its message volume increased by a factor of 50 over this twoyear time period.)

Most Twitter users appear to live in the U.S., but we made no systematic attempt to identify user locations or even message language, though our analysis technique should largely ignore non-English messages.

There probably exist many further issues with this text sample; for example, the demographics and communication habits of the Twitter user population probably changed over this time period, which should be adjusted for given our desire to measure attitudes in the general population.

Two well-known surveys that measure U.S. consumer confidence are the Consumer Confidence Index from the Consumer Board, and the Index of Consumer Sentiment (ICS) from the Reuters/University of Michigan Surveys of Consumers. We use the latter,as it is more extensively studied in economics, having been conducted since the 1950s.

We also use another poll, the Gallup Organization’s “Economic Confidence” index,3 which is derived from answers to two questions that ask interviewees to to rate the overall economic health of the country.

*If there is enough training data, this could be formulated as a topic-sentiment model (Mei et al. 2007), in which the topics and sentiment of documents are jointly inferred*.

Our dataset, however, is asymmetric, with millions of text messages per day (and millions of distinct vocabulary items) but only a few hundred polling data points in each problem.

The signal-to-noise ratio is typical of information retrieval problems: we are only interested in information contained in a small fraction of all messages.

We therefore opt to use a transparent, deterministic approach based on prior linguistic knowledge, counting instances of positive-sentiment and negative-sentiment words in the context of a topic keyword

Positive and negative words are defined by the subjectivity lexicon from OpinionFinder, a word list containing about 1,600 and 1,200 words marked as positive and negative, respectively (Wilson, Wiebe, and Hoffmann 2005).6 We do not use the lexicon’s distinctions between weak and strong words.

A message is defined as positive if it contains any positive word, and negative if it contains any negative word. (This allows for messages to be both positive and negative.)

We only use messages containing a topic keyword, manually specified for each poll: •

1. For consumer confidence, we use economy, job, and jobs.

2. For presidential approval, we use Obama. 

3. For elections, we use Obama and Mccain.

In the earliest and smallest part of our dataset, the topic samples sometimes come out just several hundred messages per day; but by late 2008, there are thousands of messages per day for most datasets.

However, we are only interested in aggregate sentiment. A high error rate merely implies the sentiment detector is a noisy measurement instrument.

In order to derive a more consistent signal, and following the same methodology used in public opinion polling, we smooth the sentiment ratio with one of the simplest possible temporal smoothing techniques, a moving average over a window of the past k days:

**Smoothing is a critical issue.** It causes the sentiment ratio to respond more slowly to recent changes, thus forcing consistent behavior to appear over longer periods of time. Too much smoothing, of course, makes it impossible to see fine-grained changes to aggregate sentiment.

Several prior studies have estimated and made use of **aggregated text sentiment**.

We always consider the last day of the poll’s window to be the poll date, which is the earliest possible day that the information could actually be used

Also note that more smoothing increases the correlation: for Gallup, 7-, 15-, and 30-day windows peak at r = 71.6%, 76.3%, and 79.4% respectively.

We also found that the **topic frequencies** correlate with polls much more than the sentiment scores.

Furthermore, the Obama message volume substantially correlates to the poll numbers.

The elections setting may be structurally more complex than presidential job approval. In many of the tracking polls, people can choose to answer any Obama, McCain, undecided, not planning to vote, and third-party candidates.
