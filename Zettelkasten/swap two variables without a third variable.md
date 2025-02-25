---
aliases:
  - xor trick
---
This is the *xor trick*. Given any two numbers, $\displaystyle \large a$ and $\displaystyle \large b$. We can swap them by using a [[XOR]] operator, three times:

$$\displaystyle \Huge \begin{eqnarray} 
a &=& a \oplus b
\\
b &=& a \oplus b
\\
a &=& a \oplus b
\end{eqnarray}$$

```python
a = 17
b = 332

a = a ^ b
b = a ^ b
a = a ^ b

a # 332
b # 17
```
