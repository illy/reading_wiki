The psycholinguistic theory of communication accommodation accounts for the general observation that participants in conversations tend to converge to one another's communicative behavior: they coordinate in a variety of dimensions including choice of words, syntax, utterance length, pitch and gestures.

###Introduction

These findings suggest that the communicative behavior of conversational partners are “patterned and coordinated, like a dance” [32]. However, up to now this “dance” was exclusively studied in controlled laboratory experiments or through small scale studies. The work presented here demonstrates for the first time the robustness of accommodation theory in a large scale, real world environment: Twitter.

It is estimated that a quarter of all its users hold conversations with other users on this platform [22] and **that around 37% of all tweets are conversational** [36].

One of the dimensions on which people were shown to accommodate is linguistic style [32, 39, 14], where style denotes the components of language that are unrelated to content: how things are said as opposed to what is said.

This is a rather important dimension, since, even though only 0.05% of the English vocabulary is composed of style words (such as articles and prepositions), an estimated 55% of all words people employ are style words [38].

Linguistic style has also been **central** to a series of NLP applications like authorship attribution and forensic linguistics [30, 41, 18, 23], gender detection [25, 31, 17] and personality type detection [1].

Linguistic style is also known to be, for the most part, generated and processed nonconsciously [26], and thus a suitable vehicle for studying the phenomenon of accommodation, which itself is assumed to occur nonconsciously.

Previous work on accommodation relied mainly on simple correlation-based measures.

The main desirables from such a framework are:

1.Comparability: the effects of accommodation on different components of style should be comparable.

2.Expressivity: the framework should be expressive enough to permit the evaluation of particular properties of accommodation (discussed in Section 2). 

3.Purity: accommodation should not be confounded with other phenomena.

The last of these desirables is probably the hardest to achieve and thus deserves some discussion here. The main challenge is to distinguish accommodation from the effects of homophily: people that converse are likely to employ a similar linguistic style simply because they know each other.

Another advantage of the proposed framework is that a new concept of stylistic influence emerges naturally: given two conversational partners, one can influence the style of the other more than vice-grained version of the concept of symmetry of accommodation proposed in the psycholinguisic literature [12]: accommodation can occur symmetrically when both participants in a conversation accommodate to each other or asymmetrically when only one accommodates.

We are able to show that imbalance in stylistic influence between Twitter users is preponderant and that symmetry in accommodation is dependent on the stylistic dimension (Figure 4); for example, users are more likely to accommodate symmetrically on the use of 1st person singular pronouns but to accommodate asymmetrically on the use of prepositions.

This is the first time such a rich complexity of the accommodation phenomenon is revealed.

For example, it was hypothesized that a person of lower status will try to accommodate to a person of higher status in order to gain her approval [11, 37].

We take the first steps towards understanding the relation between the concepts of stylistic influence and social status, as reflected in Twitter network features, like number of followers and number of friends, that could be considered (rough) proxies for social status (Section 6.3).

**Rather surprisingly, we observe almost no correlation between these features and stylistic influence.**

###Communication Accommodation Theory

The psycholinguistic theory of communication accommodation was developed around the following main hypothesis: in dyadic conversations the participants converge to one another's communicative behavior in terms of a wide range of dimensions [12], both verbal and non-verbal.

Asymmetric accommodation has two flavors, depending on the behavior of the non-accommodating participant:

1.Default asymmetry: the non-accommodating participant maintains her default behavior (like in the previous example); 

2Divergent asymmetry: the non-accommodating participant adjusts her behavior in the opposite direction from that of the accommodating participant (i.e., diverges) [12].

Long-term accommodation is considered to be a separate phenomenon with potentially different properties [9, 12]. With a few notable exceptions [9, 32], empirical support for long-term accommodation is absent mostly due to the necessity of longitudinal data.

####Hypotheses:

1. One hypothesis is that accommodation occurs from a desire to increase communicational efficiency [37].

2. Another hypothesis is that a person's convergence to another person's communicative patterns is (non-consciously) driven by the desire gain the other's social approval [11, 37].

3. Yet another possible motivation is that accommodation is used to “maintain a positive social identity” [20] with the other.

With this work we aim to change this state of affairs and demonstrate the robustness of this theory in a large scale, real world environment where conversations are not as richly supported as they are in real-time interactions.

###Conversational Data

