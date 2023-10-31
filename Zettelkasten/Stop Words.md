---
tags:
  - Russel-n-Norvig-chap-23
---
Stop words are the *most common words in a language*. After [[Tokenization]] it is common on [[Natural Language Processing|NLP]] models that we remove this words since they don't bring (usually) real meaning.

There are some situations that we must keep them. Some [[Word Embeddings]] using deep learning and [[Transformers]], often don't remove them because they can capture the contextual meaning