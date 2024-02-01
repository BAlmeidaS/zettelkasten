---
tags:
  - Calculus
---
Similar to the [[max and min - single variable|concavity test]] but to [[multivariable function]].

But instead of using derivatives, we will use [[partial derivatives]] or more explicit [[gradient]]. We want to find the [[Critical Points]], then we apply the *second-partial derivative test*.

The test is about calculating the value of $\displaystyle \large D(\boldsymbol{x})$ in a [[Critical Points|critical point]] $\displaystyle \large \boldsymbol{x_0}$
$$\displaystyle \Huge \begin{eqnarray} 
& &D(x,y) = 
f_{xx}(x,y)
f_{yy}(x,y)
-(f_{xy}(x,y))^2
\end{eqnarray}$$
$$\displaystyle \Huge \begin{eqnarray} 
&\text{if, }& D(x_0,y_0) < 0&,& &then\ (x_0,y_0) \text{ is } saddle\ point 
\\
&\text{if, }& D(x_0,y_0) > 0\text{ and } f_{xx}(x_0, y_0) > 0&,& &then\ (x_0, y_0) \text{ is } minimum
\\
&\text{if, }& D(x_0,y_0) > 0\text{ and } f_{xx}(x_0,y_0) < 0&,& &then\ (x_0,y_0) \text{ is } maximum
\\
&\text{if, }& D(x_0,y_0) = 0&,& &then\ (x_0, y_0) \text{ is } undefined
\end{eqnarray}$$

In the case of $\displaystyle \large D(x_0, y_0) > 0$, I decided to use $\displaystyle \large f_{xx}$, but it could be $\displaystyle \large f_{yy}$, totally optional.

![[Pasted image 20240201165716.png]]

### general formula

*it can also be calculated using the [[determinant of hessian matrix]]*, which is crucial to have a practical way to understand when we have more than 2 variables:
$$\displaystyle \Huge \begin{eqnarray} 
D(\boldsymbol{x_0}) &=& det(\boldsymbol{H_f}(\boldsymbol{x_0})) \\\\
\end{eqnarray}$$
