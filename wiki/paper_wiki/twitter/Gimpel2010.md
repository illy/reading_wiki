One of the most fundamental parts of the linguistic pipeline is part-of-speech (POS) tagging, a basic form of syntactic analysis which has countless applications in NLP.

Tagging performance degrades on out-of-domain data, and Twitter poses additional challenges due to the conversational nature of the text, the lack of conventional orthography, and 140-character limit of each message (“tweet”).

This was made possible by two things:

1.an annotation scheme that fits the unique characteristics of our data and provides an appropriate level of linguistic detail;

2.a feature set that captures Twitter-specific properties and exploits existing resources such as tag dictionaries and phonetic normalization.

Next, we obtained a random sample of mostly American English1 tweets from October 27, 2010, automatically tokenized them using a Twitter tokenizer (O’Connor et al., 2010b),2 and pre-tagged them using the WSJ-trained Stanford POS Tagger (Toutanova et al., 2003) in order to speed up manual annotation.

 >Heuristics were used to mark tokens belonging to special Twitter categories, which took precedence over the Stanford tags.

The annotation process uncovered several situations for which our tagset, annotation guidelines, and tokenization rules were deficient or ambiguous.

We set out to develop a POS inventory for Twitter that would be intuitive and informative—while at the same time simple to learn and apply—so as to maximize tagging consistency within and across annotators.

http://github.com/brendano/tweetmotif

Our first round of annotation revealed that, due to nonstandard spelling conventions, tokenizing under a traditional scheme would be much more difficultthan for Standard English text.

 >For example, apostrophes are often omitted, and there are frequently words like ima (short for I’m gonna) that cut across traditional POS categories.

Therefore, we opted not to split contractions or possessives, as is common in English corpus preprocessing; rather, we introduced four new tags for combined forms: {nominal, proper noun} × {verb, possessive}.5

Figure 2 shows where tags in our data tend to occur relative to the middle word of the tweet.

 >We see that Twitter-specific tags have strong positional preferences: at-mentions (@) and Twitter discourse markers (~) tend to occur towards the beginning of messages, whereas URLs (U), emoticons (E), and categorizing hashtags (#) tend to occur near the end.

Our tagger is a conditional random field (CRF; Lafferty et al., 2001 http://www.cis.upenn.edu/~pereira/papers/crf.pdf), enabling the incorporation of arbitrary local features in a log-linear model.

 >Our base features include:

 >1.a feature for each word type,

 >2.a set of features that check whether the word contains digits or hyphens,
 
 >3.suffix features up to length 3,

 >4.features looking at capitalization patterns in the word.

Microbloggers are inconsistent in their use of capitalization, so we compiled gazetteers of tokens which are frequently capitalized.

Unlike previous work that uses tag dictionaries as hard constraints, we use them as soft constraints since we expect lexical coverage to be poor and the Twitter dialect of English to vary significantly from the PTB domains.

Since Twitter includes many alternate spellings of words, we used the **Metaphone algorithm** (Philips, 1990 http://en.wikipedia.org/wiki/Metaphone) to create a coarse phonetic normalization of words to simpler keys.

 >We include two types of features.

 >1.we use the Metaphone key for the current token, complementing the base model’s word features.

 >2.we use a feature indicating whether a tag is the most frequent tag for PTB words having the same Metaphone key as the current token.

Instead, we retrained it on our labeled data, using a standard set of features: words within a 5-word window, word shapes in a 3-word window, and up to length-3 prefixes, length-3 suffixes, and prefix/suffix pairs.1

Substantial challenges remain; for example, despite the NAMES feature, the system struggles to identify proper nouns with nonstandard capitalization.

The system also struggles with the miscellaneous category (G), which covers many rare tokens, including obscure symbols and artifacts of tokenization errors.

http://www.ark.cs.cmu.edu/TweetNLP.

###Summary

The linguistic features of tweet bring challenges to analysis, for instance, POS-tagging is rather difficult. Gimpel et al's (2011) develop a specific POS tag set for tweets based on CRT algorithm and metaphone algorithm. Moreover, they try to correct wrong capitalizations in tweets by compiling gazetteers, and use traditional tag dictionary as soft constraints to implement the annotation. Their result shows a 90% accuracy of tagging, and also the common tag position relating to the middle word of tweet. However, some challenges still remain: proper nouns with nonstandard capitalisation cannot be well recognised, and the G category which involving many abbreviations cannot be well classified.
