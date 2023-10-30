---
tags:
  - Russel-n-Norvig-chap-23
---
Similar to [[N-gram word model]] but instead of only count nearby words, it skips first before considering the next words.

*1-skip-bigram*: skips 1 word and considers two words: "a b c d" will consider "a c" and "b d".