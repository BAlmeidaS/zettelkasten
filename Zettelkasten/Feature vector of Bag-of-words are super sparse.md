---
tags:
  - Russel-n-Norvig-chap-23
---
Since the features of a [[Bag-of-words]] models are the words and the values the amount of times they appeared in the text, this ends up with a *really sparse feature vector.* (Small texts will have many words never used).

We must do some type of [[Feature Selection]]. Removing words that are very rare (narrow domains only) or removing words that are very common (articles and pronouns, for instance).

