---
tags:
  - computer-science
---
**XOR (exclusive OR)** is a logical operation that outputs *true **only when the inputs are different*** (one is 1 and the other is 0). 

If both inputs are the same (both 0 or both 1), it outputs **false**.

$$\displaystyle \Huge \begin{eqnarray} 
a\ \text{xor}\ b = a \oplus b
\end{eqnarray}$$

![[Pasted image 20250225180127.png|300]]

#### python

```python
a = 0b1100
b = 0b1010

a ^ b # a xor b
# 0b0110
```
