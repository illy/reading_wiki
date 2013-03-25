Such local grammars do not just capture some rare linguistic phenomena. Widespread technical jargon, idioms, or clichés, lead to common syntactic constraints that can be accurately described locally without resorting to more powerful syntactic formalisms.

A local grammar may describe a set of forbidden or unavoidable sequences. In both cases, it can be compactly represented by a finite automaton.

A collection of local grammars can be combined and represented by a more complex finite automaton by taking the union of the simpler local grammar automata.

###9.1 Description of the problem

Let Σ denote the alphabet and let A be a local grammar finite automaton specifying a set of forbidden sequences. We denote by L(A) the language accepted by A. By definition, any sequence containing a sequence accepted by A is unacceptable. Thus, acceptable sequences must be in Σ∗L(A)Σ∗.

 >Let T be the automaton representing the set of all possible tagging of a text (Koskenniemi, 1990).

 >T can be obtained by concatenating simpler automata representing the set of possible tagging for each of the word composing the text.

The main problem for the application of a large local grammar A to a text automaton T is the efficient computation of an automaton representing L(T) ∩ Σ∗ L(A)Σ∗ .

###9.2 Algorithms

####9.2.1 A simple Algorithm

The problem of the application of a local grammar can be viewed as a generalization to automata of pattern-matching in text.

1.A simple algorithm for the application of A to T is to search for all sequences accepted by A starting from each state of T.

2.If a forbidden sequence is found, the appropriate transition is removed to disallow that sequence.

 >This can be done by: simulating the presence of a self-loop labeled with all elements of Σ at the initial state of A;
    
 >reading the paths of T starting from its initial state while pairing each state reached by a string x with the set of all states of A that can be reached by x from its initial state.

Each state of the output automaton is a pair (p, s) where p is a state of T and s an element of the powerset of the states of A.

At each state, the transitions of state p and those of the set of states in s are matched to form new transitions.

In general, this operation may be very costly because of the large number of transitions leaving the states of s.

As it is clear from this example, the algorithm is very similar to the **simple quadratic-time string-matching algorithm** seeking to match a pattern at each position of the text, ignoring the information derived from matching attempts at previous positions.

The next section describes an algorithm that precisely exploits such information as with the **linear-time string-matching algorithm** of Knuth et al. (1977).

Figure 4(d) shows the result of the application of that algorithm. Each state of the output automaton is identified with a pair of states (p, q) where p is a state of T and q the state of A corresponding to the longest (proper) suffix of the strings leading to p.

####9.2.2 A more efficient local grammar algorithm

The application of a local grammar is directly related to the computation of a deterministic automaton representing Σ∗L(A).

1.Let A′ be the automaton constructed by augmenting A with a self-loop at its initial state labeled with all elements of the alphabet Σ, and let B = det(A′) be the result of the determinization of A′. B recognizes the language Σ∗L(A).

2.To apply the local grammar A to T , we can proceed as for computing the intersection B ∩ T , barring the creation of transitions leading to a state identified with a pair (p, q) where q is a final state of B.

3.In fact, since determinization can be computed on-the-fly (Aho et al., 1986, Mohri, 1997a), the full determinization of A′ is not needed, only the part relevant to the computation of the intersection with T.

In general, the computation of B′ may be very costly though, in particular because of the alphabet size |Σ| which can reach several hundred thousand.

There exists an algorithm for constructing a compact representation of the deterministic automaton representing Σ∗L(A) using failure transitions (Mohri, 1997b).

 >A **failure transition** is a special transition that is taken when no standard transition with the desired input label is found.

The algorithm can be viewed as a generalization to an arbitrary deterministic automaton A of the classical algorithms of Knuth et al. (1977) and that of Aho and Corasick (1975) that were designed only for strings or trees.

When A is a tree, the complexity of the algorithm of Mohri (1997b) coincides with that of Aho and Corasick (1975): it is linear in the sum of the lengths of the strings accepted by A.

### 9.3 Conclusion

Accurate local grammar automata are useful tools for disambiguation.

They can significantly speed up the application of further text processing steps such as part-of-speech tagging or parsing.

Another natural way to define local grammars is to use context-dependent rewrite rules.

Context-dependent rules can be efficiently compiled into finite-state transducers that can then be readily applied to an input text automaton (Kaplan and Kay, 1994, Mohri and Sproat, 1996). They can be further generalized to weighted context-dependent rules compiled into weighted transducers (Mohri and Sproat, 1996).