The resulting dataset contains 15 million tweets which make up the complete 2 public twitter activity (a.k.a. public timeline) of 7,800 users; for each user Twitter metadata (such as the number of friends, the number of followers, the location, etc.) is also available.

This conversational dataset is complete, in the sense that all twitter conversations ever held within each pair are available. To the best of our knowledge, this is the largest complete conversational dataset.

The main unit of interaction in this work is a conversational turn, which is defined as two consecutive tweets in a conversation. The two tweets in a turn are always sent by different users and are not retweets. Conversational dataset A contains 2.6 million turns and conversational dataset B contains 420,000 turns.4

###Probabilistic Framework

We start by addressing the more general phenomenon of stylistic cohesion. It reflects the intuition that tweets belonging to the same conversation are closer stylistically than tweets that do not.

Cohesion is defined by comparing the probability that a stylistic dimension is exhibited in tweets that are part of a conversation with the probability that the same dimension is exhibited in unrelated tweets.

Formally, for a given dimension C, the measure of stylistic cohesion can be expressed through the following probabilistic expression:

    Coh(C)≜p(TC∧RC|T ↔ R) -P(TC∧RC) (1)

where TC (respectively RC) is the event in which a tweet T (respectively R) exhibits C, and T ↔ R is the condition that tweets T and R form a conversational turn5. Thus, demonstrating that cohesion is observable for stylistic dimension C is reduced to showing that Coh(C) > 0.

When defining a probabilistic framework for linguistic style accommodation it is important to control for the effects of background style similarity (and provide the purity desiderata introduced in Section 1).

Therefore, the goal is to measure for a given pair of users a and b who engage in a conversation whether the use of a stylistic dimension C in the initial tweet (of user a) increases the probability of that stylistic dimension in the reply (of user b) beyond what is normally expected from user b (when replying to user a).

Formally, for a given stylistic dimension C and pair of users (a, b), the accommodation of user b to user a is measured by how much the fact that user a exhibits C in a tweet Ta increases the probability of b to also exhibit C in a reply to Ta:

    Acc(a,b)(C)≜P(TbC|TaC, Tb→Ta)−P(TbC|Tb→Ta) (2)

where TaC (respectively TbC ) is the event in which a tweet posted by user a (respectively b) exhibits C, and Tb→Ta is the condition that Tb is a reply to Ta.

Since the main goal is to address global accommodation (as opposed to the within-pair accommodation described above), the accommodation for a given dimension C is defined as:

    Acc(C) = E[Acc(a,b)(C)] (3)

where the expectation is taken over all possible conversing pairs (a, b).

One important property of the way Acc is defined is its asymmetry: the accommodation of user b to user a on stylistic dimension C is potentially different from the accommodation of user a to user b on the same stylistic dimension.

The notion of stylistic influence arises naturally:

I(a,b)(C) ≜ Acc(a,b)(C) − Acc(b,a)(C) (4)
for a given stylistic dimension C. If I(a,b)(C) > 0 we can say that b accommodates more to a on C than b does to a.

A related concept is accommodation symmetry (discussed in Section 2), which is tied to to the accommodation measure in the following way. Given that b accommodates to a, i.e Acc(a,b)(C) > 0, we have

1. Symmetry when Acc(b,a)(C) > 0,
 
2.Default asymmetry when Acc(b,a)(C) = 0,

3.Divergent asymmetry when: Acc(b,a)(C) < 0

###Empirical validation

In order to demonstrate that cohesion is exhibited in our data we estimate the two probabilities involved in (1) as follows. We estimate the first probability as the fraction of all turns in which both tweets exhibit dimension C: P-bar(TC∧RC|T ↔ R)=|{(t, r)|t ↔ r, tC, rC}|/|{(t, r)|t ↔ r}| (5)

where tC denotes the condition that a tweet t exhibits C.

To estimate the second probability, we first construct a set of “fake turns” by randomly pairing together tweets from the entire conversational data (regardless of their authors). We can then write: P-bar(TC∧RC)=|{(t, r)|t ↔ r, tC, rC}|/|{(t, r)|t ↔ r}| (6)

 >where tC is the condition that the tweet t exhibits C and t ↔ r is the condition that the tweets t and r are paired together in a fake turn.

All the differences are statistically significant with a p-value smaller than 0.0001 according to a two-tailed paired t-test11 for all strictly non-topical style dimensions with the exception of the 2nd person pronoun stylistic dimension for which the difference is not statistically significant.

Here are some of the comparisons worth pointing out:

