Main fields of research in Sentiment analysis are Subjectivity Detection, Sentiment Prediction, Aspect Based Sentiment Summarization, Text Summarization for Opinions, Contrastive Viewpoint Summarization, Product Feature Extraction, detecting opinion spam. Subjectivity Detection is a task of determining whether text is opinionated or not.

Sentiment Prediction is about predicting the polarity of text whether it is positive or negative.

Aspect Based Sentiment Summarization provides sentiment summary in the form of star ratings or scores of features.

Text Summarization generates a few sentences that summarize the reviews of a product.

Contrastive Viewpoint Summarization puts an emphasis on contradicting opinions.

Product Feature Extraction is a task that extracts the product features from its review.

Detecting opinion spam is concern with identifying fake or bogus opinion from reviews.

The objective of this paper is to discover the concept of Sentiment Analysis in the field of Natural Language Processing and explore its applications and challenges in this field.

Depending on the task at hand and perspective of the person doing the sentiment analysis, the approach can be discourse-driven, relationship-driven, language-model driven, or keyword-driven.

Supervised methods have shown better performance than the unsupervised methods.

The main task in this approach is the construction of word lexicons that indicate positive class or negative class. The sentiment values of the words in the lexicon are determined prior to the sentiment analysis work.

SENTIWORDNET 3.0 is a publicly available lexical resource explicitly devised for supporting sentiment classification and opinion mining applications

Cui et al. [12] have argued that SVMs are more appropriate for sentiment classification because they can better perform when review contains both positive and negative words.

However, when the set of training data is small, a Naïve Bayes classifier might be more appropriate because SVMs requires a large set of data in order to build a high-quality classifier.

One of the most important tasks in sentiment classification is selecting an appropriate set of features.

In this approach the n-gram language models are built. Presence or frequency of n-grams can be used. In text classification, frequency of n-grams gives better results.

Term presence and their frequency: These features include uni-grams or n-grams and their frequency or presence. These features have been widely and successfully used in sentiment classification.

Part of speech information: Part-of-speech is used to disambiguate sense which in turn is used to guide feature selection [11]. Part-ofspeech tagging is useful for identifying adjectives and adverbs in the sentences which identify the opinion words and nouns which are used to identify features of the products.

In many reviews, the overall sentiment is usually expressed at the end of the text [1].

In this discourse-driven approach the sentiment of the whole review is obtained by determining sentiment between different discourse components and the discourse relations that exist between them.

Negation is also an important feature to take into account since it has the potential of reversing a sentiment [11].

Opinion words and phrases such as “like”, “nice”, “hate”, “I'd suggest that...” are words and phrases that express positive or negative opinions. The main approaches to identify the semantic orientation (positive or negative) or polarity of an opinion words are statistical-based or lexicon-based.

The main limitation of supervised learning is that it is dependent on the amount and quality of the training data and may fail when training data are insufficient.

In unsupervised technique, classification is done by comparing the features of a given text against word lexicons whose sentiment values are determined prior to their use.

The most prominent work done using unsupervised methods for opinion mining and sentiment detection is by Turney [2]. He uses “poor” and “excellent” seed words as they are appear more in web for calculating the semantic orientation of phrases, where orientation is measured by pointwise mutual information.

Ting-Chun Peng and Chia-Chun Shih [13] uses part-of-speech(POS) patterns for extracting the sentiment phrases of each review, they used unknown sentiment phrase as a query term and get top-N relevant phrases from a search engine. Next, sentiments of unknown sentiment phrases are computed based on the sentiments of nearby known relevant phrase using lexicons.

Sarcastic or ironic sentences can be hard to identify which can lead to erroneous opinion mining.

The accuracy of sentiment classification can be influenced by the domain of the items to which it is applied. The reason is that the there are many words whose meaning changes from domain to domain

Text classification has many classes as there are many topics but sentiment analysis has only three classes.

Many times text contains different words having same meaning. So such word should be identified and group together for accurate classification.

Coreference resolution may be useful for the topic/aspect based sentiment analysis. Coreference resolution may improve the accuracy of opinion mining.

Negation handling is a difficult task in sentiment analysis as it reverses the polarity. Negation also expresses by sarcasm and implicit sentences which doesn’t contain any negative words.

If the opinion provided services contain large number of spams, they will affect the users’ experience. Furthermore, if the user is cheated by the provided opinion, he will never use the system again.

Although, some of the algorithms have been used in sentiment analysis gives good results, but still no algorithm can resolve all the challenges.

Most of the researchers reported that Support Vector Machines (SVM) has high accuracy than other algorithms, but it also has limitations.

It is found that sentiment classification is domain dependent.
