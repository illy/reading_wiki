###11.1 Indroduction

As a simple computation shows, there are more than 1050 sentences having at most 20 words, a number which seems to deprive of any meaning the possibility of performing a systematic inquiry.

But grammarians operating at the level of sentences seem to be interested only in elaborating general rules and do so without performing any sort of systematic observation and without a methodical accumulation of sentence forms to be used by further generations of scientists.

It is not necessary to stress that such an accumulation in any science is mad possible by constructing and using suitable equivalence relations to eliminate what are deemed to be accidental variations, irrelevant to the specified goal of the catalog.

The approach in linguistics leads all too easily to overgeneralization.

 >The earliest models (Markovian model) of language dealt with sequences of grammatical categories, i.e. they formalized sentence forms where each word is replaced by its grammatical category.

 >Such models succeeded in capturing in a natural way gross positional features such as the place of articles and adjectives on the left of their noun.

 >Chomsky 1957 formalized them under the name of context-free grammars and demonstrated some of their fundamental inadequacies on the basis of carefully selected examples.

 >In fact, as early as 1952, Harris had proposed transformational grammars, which constituted a vast improvement over the Markovian and phrase structure models. Detailed attempts of systematic applications have revealed an endless number of subclasses of exceptions, each of them require a special treatment.

Previous Markovian models were aimed at giving a global description of a language, where as the model we advocate, and which we call it finite-state for short, is of a strictly local nature.

 >In this perspective, the global nature of language results from the interaction of a multiplicity of local finite-state schemes which we call finite-state local automata.

Our **goal** repeat is very specifically to account for all the possible sentences within a given corpus, and this with no exception.

 >The apparent obstruction evoked above to the realization of such a program is avoided by the complexity of the various automata necessary for the description of the corpus.

It turns out that the long range constrains are taken care of automatically, so to say, by the interaction of the automata within the complete structured schema.

These individual automata can be reused to describe other corpora.

Many adverbs derived from adjectives are systematically accepted in the left context of speaking and of no other forms. This phenomena is clearly of a finite-state nature.

Finite state automata: each has one initial state and one final state.

1.It departs from classical representations in that states are not overtly represented: the nodes are not the states, there is no symbol for them.

2.To avoid multiplying parallel paths with words having identical roles, labels are grouped in boxes.

3.We note sentence patterns in the following way: N0 V N1 Prep N2 represents the structure subject-verb-two complements; the N,,i,s are noun phrases.

###11.2 Linguistic modules

Such separations are crucial in the sense they allow a modular construction of the grammar of the field. But we will see that in other situations, one must introduce both semantic and syntactic criteria to obtain separations. Moreover, ergonomic limitations such as the size of computer screens also intervene as boundary conditions in the effective construction of local grammar.

####11.2.1 Example 1

###11.3 Transformations

Many transformation affect word order. Finite automata can compactly represent sets of strings that differ by variant substrings including the null variant, but they cannot well represent pairs of strings that differ by a permutation.
