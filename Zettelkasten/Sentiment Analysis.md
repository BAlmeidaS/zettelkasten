---
tags:
  - Russel-n-Norvig-chap-24
aliases:
  - sentiment classification
---
The goal of a Sentiment Analysis models is to classify using [[Natural Language Processing|NLP]] either *Positive* or *Negative* sentiment. But some schemes use more than 2 categories, or even a numerical scalar value.

Also known as *sentiment classification*.

>[!note] 
>The Simplest sentiment analysis one can build is using [[Word Embedding]].
>
>Transform phrases into their embeddings, aggregate them with a function like *average*, and pass to a *softmax* to get your classes (this is a sample architecture). However this does not perform well, a best approach is using any type of [[Recurrent Neural Network|RNNs]].

Using [[Recurrent Neural Network|RNNs]] we can collect all the [[Word Embedding]], and feed to an [[Recurrent Neural Network|RNN]] that the goal is to predict after the whole sequence the sentiment of the text:
![[Pasted image 20240712181554.png|700]]






