---
tags:
  - Russel-n-Norvig-chap-12
aliases:
  - PDF
---
A function that defines the probability of a **continuous** [[Random Variable]]. Theoretically, the probability of a point is zero, we define probabilities of ranges.

![[Pasted image 20231015025759.png|400]]

Formally, $\large P(x)$ in a pdf is the range: $\huge P(x) \lim\limits_{dx \to 0} \frac{P(x \le X \le x + dx)}{dx}$ - [[Limit]]