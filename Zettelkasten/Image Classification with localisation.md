---
tags:
  - deep-learning
---
A type of problem that [[Convolutional Neural Network|CNNs]] are useful to solve.

Besides the [[softmax function|softmax]] to classify the image $\displaystyle \large c$ (stands for class), 4 other numbers are predicted: $\displaystyle \large b_x, b_y, b_h, b_w$, the variables that define the *bounding box around the object identified* 
![[Pasted image 20240719124758.png]]
$\displaystyle \Large p_c$ says if there is something on the image (if there is nothing, $\displaystyle \large p_c = 0$)
