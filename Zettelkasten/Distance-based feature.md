---
tags:
  - machine-learning
  - computer-science
---
A possible feature to measure how much two [[Vertices]] are *close to be connected*, to predict [[Edge-level Task - Traditional ML methods|if a new edge should be added]], would be *shortest-path distance*

The claim is *If the shortest-path distance is small, they might be more likely to have a connection*.

>[!example] 
>$$\displaystyle \Huge S_{BH} = S_{AB} = 2$$
>$$\displaystyle \Huge S_{BG} = S_{BF} = 3$$
>![[Pasted image 20240620223343.png|400]]

*Although, this does not capture the degree of neighbourhood overlapping*.
Node pair $\displaystyle \large (B, H)$ has 2 shared neighbouring nodes ($\displaystyle \large C$ and $\displaystyle \large D$), whereas $\displaystyle \large (A, B)$ has only 1, tho they have the same number (2).