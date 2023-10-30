---
tags:
  - Russel-n-Norvig-chap-23
---
Even dealing with unknown words in, [[N-gram word model]] have a problem of unseen n-grams, set of words that where not put it together in the whole *corpus*. Something like *colorless aquamarine ideas* in a (3-gram)

The problem lies on the fact that rare n-grams can appear on the training set and other not. Ideally **it should deal with all similar n-grams in the same way**.

The process to deal with similar n-grans is by the process of [[Smoothing - Backoff model]]