1.Users accommodate significantly more on tentativeness than on certainty (p-value smaller than 0.01 according to an independent t-test).12

2.Users accommodate significantly more on negative emotions than on positive emotions (not illustrated, Acc(Neg. emo.) = 0.07, Acc(Pos. emo.) = 0.04; p-value smaller than 0.01 according to an independent t-test for the difference).

1st person singular pronoun vs. 2nd person pronoun. In retrospect, the fact that accommodation is not exhibited for the 2nd person pronoun dimension seems natural: words like ‘you' have a different meaning for two participants involved in a conversation. However, the same holds for the 1st person singular pronoun dimension for which accommodation is observed. This could be explained by the socialpsychology hypothesis of disclosure reciprocity in dyadic relationships [6].

In terms of our framework, we can test whether in expectation there is an imbalance of accommodation between participants in a conversation by verifying whether we can reject the null hypothesis E ˆ abs(I(a,b)(C)) ˜ = 0, where the expectation is taken over all conversing pairs (a, b). Using definition (4), this is reduced to rejecting:

    E[abs(Acc(a,b)(C) − Acc(b,a)(C)]=0. and further to rejecting:

    E[max(Acc(a,b)(C), Acc(b,a)(C)]= E[[min(Acc(a,b)(C), Acc(b,a)(C)]

where the first term is the expected accommodation of the most accommodating users (where the accommodation is always compared within each pair), and can by estimated the mean of: {max(Acc(a,b)(C), Acc(b,a)(C)|(a,b) ∈ Pairs},

and the second term is the expected accommodation of the least accommodating users, estimated by the mean of: {max(Acc(a,b)(C), Acc(b,a)(C)|(a,b) ∈ Pairs}.

of the most accommodating users (blue/right) in a pair. A difference in the type of imbalance between dimension is revealed; for example, while for 1st person plural pronouns in general the least accommodating users still match the style of the most accommodating participants (even though significantly less than vice-versa), for certainty the least accommodating users in general diverge from the style of the most accommodating participants.

However, our study indicates a clear difference between dimensions:

1.Symmetric accommodation is dominant for 1st pron. pl., Discrepancy and Indef. pron.;

2.Asymmetric accommodation (of both types) is dominant in most of the other dimensions;

3.Asymmetric diverging accommodation is dominant for 2nd person pronoun.

We find that for all style dimensions none of these features correlate strongly with stylistic influence; the largest positive Pearson correlation coefficient obtained was 0.15 between #followees and stylistic influence on 1st pron. pl.. Also, for the task of predicting the most influential user in each pair a decision tree classifier15 rendered relatively poor results.

###Related work

Much of the research in understanding social media focuses on the network relations between users. More recently, this line of work has been complimented with a rich analysis of the content of posts as well as structural relations among posters.

Latent variable models have also been used to summarize more general linguistic patterns in social media.

Another way of characterizing key trends in text data is to use known distinctions or dimensions.

Of particular interest in our work is the distinction between linguistic style and content.

Style or function words make up about 55% of the words that we speak, read and hear according to Tausczik and Pennebaker [38], similar to findings of Ramage et al. [35] in their analysis of Twitter.

One particularly interesting type of linguistic activity in social media has to do with conversations, that is with exchanges between one or more individuals.

Java et al. [22] found that 21% of users in their study used Twitter for conversational purposes (as measured by the use of @, a convention to address a post to a particular user), and that 12.5% of all posts were part of conversations.

Honeycutt and Herring [19] analyzed conversational exchanges on the Twitter public timeline, focusing on the function of the @ sign. They found that short dyadic conversations occur frequently, along with some longer multi-participant conversations

Linguistic style was shown to be crucial in the area of authorship attribution and in forensic linguistics (for an overview see [23]).

To identify an author, it is necessary to look beyond content into the — often subconscious — stylistic properties of the language. Simple measures like word length, word complexity, sentence length and vocabulary complexity were at the forefront of earlier research into attribution problems (e.g. [41, 18]).

Since Mosteller and Wallace's seminal work on the Federalist Papers [30], however, a trend has emerged to focus on the distribution of function words as a diagnostic for authorship, a method that in various incarnations now dominates the research.

###Conclusion and future work

One question we have not addressed is the issue of long-term accommodation: can we measure accommodation over a longer period of time, from the first interaction of two users on? Answering this question is challenging because it requires richer longitudinal data.
