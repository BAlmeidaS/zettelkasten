---
tags:
  - Russel-n-Norvig-chap-23
---
A type of evolution of [[Bag-of-words]] model.

Despite of bag-of-words, *N-gram considers that there is a dependency among the words*.

We could say that each word depends on all the ones that come before:
$$\displaystyle \Huge P(w_{1:N}) = \prod_{j=1}^n P(w\mid w_{1:j-1})$$

Though this is **completely unfeasible** - Vocabulary with 100k words and texts with 40 words will demand a model with $\displaystyle \large 10^{200}$ parameters.


So the answer is to consider some *n-words* before:
$$\displaystyle \Huge \begin{eqnarray} 
P(w \mid w_{1:j-1}) \approx\ &P&(W_j\mid w_{j-n+1:j-1}) \\
P(w_{1:N}) = \prod_{j=1}^n &P&(W_j\mid w_{j-n+1:j-1})
\end{eqnarray}$$

There are many types of famous n-grams, like **unigram / 1-gram**, **bigram / 2-gram**, **trigram / 3-gram**.