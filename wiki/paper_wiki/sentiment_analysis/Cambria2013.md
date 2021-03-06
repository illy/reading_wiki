This review paper intends to give an overview on past, present, and future trends of sentiment analysis by delving into the evolution of different opinion mining systems from heuristics to discourse structure, from coarse- to fine-grained, from keyword-to concept-based analysis. More comprehensive surveys on sentiment analysis can be found in [1], [2], [3].

##Common sentiment analysis tasks

The basic task of opinion mining is polarity classification, that is, given an opinionated piece of text wherein it is assumed that the overall opinion is about one single issue or item, classify the opinion as falling under one of two opposing sentiment polarities.

Another instance of binary sentiment classification is agreement detection, that is, given a pair of text documents, deciding whether they should receive the same or differing sentiment-related labels.

###Topic detection

Typically, sentiment analysis is performed over on-topic document, e.g., on the result of a topic-based search engine.

However, several studies suggested that managing these two task jointly can be beneficial for the overall performances.

In this case, it is therefore necessary to identify the topics and separate the opinions associated with each of them.

While a topic is more likely to be emphasised by frequent occurrences of certain keywords, overall sentiment may not usually be highlighted through repeated use of the same terms.

##Evolution of opinion mining

Most of the existing approaches to opinion mining and sentiment analysis rely on **the extraction of a vector representing the most salient and important text features, which is later used for classification purposes**.

Some of the most commonly used features are _term frequency_ and _presence_.

The latter is a binary-valued feature vectors in which the entries _merely_ indicate whether a term occurs (value 1) or not (value 0) formed a more effective basis for review polarity classification.

Other term-based features are often added to the features vector. **Position** is one of these, in consideration of how the position of a token in a text unit can affect the way in which the token affects the sentiment of the text.

Also presence n-grams, typically bi-grams and trigrams, are often taken into account as useful features. Some methods also rely on the distance between terms.

Part of speech (POS) information (nouns, adjectives, adverbs, verbs, etc.) is also commonly exploited in general textual analysis as a basic form of word-sense disambiguation.

In other works, finally, the detection of sentiments was performed through selected phrases, which were chosen via a number of pre-specified POS patterns, most including an *adjective* or an *adverb*.

Moreover, most of the literature on sentiment analysis has focused on text written in English and, consequently, most of the resources developed, e.g., sentiment lexicons and corpora, are in English. Adapting such resources to other languages can be considered as a domain adaptation problem.

###From Heuristics to discourse structure

Several unsupervised learning approaches rely on the creation of a sentiment lexicon, which is later used to determine the degree of positivity (or subjectivity) of a text unit.

The crucial component is, therefore, the creation of the lexicon via the unsupervised labelling of words or phrases with their sentiment polarity or subjectivity [1].

Because such approaches lacked the capability of detecting novel expressions of sentiment, later works focussed on propagating the valence of seed words (for which the polarity is known) to terms that co-occur with them in general text (or in dictionary glosses), or to synonyms and words that co-occur with them in other WordNet-defined relations.

Regression techniques are often employed for the prediction of the degree of positivity in opinionated documents such as product reviews.

Regression, in fact, allows to implicitly model similarity relationships between classes that correspond to points on a scale, such as the number of ‘stars’ given by a reviewer [1]

Modelling discourse structure, such as twists and turns in documents, contributes to a more effective overall sentiment labelling.

More recent studies have underlined that position is particularly relevant in the context of sentiment summarisation.

In particular, in contrast to topic-based text summarisation, where the incipits of articles usually serve as a strong baseline, the last n sentences of a review have been shown to serve as a much better summary of the overall sentiment of the document, and to be almost as good as the n (automatically-computed) most subjective sentences [7].

###From coarse- to fine-grained analysis

The evolution of research works in the field of opinion mining and sentiment analysis can be seen not only in the use of more and more sophisticated techniques, but also in the different depths of analysis adopted.

However, opinions and sentiments do not occur only at document-level, nor are they limited to a single valence or target.

Contrary or complementary attitudes toward the same topic or multiple topics can be present across the span of a document

Hence, later works adopted a segment-level opinion analysis aiming to distinguish sentimental from non- sentimental sections, e.g., by using graph-based techniques for segmenting sections of a document on the basis of their subjectivity [7], or by performing a classification based on some fixed syntactic phrases that are likely to be used to express opinions [11], or by bootstrapping using a small set of seed opinion words and a knowledge base such as WordNet [12].

In other works, text analysis granularity has been taken down to sentence-level, e.g., by using presence of opinion-bearing lexical items (single words or n-grams) to detect subjective sentences [13], or by using semantic frames for identifying the topics (or targets) of sentiment [14].

