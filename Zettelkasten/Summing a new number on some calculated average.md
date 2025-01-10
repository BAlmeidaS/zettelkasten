---
tags:
  - math
  - Statistics
cssclasses:
  - wider_page.css
aliases:
  - mean iteration calculation
  - variance iteration calculation
  - covariance iteration calculation
---
Considering a [[Average|Mean]] calculated over $\displaystyle \large n-1$ numbers. If a new number $\displaystyle \large x_n$ is introduced, how does it change the average?

$$\displaystyle \Huge \begin{eqnarray} 
given, \\
Average_n &=& \dfrac{x_1+x_2+\dots+x_n}{n} \\
\\
Average_{n-1} &=& \dfrac{x_1+x_2+\dots+x_{n-1}}{n-1} \\
Average_{n-1}*(n-1) &=& x_1+x_2+\dots+x_{n-1}

\\\\
so,
\\
Average_n &=& \dfrac{x_1+x_2+\dots+x_{n-1}+x_n}{n} \\
&=& \dfrac{Average_{n-1}*(n-1)+x_n}{n} \\
&=& \dfrac{Average_{n-1}*n - Average_{n-1} + x_n}{n} \\
&=& \dfrac{Average_{n-1}*n}{n} + \dfrac{-Average_{n-1} + x_n}{n} \\
&=& Average_{n-1} + \dfrac{x_n - Average_{n-1}}{n} \\\\
so,\\
\overline{x_n} &=& \overline{x_{n-1}} + \dfrac{x_n - \overline{x_{n-1}}}{n}

\end{eqnarray}$$

And how about the [[Variance]], how will it change?

### first wrong solution

$$\displaystyle \Huge \begin{eqnarray} 
\sigma^2_{n-1} &=& \dfrac{\sum\limits^{n-1} (x-\overline{x_{n-1}})^2}{n-1}\\
\sigma^2_{n} &=& \dfrac{\sum\limits^n (x-\overline{x_n})^2}{n} \\
\\\\

\sigma^2_{n} &=& \dfrac{\sum\limits^n 
\left(x 
- \overline{x_{n-1}} 
- \dfrac{x_n - \overline{x_{n-1}}}{n}
\right)^2} {n}
\\\\ && \text{using }(a-b)^2 = a^2 - 2ab + b^2,
\\
&=& \dfrac{\sum\limits^n 
\left(
x - \overline{x_{n-1}} 
\right)^2
-2\left(
(x - \overline{x_{n-1}})
* (\dfrac{x_n - \overline{x_{n-1}}}{n})
\right)^2
+\left(
\dfrac{x_n - \overline{x_{n-1}}}{n}
\right)^2
}{n}
\\\\&&\text{splitting } \Sigma s,
\\
&=& \dfrac{
\sum\limits^n 
\left(
x - \overline{x_{n-1}} 
\right)^2
-2
\overbrace{
\sum\limits^n 
\left(
\overbrace{
(x - \overline{x_{n-1}})
}^{\text{around the mean}}
*
\overbrace{
(\dfrac{x_n - \overline{x_{n-1}}}{n})
}^{\text{not depent of i}}
\right)^2
}^{\text{this part is 0}}
+
\sum\limits^n 
\left(
\dfrac{x_n - \overline{x_{n-1}}}{n}
\right)^2
}{n}
\\
&=& \dfrac{
\sum\limits^n 
\left(
x - \overline{x_{n-1}} 
\right)^2
+
\overbrace{
\sum\limits^n 
\left(
\dfrac{x_n - \overline{x_{n-1}}}{n}
\right)^2
}^{\text{not dependent on i, only will occur n times}}
}{n}
\\
&=& \dfrac{
\sum\limits^n 
\left(
x - \overline{x_{n-1}} 
\right)^2
}{n}
+
\dfrac{
n*
\left(
\dfrac{x_n - \overline{x_{n-1}}}{n}
\right)^2
}{n}
\\
&=& \dfrac{
\sum\limits^n 
\left(
x - \overline{x_{n-1}} 
\right)^2
}{n}
*
\left(
\dfrac{n-1}{n-1}
\right)
+
\dfrac{
\cancel{n}*
\left(
\dfrac{x_n - \overline{x_{n-1}}}{n}
\right)^2
}{\cancel{n}}
\\
&=& \dfrac{
\sum\limits^n 
\left(
x - \overline{x_{n-1}} 
\right)^2
}{n-1}
*
\left(
\dfrac{n-1}{n}
\right)
+
\left(
\dfrac{x_n - \overline{x_{n-1}}}{n}
\right)^2
\\
&=& 
\sigma^2_{n-1}
*
\left(
\dfrac{n-1}{n}
\right)
+
\left(
\dfrac{x_n - \overline{x_{n-1}}}{n}
\right)^2
\end{eqnarray}$$



