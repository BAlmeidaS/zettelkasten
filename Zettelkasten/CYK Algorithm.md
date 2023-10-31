---
tags:
  - Russel-n-Norvig-chap-23
---
Probabilistic version of a bottom-up [[Parsing]].

It requires the [[Grammar]] to be on the [[Chomsky Normal Form]].

Space-complexity: $\displaystyle \large O(n^2m)$
Time-complexity: $\displaystyle \large O(n^3m)$

$\displaystyle \large n$: number of words in the sentence
$\displaystyle \large m$: number of non-terminal symbols in the grammar

Guarantee to *parse all possible* [[Context-Free Grammar|Context-Free Grammars]]

![[Pasted image 20231031110819.png]]