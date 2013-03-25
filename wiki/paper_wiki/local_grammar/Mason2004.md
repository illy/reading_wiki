###Introduction

These case studies are sufficient to demonstrate the validity and use of a corpus-based approach to language analysis, but are not scaleable–they require a lot of careful effort by a specialist.

The basic underlying model of language is that a language is a system of choices/options/elements which make only sense in comparison with each other, ie. when a selection is made part of its meaning is in all the other available options which have not been chosen.

A single choice looked at in isolation (without the range of possible alternatives) does not make (much) sense. However, it is difficult to comprehensively study all options manually, as analysing language data is time-consuming and requires a high level of skill.

for example when it comes to word classes: these have originally been specified in antiquity and are based on ancient Greek and Latin (as are a lot of other grammatical categories).

In a hierarchical model of processing (which is how most NLP systems operate) errors made at an early stage can propagate upwards, making it difficult to reach accurate final results.

In general, tasks involving assumed grammatical categories are always problematic and any outcomes have to be carefully analysed to assert their validity; the problem here is that it cannot be easily determined whether it is the program that is at fault, or whether the grammatical categories are simply inadequate.

In real life, language, however, is rarely ambiguous due to additional information supplied by common sense or shared contextual knowledge.

Studies in corpus linguistics have shown that even different inflected forms of a word often have complementary distributions. Sinclair (1991) demonstrates that eye and its plural form eyes are used in different contexts and cannot be interchanged, yet they both share the word class ‘noun’.

Automation is essential if a reasonably comprehensive analysis is to be attempted. This is one of the aims of this work.

###Local grammar patterns

Most grammatical formalisms are based on either constituency or dependency, the two basic principles of structural description.

The basic idea is that local grammars for recurring elements (eg. date expressions) are constructed, which can then be re-used in the description of larger linguistic constructions; basically a bottom-up approach towards a comprehensive description of a language.

Local grammars are also well-suited for (semi-) fixed phrases, where some limited variation is form is possible, but with minimal change in meaning.

Pattern Grammar (eg. Hunston and Francis (2000)) abandons a rule-based hierarchical structure in favour of patterns or templates that describe typical environments a word occurs in.

 >Patterns are derived from analysing corpus data, so they are based on actual usage. Like local grammar, patterns contain a mixture of actual lexical items (mostly prepositions) and abstract elements (such as noun group, that-clause, etc).

Unlike local grammar, pattern grammar attempts a broader description of syntactic behaviour, which is less lexicalised.

 >Typically the only lexically restricted elements in a pattern will be the main word the pattern belongs to, and perhaps a preposition (which is more specific than the general class of all prepositions).

One of the important issues with pattern grammar is the correspondence between form and meaning: it can be seen that words which share aspects of their meaning also occur in similar sets of patterns.

 >Typically a pattern will be used to realise several different meanings, and each of these meanings will be associated with a different set of related words which go together with this pattern.

###System outline

Senotence boundaries are not taken into account, as the aim is the recognition of a pattern and not yet the analysis of a complete sentence.

The final stage in processing is an RTN parser, which takes as input a finite-state network describing a set of patterns for a word.

The RTN parser ranks each path through the RTN according to length; typically a pattern can match in several ways.

###Evaluation

From a selection of corpora (3 million words in size) 56 lines for blend and its inflected forms were retrieved and tested on the automaton generated from the pattern list.

There are four possible outcomes of a pattern match:

1.The correct pattern is the highest ranking pattern returned by the recogniser

2.The correct pattern has been found, but is not at the highest rank

3.The correct pattern has not been identified at all

4.A pattern has been recognised, but there is actually no pattern in the data