### second solution

$$\displaystyle \Huge \begin{eqnarray} 
\sigma^2_{n-1} &=& \dfrac{\sum\limits^{n-1} (x-\overline{x_{n-1}})^2}{n-1}\\
\sigma^2_{n} &=& \dfrac{\sum\limits^n (x-\overline{x_n})^2}{n} \\
\\\\

\sigma^2_{n} &=& \dfrac{\sum\limits^n 
\left(x 
- \overline{x_{n-1}} 
- \dfrac{x_n - \overline{x_{n-1}}}{n}
\right)^2} {n}
\\\\ && \text{using }(a-b)^2 = a^2 - 2ab + b^2,
\\
&=& \dfrac{\sum\limits^n 
\left(
x - \overline{x_{n-1}} 
\right)^2
-2\left(
(x - \overline{x_{n-1}})
* (\dfrac{x_n - \overline{x_{n-1}}}{n})
\right)^2
+\left(
\dfrac{x_n - \overline{x_{n-1}}}{n}
\right)^2
}{n}
\\\\&&\text{splitting } \Sigma s,
\\
&=& \dfrac{
\sum\limits^n 
\left( x - \overline{x_{n-1}}  \right)^2
-
\overbrace{
\sum\limits^n 
2 \left( (x - \overline{x_{n-1}}) * \dfrac{x_n - \overline{x_{n-1}}}{n} \right)^2
}^{\text{remove from $\Sigma$ elements independent of i} \atop \text{do not forget the square!}}
+
\overbrace{
\sum\limits^n \left( \dfrac{x_n - \overline{x_{n-1}}}{n} \right)^2
}^{\text{not dependent on i,} \atop \text{will only occur n times}}
}{n}
\\
&=& 
\overbrace{
\dfrac{ \sum\limits^n  \left( x - \overline{x_{n-1}} \right)^2 }{n}
}^{\text{same element}}
-2
\dfrac{(x_n - \overline{x_{n-1}})^2}{n^2}
\overbrace{
\dfrac{ \sum\limits^n  \left( x - \overline{x_{n-1}} \right)^2 }{n}
}^{\text{same element}}
+\dfrac{ \cancel{n}* \left( \dfrac{x_n - \overline{x_{n-1}}}{n} \right)^2 }{\cancel{n}}
\\
&=& 
\dfrac{ \sum\limits^n  \left( x - \overline{x_{n-1}} \right)^2 }{n}
*\left(1-2 \dfrac{(x_n - \overline{x_{n-1}})^2}{n^2} \right)
+\left( \dfrac{x_n - \overline{x_{n-1}}}{n} \right)^2
\\
&=& 
\dfrac{ \sum\limits^n  \left( x - \overline{x_{n-1}} \right)^2 }{n}
* \left(\dfrac{n-1}{n-1}\right)
*\left(1-2 \dfrac{(x_n - \overline{x_{n-1}})^2}{n^2} \right)
+\left( \dfrac{x_n - \overline{x_{n-1}}}{n} \right)^2
\\
&=& 
\dfrac{ \sum\limits^n  \left( x - \overline{x_{n-1}} \right)^2 }{n-1}
* \left(\dfrac{n-1}{n}\right)
*\left(1-2 \dfrac{(x_n - \overline{x_{n-1}})^2}{n^2} \right)
+\left( \dfrac{x_n - \overline{x_{n-1}}}{n} \right)^2
\\
&=& 
\sigma^2_{n-1}
* \left(\dfrac{n-1}{n}\right)
*\left(1-2 \dfrac{(x_n - \overline{x_{n-1}})^2}{n^2} \right)
+\left( \dfrac{x_n - \overline{x_{n-1}}}{n} \right)^2
\\\\
&& \text{using that } x_n - \overline{x_{n-1}} = (\overline{x_n} - \overline{x_{n-1}})*n
\\
&=& 
\sigma^2_{n-1}
* \left(\dfrac{n-1}{n}\right)
*\left(1 - 2\dfrac{
(\overline{x_n} - \overline{x_{n-1}})^2*n^2
}{n^2} \right)
+\left( \dfrac{x_n - \overline{x_{n-1}}}{n} \right)^2
\\
&=& 
\sigma^2_{n-1}
* \left(\dfrac{n-1}{n}\right)
*\left(1 - 2 (\overline{x_n} - \overline{x_{n-1}})^2 \right)
+\left( \dfrac{x_n - \overline{x_{n-1}}}{n} \right)^2
\\
&=& 
\sigma^2_{n-1} * \left(\dfrac{n-1}{n}\right)
- \sigma^2_{n-1} * \left(\dfrac{n-1}{n}\right) * 2 (\overline{x_n} - \overline{x_{n-1}})^2
+\left( \dfrac{x_n - \overline{x_{n-1}}}{n} \right)^2

