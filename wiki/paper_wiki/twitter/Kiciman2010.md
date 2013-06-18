With the eventual goal of building more accurate and less expensive models of microblog streams, this paper investi- gates the degree to which language variance is related to the metadata of microblog content.

We hypothesize that if a strong relationship exists between metadata features and language then we can use this metadata as a trivial clas- sifier to match individual messages with specialized, more accurate language models.

For each metadata fea- ture we studied, we divided the English portion of the corpus into subsets based on its feature value, and used each subset to learn an n-gram model.

For example, as might be expected, the coarse location of users (e.g., their timezone) seems to have a strong relation to their aggregate observed language.

The recognition of such distinct classes of users and messag- ing activities leads us to suspect distinct language styles are in use on Twitter.

The language models are smoothed using Modified Kneser-Ney smoothing.

We believe that such statistical mod- eling of message content will become an important tool in future research, as well as a foundation for information re- trieval and other applications built atop microblogging ser- vices.

It is important to note that our analysis only serves to identify correlations between individual features and lan- guage di↵erences. In particular, our algorithm does not ac- count for potential correlations among features themselves.

First, the likelihood of location names is strongly associated with timezone.

Secondly, we see variance in the probability of words associated with topics of a geographic nature.

Finally, we see dialect variance, such as the spelling variations (“favourite” vs. “favorite”), and colloquialisms such as the use of ‘gon’ instead of ‘going to’.

Despite ease of global communication in Twitter, we see a strong correlation between such colloquial usage and geography as represented by time zone.
As shown in Figure 3, we see that while there are notice- able di↵erences in language among the groupings of messages whose authors had less than 10, 100, and 1000 followers, the largest language di↵erence occurs among messages whose authors had more than 1000 followers.

There is mixed evidence of a similar shift in the usage of 2nd-person words such as ‘you’ or ‘your’.

D. Boyd, S. Golder, and G. Lotan. Tweet, tweet, retweet: Conversational aspects of retweeting on twitter. In HICSS ’10: Proceedings of the 2010 43rd Hawaii International Conference on System Sciences, pages 1–10, Washington, DC, USA, 2010. IEEE Computer Society.
