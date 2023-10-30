---
tags:
  - Russel-n-Norvig-chap-23
---
Using [[N-gram word model]] it is possible that the model will evaluate some text that contains a word not mapped. Attribute *zero probability leads to a big mistake* because since the words are correlated this can lead to *lose a big portion of the text*.

An alternative is attributing special tokens on the [[Tokenization]]. Something like *\<UNK\>*. Even different tokens can be used at the same time, *\<EMAIL>*,  *\<NUM>*, and so on.