\end{eqnarray}$$

### third solution

$$\displaystyle \Huge \begin{eqnarray} 
\sigma^2_{n-1} &=& \dfrac{\sum\limits^{n-1} (x-\overline{x_{n-1}})^2}{n-1}\\
\sigma^2_{n} &=& \dfrac{\sum\limits^n (x-\overline{x_n})^2}{n} \\
\\\\

\sigma^2_{n} &=& \dfrac{\sum\limits^n 
\left(x 
- \overline{x_{n-1}} 
- \dfrac{x - \overline{x_{n-1}}}{n}
\right)^2} {n}

\\\\
\cdots
\\\\

\sigma_n^2 &=& \frac{n-1}{n} \sigma_{n-1}^2 + \frac{1}{n} (x_* - \bar{x}_{n-1})(x_* - \bar{x}_n)

\end{eqnarray}$$

chategpt defined slightly different:
![[Pasted image 20250109165124.png]]

## Covariances
from [[Covariance]]:
$$\displaystyle \Huge \begin{eqnarray} 
COV_n(x,y) &=& \sum\limits^{n}_{i=1}\dfrac{(x_i-\bar{x}_n)(y_i-\bar{y}_n)}{n}
\\
COV_{n-1}(x,y) &=& \sum\limits^{n-1}_{i=1}\dfrac{(x_i-\bar{x}_{n-1})(y_i-\bar{y}_{n-1})}{n}
\end{eqnarray}$$
so, we can expand $\displaystyle \large COV_n$ using the mean definition (seen above)
$$\displaystyle \Huge \begin{eqnarray} 
COV_n(x,y) &=& \sum\limits^{n}_{i=1}\dfrac{(x_i-\bar{x}_n)(y_i-\bar{y}_n)}{n}
\\
&=& \sum\limits^{n}_{i=1}\dfrac{
(x_i - \bar{x}_{n-1} - \dfrac{x_n - \bar{x}_{n-1}}{n})
(y_i - \bar{y}_{n-1} - \dfrac{y_n - \bar{y}_{n-1}}{n})
}{n}
\\\\
&& \text{let's remove the first $n$th-term:}
\\
&=& 
\overbrace{
(x_n - \bar{x}_{n-1} - \dfrac{x_n - \bar{x}_{n-1}}{n})
(y_n - \bar{y}_{n-1} - \dfrac{y_n - \bar{y}_{n-1}}{n})
\dfrac{1}{n}
}^{\text{first part of the queation}}
 +
\overbrace{
\sum\limits^{n-1}_{i=1}\dfrac{
(x_i - \bar{x}_{n-1} - \dfrac{x_n - \bar{x}_{n-1}}{n})
(y_i - \bar{y}_{n-1} - \dfrac{y_n - \bar{y}_{n-1}}{n})
}{n}
}^{\text{second part of the queation}}
\end{eqnarray}$$

#### let's solve the first part:
$$\displaystyle \Huge \begin{eqnarray} 
1st &=& 
(x_n - \bar{x}_{n-1} - \dfrac{x_n - \bar{x}_{n-1}}{n})
(y_n - \bar{y}_{n-1} - \dfrac{y_n - \bar{y}_{n-1}}{n})
\dfrac{1}{n}
\\ &=& 
(\dfrac{n(x_n - \bar{x}_{n-1}) - (x_n - \bar{x}_{n-1})}{n})
(\dfrac{n(y_n - \bar{y}_{n-1}) - (y_n - \bar{y}_{n-1})}{n})
\\ &=& 
(\dfrac{(x_n - \bar{x}_{n-1})(n-1)}{n})
(\dfrac{(y_n - \bar{y}_{n-1})(n-1)}{n})
\dfrac{1}{n}
\\ &=& 
\dfrac{(x_n - \bar{x}_{n-1})(y_n - \bar{y}_{n-1})(n-1)^2}{n^3}
\end{eqnarray}$$
#### let's solve the second part:

$$\displaystyle \Huge \begin{eqnarray} 
2nd&=&
\overbrace{
\sum\limits^{n-1}_{i=1}\dfrac{
(x_i - \bar{x}_{n-1} - \dfrac{x_n - \bar{x}_{n-1}}{n})
(y_i - \bar{y}_{n-1} - \dfrac{y_n - \bar{y}_{n-1}}{n})
}{n}
}^{\text{second part of the queation}}
\\
&=&

\sum\limits^{n-1}_{i=1}\dfrac{
(
\overbrace{x_i - \bar{x}_{n-1}}^{\text{a}} - \overbrace{\dfrac{x_n - \bar{x}_{n-1}}{n}}^{\text{b}}
)(
\overbrace{y_i - \bar{y}_{n-1}}^{\text{c}} -  \overbrace{\dfrac{y_n - \bar{y}_{n-1}}{n})}^{\text{d}}
}{n}
\\\\
&& \text{condidering the coeficients we have: $ac-ad-bc+bd$:}
\\
&=&
\sum\limits^{n-1}_{i=1}\dfrac{
(x_i - \bar{x}_{n-1})(y_i - \bar{y}_{n-1})
- (x_i - \bar{x}_{n-1})(\dfrac{y_n - \bar{y}_{n-1}}{n})
- (y_i - \bar{y}_{n-1})(\dfrac{x_n - \bar{x}_{n-1}}{n})
+ (\dfrac{x_n - \bar{x}_{n-1}}{n})(\dfrac{y_n - \bar{y}_{n-1}}{n})
}{n}
\\\\
&& \text{lets split the sigma}
\\
&=&
\overbrace{
\sum\limits^{n-1}_{i=1}\dfrac{
	(x_i - \bar{x}_{n-1})(y_i - \bar{y}_{n-1})
}{n}
}^{\text{i-term}}
-
\overbrace{
\sum\limits^{n-1}_{i=1}\dfrac{
	(x_i - \bar{x}_{n-1})(\dfrac{y_n - \bar{y}_{n-1}}{n})
}{n}
}^{\text{ii-term}}
-
\overbrace{
\sum\limits^{n-1}_{i=1}\dfrac{
	(y_i - \bar{y}_{n-1})(\dfrac{x_n - \bar{x}_{n-1}}{n})
}{n}
}^{\text{iii-term}}
+
\overbrace{
\sum\limits^{n-1}_{i=1}\dfrac{
	(\dfrac{x_n - \bar{x}_{n-1}}{n})(\dfrac{y_n - \bar{y}_{n-1}}{n})
}{n}
}^{\text{iv-term}}
\end{eqnarray}$$

*let's break down each term:*
##### i-term
$$\displaystyle \Huge \begin{eqnarray} 
\text{i-term} &=&
\sum\limits^{n-1}_{i=1}\dfrac{
	(x_i - \bar{x}_{n-1})(y_i - \bar{y}_{n-1})
}{n}
\\ &=&
\sum\limits^{n-1}_{i=1}\dfrac{
	(x_i - \bar{x}_{n-1})(y_i - \bar{y}_{n-1})
}{n}*\dfrac{n-1}{n-1}
\\ &=&
\sum\limits^{n-1}_{i=1}\dfrac{
	(x_i - \bar{x}_{n-1})(y_i - \bar{y}_{n-1})
}{n-1}*\dfrac{n-1}{n}
\\ &=&
COV_{n-1}(x,y)*\dfrac{n-1}{n}
\end{eqnarray}$$
##### ii-term
$$\displaystyle \Huge \begin{eqnarray} 
\text{ii-term} &=&
\sum\limits^{n-1}_{i=1}\dfrac{
	(x_i - \bar{x}_{n-1})(\dfrac{y_n - \bar{y}_{n-1}}{n})
}{n}
\\ &=&
(\dfrac{y_n - \bar{y}_{n-1}}{n})
\sum\limits^{n-1}_{i=1}\dfrac{
	(x_i - \bar{x}_{n-1})
}{n}
\\
since, && \sum^m (x_i-\bar{x}_m) = (\sum^m x_i)-\bar{x}_m =\bar{x}_m-\bar{x}_m = 0
\\\\
\text{ii-term} &=& 0

\end{eqnarray}$$

##### iii-term
$$\displaystyle \Huge \begin{eqnarray} 
\text{iii-term} &=&
\sum\limits^{n-1}_{i=1}\dfrac{
	(y_i - \bar{y}_{n-1})(\dfrac{x_n - \bar{x}_{n-1}}{n})
}{n}
\\
&& \text{same argument of ii-term...}
\\
\text{iii-term} &=&0
\end{eqnarray}$$

##### iv-term
$$\displaystyle \Huge \begin{eqnarray} 
\text{iv-term} &=&
\sum\limits^{n-1}_{i=1}\dfrac{
	(\dfrac{x_n - \bar{x}_{n-1}}{n})(\dfrac{y_n - \bar{y}_{n-1}}{n})
}{n}
\\ &&
\text{nothing depends on $i$, so we replace sigma }
\\\\ &=&
(n-1)*(\dfrac{x_n-\bar{x}_{n-1}}{n})(\dfrac{y_n-\bar{y}_{n-1}}{n}) * \dfrac{1}{n}
\\ &=&
\dfrac{(n-1)(x_n-\bar{x}_{n-1})(y_n-\bar{y}_{n-1})}{n^3}

\end{eqnarray}$$

#### putting all pieces together of the 2nd equation:
$$\displaystyle \Huge \begin{eqnarray} 
2nd&=&
\overbrace{
\sum\limits^{n-1}_{i=1}\dfrac{
(x_i - \bar{x}_{n-1} - \dfrac{x_n - \bar{x}_{n-1}}{n})
(y_i - \bar{y}_{n-1} - \dfrac{y_n - \bar{y}_{n-1}}{n})
}{n}
}^{\text{second part of the queation}}
\\ &=&
COV_{n-1}(x,y)*\dfrac{n-1}{n} + \dfrac{(n-1)(x_n-\bar{x}_{n-1})(y_n-\bar{y}_{n-1})}{n^3}
\end{eqnarray}$$

#### putting 1st and 2nd part together:

$$\displaystyle \Huge \begin{eqnarray} 
COV_n(x,y) &=& \sum\limits^{n}_{i=1}\dfrac{(x_i-\bar{x}_n)(y_i-\bar{y}_n)}{n}
\\
&=& 
\dfrac{(x_n - \bar{x}_{n-1})(y_n - \bar{y}_{n-1})(n-1)^2}{n^3}
+COV_{n-1}(x,y)*\dfrac{n-1}{n} + \dfrac{(n-1)(x_n-\bar{x}_{n-1})(y_n-\bar{y}_{n-1})}{n^3}
\\ &=& 
COV_{n-1}(x,y)*\dfrac{n-1}{n}
+ \dfrac{(x_n - \bar{x}_{n-1})(y_n - \bar{y}_{n-1})(n-1)(n-1)}{n^3}
+ \dfrac{(x_n-\bar{x}_{n-1})(y_n-\bar{y}_{n-1})(n-1)}{n^3}
\\ &=& 
COV_{n-1}(x,y)*\dfrac{n-1}{n}
+ \dfrac{(x_n - \bar{x}_{n-1})(y_n - \bar{y}_{n-1})(n-1)(n-1+1)}{n^3}
\\ &=& 
COV_{n-1}(x,y)*\dfrac{n-1}{n}
+ \dfrac{(x_n - \bar{x}_{n-1})(y_n - \bar{y}_{n-1})(n-1)n}{n^3}

\end{eqnarray}$$