Even sentence-level approaches, however, often fail to correctly discover sentiments on entities and/or their aspects. To this end, other works adopt an aspect-level approach [15], [16], [17], which is based on the idea that an opinion consists of targets and sentiments associated to them.

Based on this level of analysis, a structured summary of opinions about entities and their aspects can be produced and, hence, more accurate statistics about such aspects can be drawn.

###From keywords to concepts

The evolution of sentiment analysis research, finally, can be studied in terms of the different tokens, or building blocks, of the analysis, and the implicit information associated with them. In this sense, existing approaches can be grouped into four main categories: keyword spotting, lexical affinity, statistical methods, and concept-based techniques.

Keyword spotting is the most naïve approach and probably also the most popular because of its accessibility and economy. Text is classified into affect categories based on the presence of fairly unambiguous affect words like ‘happy’, ‘sad’, ‘afraid’, and ‘bored’.

The weaknesses of this approach lie in two areas: poor recognition of affect when negation is involved and reliance on surface features. About its first weakness, while the approach can correctly classify the sentence “today was a happy day” as being happy, it is likely to fail on a sentence like “today wasn’t a happy day at all”. About its second weakness, the approach relies on the presence of obvious affect words which are only surface features of the prose.

Lexical affinity is slightly more sophisticated than keyword spotting as, rather than simply detecting obvious affect words, it assigns arbitrary words a probabilistic ‘affinity’ for a particular emotion.

Though often outperforming pure keyword spotting, there are two main problems with the approach. First, lexical affinity, operating solely on the word-level, can easily be tricked by sentences like “I avoided an accident" (negation) and “I met my girlfriend by accident” (other word senses). Second, lexical affinity probabilities are often biased toward text of a particular genre, dictated by the source of the linguistic corpora.

Statistical methods, such as Bayesian inference and support vector machines, have been popular for affect classification of texts and have been used by researchers on projects such as Pang’s movie review classifier [9] and many others [10], [15], [24].

However, statistical methods are generally semantically weak, meaning that, with the exception of obvious affect keywords, other lexical or co-occurrence elements in a statistical model have little predictive value individually.

As a result, statistical text classifiers only work with acceptable accuracy when given a sufficiently large text input.

So, while these methods may be able to affectively classify user’s text on the page- or paragraph-level, they do not work well on smaller text units such as sentences or clauses.

Concept-based approaches, in turn, focus on a semantic analysis of text through the use of web ontologies [25] or semantic networks [26], [27], which allow grasping the conceptual and affective information associated with natural language opinions.

Differently from purely syntactical techniques, in fact, concept-based approaches are able to detect also sentiments that are expressed in a subtle manner, e.g., through the analysis of concepts that do not explicitly convey any emotion, but which are implicitly linked to other concepts that do so.

The validity of concept-based approaches mainly depends on the depth and breadth of the employed knowledge bases. Without a comprehensive resource that encompasses human knowledge, in fact, it is not easy for an opinion mining system to grasp the semantics associated with natural language text.

Another limitation of semantic approaches is in the typicality of their knowledge bases.

Knowledge representation, in fact, is usually strictly defined and does not allow handling different concept nuances, as the inference of semantic and affective features associated with concepts is bounded by the fixed/flat representation.

##Multimodal sentiment analysis

A larger body of literature on how to handle linguistic, acoustic, and potentially also video information exists in the related field of affect analysis.

Yet, linguistic information is based on the transcript of the spoken content rather than on automatic speech recognition output.

Overall, multimodal sentiment analysis is thus yet to be seen more frequently. It certainly holds great promises from both, an application point of view for example when textual- transcripts are not available, and a performance point of view owing to synergy effects and fail-safeness.

##Discussion

In recent years, sentiment analysis research is gradually setting itself as a field in between mere NLP and natural language understanding.

Following such a trend, we envision the future of sentiment analysis research to move towards a content-, concept-, and context-based analysis of natural language text, supported by time-efficient parsing techniques suitable for big social data analysis [32].

The processing at content/syntactic-level will still be heavily needed for the collection of opinions over the Web, while filtering out non-opinionated user-generated contents (subjectivity detection), and for accordingly balancing the weight/trustworthiness of such opinions with respect to their source.

The analysis at concept/semantic-level, instead, is intended to infer the semantic and affective information associated with natural language opinions and, hence, to enable a comparative fine-grained feature-based sentiment analysis.

The context/intent-level analysis, finally, will ensure that all the gathered opinions are relevant for the specific user.

In the Era of Social Context, where intelligent system will have access to a great deal of personal identities and social relationships, opinion mining will be tailored to each user’s preferences and intent.

##Conclusion

Opinion mining and sentiment analysis are research fields inextricably bound to the affective sciences that attempt to understand human emotions."
