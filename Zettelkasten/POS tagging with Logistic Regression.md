---
tags:
  - Russel-n-Norvig-chap-23
---
The idea is using [[Logistic Regression]] to perform [[Part-of-speech tagging]].

We will create one logistic regression for each tag (adjective, noun, ...), and run every one for each word. The highest probability will give us the tag.

Regarding the features, one way is to use the whole sentence as a [[feature vector]]. Thus, we can run a [[Greedy Best-first search]] where we evaluate all the words in the sentence without any tags, get the word with the highest probability for some tag, set the tag and use this word as a tag to the next ones, until we set all the tags. *It is a greedy algorithm, finishes fast but not perfectly*. An evolution to achieve better results could be using [[Beam Search]]