# HMM-based-POS-Tagger-and-Modified_Viterbi
The Penn Treebank: a large annotated corpus of English, is a corpus consisting of over 4.5+ million words of American English.
The vanilla Viterbi algorithmon on top of the Penn TreeBank results in some drop of accuracy mainly due to the fact that when the algorithm encountered an unknown word (i.e. not present in the training set, such as 'Twitter'), it assigned an incorrect tag arbitrarily.  <br>
This is because, for unknown words, the emission probabilities for all candidate tags are 0, so the algorithm arbitrarily chooses (the first) tag. <br>
Here we will modify the basic Viterbi Algorithm to solve the problem of unknown words using different techniques. Some of the techniques are based on the below questions - 
Which tag class will most of the unknown words belong to? Can rules based on morphological cues can be used to tag unknown words? </n>
Why does the Viterbi algorithm choose a random tag on encountering an unknown word? Can we modify the Viterbi algorithm so that it considers only one of the transition or emission probabilities for unknown words?
Here we will use the Treebank dataset of NLTK with the 'universal' tagset. The Universal tagset of NLTK comprises only 12 coarse tag classes as follows: Verb, Noun, Pronouns, Adjectives, Adverbs, Adpositions, Conjunctions, Determiners, Cardinal Numbers, Particles, Other/ Foreign words, Punctuations.(compared to the 46 fine classes such as NNP, VBD etc hence making the Viterbi algorithm faster as well.) 
