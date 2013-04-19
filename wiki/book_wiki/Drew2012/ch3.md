CHAPTER 3

This line was called a separating hyperplane, but from now on we’ll use the term “decision boundary,” because we’ll be working with data that can’t be classified properly using only straight lines.

One approach in particular that we’ll focus on later is called the kernel trick, which has the remarkable property of allowing us to work with much more sophisticated decision boundaries at almost no additional computational cost.

These examples consist of a label, which we’ll also call a class or type, and a series of measured variables that describe each example. We’ll call these measurements features or predictors

As this is a recurring problem, there is a standard graphical solution: we simply add random noise to the values before we plot. This noise will “separate out” the points to reduce the amount of over-plotting. This addition of noise is called jittering, and is very easy to produce in `ggplot2` (see Figure 3-2).

At its core, text classification is a 20th-century application of the 18th-century concept of conditional probability.

A conditional probability is the likelihood of observing one thing given some other thing that we already know about.

The text classification algorithm we’re going to use in this chapter, called the Naive Bayes classifier, looks for differences of this sort by searching through text for words that are either (a) noticeably more likely to occur in spam messages, or (b) noticeably more likely to occur in ham messages.

Ultimately, our text classifier formalizes this intuition by computing (a) the probability of seeing the exact contents of an email conditioned on the email being assumed to be spam, and (b) the probability of seeing the same email’s contents conditioned on the email being assumed to be ham.

How much more likely a message needs to be to merit being labeled spam depends upon an additional piece of information: the base rate of seeing spam messages. This base rate information is usually called the prior.

To compute the probability of an email, we will assume that the occurrence counts for every word can be estimated in isolation from all of the other words. For- mally, this amounts to an assumption often referred to as statistical independence.

When we make this assumption without being certain that it’s correct, we say that our model is naive. Because we will also make use of base rate information about emails being spam, the model will be also called a Bayes model—in homage to the 18th- century mathematician who first described conditional probabilities.

This is not to say that one should always ignore the header or any other information. In fact, all sophisticated modern spam filters utilize information contained in email message headers, such as whether portions of it appear to have been forged, whether the message is from a known spammer, or whether there are bits missing.

The R language performs file I/O in a very similar way to many other programming languages.

The function shown here takes a file path as a string and opens that file in rt mode, which stands for read as text.

Note that we have to pass an anonymous function to sapply in order to concatenate the filename with the appropriate directory path using the paste function.

A huge advantage of the `tm` package is that much of the heavy lifting needed to clean and normalize the text is hidden from view.

One way of quantifying the frequency of terms in our spam email is to construct a term document matrix (TDM).

As the name suggests, a TDM is an N×M matrix in which the terms found among all of the documents in a given corpus define the rows and all of the documents in the corpus define the columns. The [i, j] cell of this matrix corre- sponds to the number of times term i was found in document j.

The `tm` package allows you to construct a corpus in several ways. In our case, we will construct the corpus from a vector of emails, so we will use the VectorSource function.

As is often the case when working with tm, once we have loaded our source text, we will use the Corpus function in conjunction with VectorSource to create a corpus object.

First, we set stopwords=TRUE, which tells `tm` to remove 488 common English stop words from all of the documents. To see the list, type stopwords() at the R console. Next, we set removePunctuation and removeNumbers to TRUE, which are fairly self-explanatory and are used to reduce the noise associated with these characters—especially because many of our documents contain HTML tags. Finally, we set minDocFreq=2, which will ensure that only terms appearing more than once in the corpus will end up in the rows of the TDM.

As such, it is good practice to ensure that our training data reflects our assumptions. We only have 500 spam messages, so we will limit or ham training set to 500 messages as well.

If a message contains just one or two terms strongly associated with spam, it will take a lot of nonspam words for the message to be classified as ham.

To calculate the probability that an email message is spam or ham, we will need to find the terms that are common between the training data and the message in question. We can then use the probabilities associated with these terms to calculate the conditional probability that a message is of the training data’s type.

To calculate the conditional probability of a message, we combine the probabilities of each term in the training data by taking their product.

Researchers have come up with many clever ways of trying to get around this problem, such as drawing a random probability from some distribution or using natural language processing (NLP) techniques to estimate the “spamminess” of a term given its context.

For our purposes, we will use a very simple rule: assign a very small probability to terms that are not in the training set.

Finally, because we are assuming that all emails are equally likely to be ham or spam, we set our default prior belief that an email is of some type to 50%.

The final step of the classification is to determine whether any of the words in the email message are present in the training set, and if so, we use them to calculate the probability that this message is of the class in question.

We know that all of these emails are ham, so ideally our classifier will assign a higher probability of being ham to all of these messages.

We also know, however, that hard ham messages are “hard” to classify because they contain terms that are also associated with spam.

This is done because our classifier compares the two predicted probabilities and determines the email’s type based on whether the probability of being spam is greater than that of ham.

First, there are many hard ham messages that have a positive probability of being spam but a near-zero probability of being ham.

Second, there are both easy and hard ham messages that have a much higher relative probability of being ham.

In practice, however, we know that this relationship is actually much closer to 80%–20% ham-to-spam.

By doing so, we are explicitly trading off false positives for improvement in false negatives. This is an excellent example of why model speci- fication is critical, and how each assumption and feature choice can affect all results.
