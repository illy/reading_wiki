#Chapter 2 Social media as corpora

Research into new media and the Internet from a communication perspective is diverse area that began to emerge **around 1996** (Tomasell et al. 209) (p15)

Studies of web-based discourse are a subdiscpline of **CMC** (computer-mediated communication). (p15)

Most often, these researcher will build their own corpora since CMC is *under-represented* in most available corpora. (p15)

A fundamental premise of corpus linguistics, equally applicable to web-based data as to more traditional data sources, is that corpora should be built according to carefully constructed selection criteria. (p15)

Unprocessed, the web is, however, not a corpus in the traditional sense, as it has not been built following selection criteria but instead has evolved as people have added, modified and deleted documents. (p16)

1. *Representativeness* is a concept used in statistics to refer to the extent to which a sample reflects the patterns in a larger population. (p16)

2. *Balance refers* to the isssue that a corpus should contain an equi-distributed sample of the range of possible genres, were is possible to catalogue genres with any kind of exhaustive way. (p16)

3. *Comparability* refers to the potential to compare different corpora by holding steady all parameters used for its construction except the one to be studied. (p16)

Internet data can be highly 'noisy' in the sense that methods for automating text collection will retrieve results that were not intended by the linguist. (p16) In particular, most web documents will contain formatting and metadata that need some kind of processing before the main text can be included in a plain text file corpus or in a relational database that also stores metadata about the texts (p 16).

###Time and streaming data

Time is of particular significance to online texts, particularly social media texts. Social media corpora are inevitably time-bound datasets, often shifting, networked assemblages of streaming data (p 16).

Streaming data is data that is produced as a sequence (p16). Streaming data produced with social media include unfolding status updates, such as microblog feeds or sequential blog posts, and feed of images and video (p 17).

Bernardini et al. (2006, p10) suggest four sense of web being as a corpus:

1. The web as corpus surrogate;

2. The web as corpus shop;

3. The web as corpus proper;

4. The mega-corpus/mini-web (p17)

Indeed, linguists fantasize abut a search engine that could filter internet data based on linguistic selection criteria and eliminate noise from the retrieved results (p17).

##Microposts as corpora

Microblogging data is episodic in nature, with posts added to user's stream over time, often a frequent intervals (p18).

In this way the data is temporally bound, and the period in time over which a corpus of microposts is collected has significant impact on the properties of the corpus and the ways in which it can be used (p18).

Contextual phenomena such as high profile events, crises, seasons and holidays all have an impact on the kind of online talk occurring via this media. (p18)

While contextual variables intervene in all corpora, the impact appears to be particularly concentrated in micropost corpora, particularly on simple measures, such as word-frequency lists. (p18)

The variation of language over time is itself of intrinsic interest and the objective of studies that work with traditional diachronic corpora. (p18)

Within the domain of social media research, time is of particular interest to researchers studying patterns of trending topics (Cataldi et al. 2010). (p18)

This magnitude of data permits quantitative claims about the properties of social media networks to be made, such as the finding that topology analysis of the follower/following relationship shows 'a non-power-law follower distribution, a short effective diameter, and low reciprocity, which all mark a deviation from known characteristics of human social networks' (Kwak et al. 2010, p 600). (p19)

These types of textual features mean that it is not possible to use tools such as off-the-shelf POS taggers on micropost corpora without significant training of the tagger. (p19)

###Non-standard orthography

Linguists can learn from the body of work in computational linguistics, where many of these types of text processing problems are encountered, when trying to automate various kinds of linguistic analyses. (p20)

###XML and escaped charcters

The corpus linguist trying to work with tweets that have been scraped from an internet feed may encounter the trivial but real problem of escaped special characters if the input text has not been 'unescaped' properly. (p20)

If one of these characters occurs in the raw text of a tweet, it must be 'escaped' by being represented by another set of characters. (p20)

###Emoticons and hashtags

Emoticons can pose a significant concordancing problem. Depending on the configuration of the concordance software used, some of the characters used in emoticons are not considered valid letters for that system and so will be filted out of the concordance. (p21)

###Abridge posts

The result is that some tweets appear in an abridged form in the corpus. Alternatively, the tweet may contain punctuation indicating that it continues in a subsequent tweet in the stream. (p21)

However, these types of tweets are relatively uncommon and may be filtered out of the corpus if the analyst can identify regular syntactic patterns with which they can be identified and removed. (p21)

###The HERMES corpus

Due to this randomization, much of the sequential nature of the streaming data is lost, and hence some other corpus collection strategy is required for exploring of exchanges between users. (p23)

Metadata about a tweet can at present be retrieved using the Twitter API. Linguists can make use of the API to build corpora taht contain different kinds of metadata retrieved from twitter. (p23)

High-level steps of collecting tweets:

1. Download all the unfiltered tweets;

2. Separate the content of the tweets from other metadata;

3. Convert any entity sequence;

4. Filter the text so that it contains only English tweets. (p24)

An in-depth tutorial on scraping data with the Twitter API is not provided here since the way Twitter allows developers to access its data and the extent of the granted access is changing as Twitter determines ways to generate income from the data. hence, any proposed method is likely to quickly become obsolete. (p24)
