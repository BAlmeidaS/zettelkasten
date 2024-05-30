---
tags:
  - paper
  - rate-3
---
URL: https://www.cs.emory.edu/~jyang71/files/walklm.pdf
Review: https://openreview.net/forum?id=ZrG8kTbt70&referrer=%5Bthe%20profile%20of%20Carl%20Yang%5D(%2Fprofile%3Fid%3D~Carl_Yang1)
Review average (1-5): 3
Conf: NeurIPS 2023

---

GNNs for training require sufficient training data for downstream tasks to achieve strong performance. Self supervised learning approaches are inefficient due to the presence of a variety of node attributes and complicated relations between nodes. Inspired from the success in LLMs, they convert the graphs into natural language to be consumed by pre -trained language models. Random walk sequences are extracted from the graph and are converted into text through entity level and walklevel textualization. Roberta model is then fine tuned to predict the masked node / edges as textual sequences. The approach is tried on various node classification and link prediction tasks with significant improvements.