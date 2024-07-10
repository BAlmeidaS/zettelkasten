---
tags:
  - Russel-n-Norvig-chap-23
---
Similar to [[N-gram word model]] but instead of only count nearby words, it skips some words. The idea is to create a dataset that gives the context of such words (sometimes for both sides).

So you will have a dataset composed of *context* and *target*

- **Input:** A corpus of text.
- **Target Word:** For each word in the corpus, the algorithm considers it as a target word.
- **Context Window:** It defines a context window size (e.g., 2 words to the left and 2 words to the right of the target word).
- **Context Words:** The words within the context window are considered as context words for the target word.
- **Dataset Creation:** Pairs of (target word, context word) are created. For example, if the sentence is "The cat sat on the mat" and the context window size is 2, the pairs for the word "sat" would be ("sat", "The"), ("sat", "cat"), ("sat", "on"), and ("sat", "the").

The Idea is that by defining this dataset a model aims to reconstruct this probability distribution, by using [[softmax function|softmax]]

![[Pasted image 20240710172916.png|600]]
