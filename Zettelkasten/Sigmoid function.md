*Sigmoid function* has the famous S-shape and it is commonly used in [[classification]] problems.

A sigmoid, $\displaystyle \large \sigma(x)$, can be defined with any one of the following:
$$\displaystyle \Huge \begin{eqnarray} 
\sigma(x) &=& \dfrac{1}{1+e^{-x}} \\ \\
\sigma(x) &=& \dfrac{e^x}{1+e^{x}} \\ \\
\sigma(x) &=& 1 - \sigma(-x) \\

\end{eqnarray}$$

![[Pasted image 20231130135514.png|500]]

The [[derivative]] of the sigmoid $\displaystyle \large \sigma$ is
$$\displaystyle \Huge \begin{eqnarray} 
\dfrac{d}{dx} \sigma(x)
&=&
\dfrac{e^{-x}}{(1+e^{-x})^2} 
\\
&=&
\dfrac{1}{1+e^{-x}} *
\dfrac{e^{-x}}{1+e^{-x}} 
\\\\
& & \text{(sum 1 and sub 1):}
\\
&=&
\dfrac{1}{1+e^{-x}} *
\dfrac{1-1+e^{-x}}{1+e^{-x}} 
\\
&=&
\dfrac{1}{1+e^{-x}} *
\left(
\dfrac{1+e^{-x}}{1+e^{-x}} -
\dfrac{1}{1+e^{-x}} 
\right)
\\
&=&
\dfrac{1}{1+e^{-x}} *
\left(
1-
\dfrac{1}{1+e^{-x}} 
\right)
\\

\dfrac{d}{dx} \sigma(x)
&=&
\sigma(x)*(1-\sigma(x))
\end{eqnarray}$$