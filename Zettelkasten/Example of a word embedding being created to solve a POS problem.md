---
tags:
  - Russel-n-Norvig-chap-24
---
Russell and Norvig present this example on the book and it clarifies how a [[Word Embedding]], is not just trained, it is part of a process and it helps to achieve that purpose.

In this case, the task is to a [[Part-of-speech tagging]]:

*from now on is literal from the textbook:*

![[Pasted image 20231101195226.png|600]]

Given a corpus of sentences with POS tags, we learn the parameters for the word embeddings and the POS tagger simultaneously. The process works as follows:
1. Choose the width w (an odd number of words) for the prediction window to be used to tag each word. A typical value is w = 5, meaning that the tag is predicted based on the word plus the two words to the left and the two words to the right. Split every sentence in your corpus into overlapping windows of length w. Each window produces one training example consisting of the w words as input and the POS category of the middle word as output.
2. Create a vocabulary of all of the unique word tokens that occur more than, say, 5 times in the training data. Denote the total number of words in the vocabulary as v.
3. Sort this vocabulary in any arbitrary order (perhaps alphabetically).
4. Choose a value d as the size of each word embedding vector.
5. Create a new v-by-d weight matrix called $\displaystyle \large E$. This is the word embedding matrix. Row i of $\displaystyle \large E$ is the word embedding of the $\displaystyle \large i\text{th}$  word in the vocabulary. Initialise $\displaystyle \large E$ randomly (or from pretrained vectors).
6. Set up a neural network that outputs a part of speech label, as shown in Figure 25.3. The first layer will consist of w copies of the embedding matrix. We might use two additional hidden layers, $\displaystyle \large z_1$ and $\displaystyle \large z_2$ (with weight matrices $\displaystyle \large W_1$ and $\displaystyle \large W_2$, respectively), followed by a softmax layer yielding an output probability distribution ˆy over the possible part-of- speech categories for the middle word:
$$\displaystyle \Huge \begin{eqnarray} 
z_1 &=& \sigma(W_1x) \\
z_2 &=& \sigma(W_2z_1) \\
\widehat{y} &=& \sigma(W_{out}z_2) \\
\end{eqnarray}$$
7. To encode a sequence of w words into an input vector, simply look up the embedding for each word and concatenate the embedding vectors. The result is a real-valued input vector $\displaystyle \large x$ of length $\displaystyle \large wd$. Even though a given word will have the same embedding vector whether it occurs in the first position, the last, or somewhere in between, each embedding will be multiplied by a different part of the first hidden layer; therefore we are implicitly encoding the relative position of each word.
8. Train the weights $\displaystyle \large E$ and the other weight matrices $\displaystyle \large W_1$, $\displaystyle \large W_2$, and $\displaystyle \large W_{out}$ using gradient descent. If all goes well, the middle word, cut, will be labeled as a past-tense verb, based on the evidence in the window, which includes the temporal past word “yesterday,” the third-person subject pronoun “they” immediately before cut, and so on.