---
tags:
  - Russel-n-Norvig-chap-12
---
The tool to deal with degrees of beliefs - or to the uncertain about facts

Defined with 3 axioms:

1. Probability of an event is a non-negative real number:  
$$\displaystyle \Huge P(Event) \in \mathbb{R}, P(event) \ge 0 \ \ \ \ \forall event \in F$$
$$\displaystyle \Large \text{$F$ is the event space}$$

2. Probability of the entire sample space ($\large \Omega$) is one: $$\displaystyle \Huge P(\Omega) = 1$$
3. The probability of disjoint sets can be calculated by the sum of their individual probabilities:
$$\displaystyle \Huge P(\bigcup\limits^{\infty}_{i=1}E_i) = \sum^{\infty}_{i=1}P(E_i)$$
$$\displaystyle \large \text{for 2 disjoint events:}$$
$$\displaystyle \large \text{If $A \cap B = \emptyset$,\ \ \ then}\ \ P(A \cup B) = P(A) + P(B)$$