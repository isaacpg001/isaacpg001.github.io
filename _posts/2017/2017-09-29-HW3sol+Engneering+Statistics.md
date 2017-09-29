---
layout: post
title: Solutions to Homework 3 of Engeneering Statistics
categories:
- HomeWork
tags:
- Engeneering Statistics
- Solutions
---

1.

a).

$\rightarrow $ Since $A^T A= I_n$, A could not be singular, and $|A|=1$. Besides, Y = AX will have will be one to one map. 

$\rightarrow $ Meanwhile,

$$\big |\frac{dX}{dY} \big | = |A^{-1}|= |A| = 1$$

$\rightarrow $ Accordingly, the distribution of Y could be derived as 

$$f(Y) = f(X)_{X=A^TY} \big |\frac{dX}{dY} \big | = \frac{1}{(2\pi)^{n/2}}\  \exp { - \frac{(A ^TY)^T  (A^TY)}{2}} == \frac{1}{(2\pi)^{n/2}}\  \exp { - \frac{Y^T  Y}{2}} $$

which implies that Y is also a standard normal distribution.  

$\rightarrow $ QED



b).

$\rightarrow $
Sinnce Y is a a standard normal distribution, it indicates that $\sum_{i=2}^n Y_i^2$ is a $\chi_{n-1}^2$

$\rightarrow $
Since $\sum_{i=1}^n Y_i^2 = \sum_{i=1}^n X_i^2 $ and $Y_1 = \sqrt{n}\overline{X}$,  one could get 

$$\sum_{i=2}^n Y_i^2 = \sum_{i=1}^n Y_i^2  - Y_1^2 =  \sum_{i=1}^n X_i^2 - n \overline{X}^2 = (n-1)S^2$$

$\rightarrow $
Therefore $(n-1)S^2$ is a  $\chi_{n-1}^2$. 


$\rightarrow $QED

2.

a) 

$\rightarrow $
Since there are $n!$ combination to cut lines, having a ordered form $ (x_1< x_2< \cdots < x_n)$, and for each case it has a density probability as 

$$f(x_1)\times f(x_2)\times \cdots\times f(x_n) = 1$$
Therefore, the ordered density distribution could be written as
$$  f (x_1,x_2, \cdots ,x_n)= n!$$

$\rightarrow $
Then we have 

$$
\begin{array}{l}\\
P(V_1\geq c_1,  V_2\geq c_2,\cdots V_{n+1}\geq c_{n+1}) \\
=P(x_1\geq c_1, x_2 \geq x_1\ \ +c_2,\cdots, x_{n} \geq x_{n-1}\ \ +c_n, 1-x_n \geq c_{n+1}) \\
= \int_{x_0 + c_1}^{U_1} dx_1 \int_{x_1 + c_2}^{U_2} dx_2 \cdots \int_{x_{n-1}\ \ +c_n}^{U_n} dx_n  \   f (x_1,x_2, \cdots ,x_n)\\
= n! \int_{x_0 + c_1}^{U_1} dx_1 \int_{x_1 + c_2}^{U_2} dx_2 \cdots  \int_{x_{n-1}\ \ +c_n}^{U_n} dx_n
\end{array}$$


where $U_j = 1-\sum_{i = j+1}^{n+1} c_i$ and $x_0=0$. 

$\rightarrow $  Let  $\mathcal{P}_j =   \int_{x_{j-1}\ \ +c_{j}}^{U_j} dx_j \cdots  \int_{x_{n-1}\  \ +c_n}^{U_n} dx_n $.  。Now we will show that 

$$Lemma:\ \ \ \ \mathcal{P}_j  = \frac{1}{(n-j+1)!}(U_{j-1}-x_{j-1})^{n-j+1},\ \ if\ j\geq1$$

It is easy to verify that  this holds as $j = n$,  Then 

$$
\begin{array}{l}\\
\mathcal{P}_{j-1} =\int_{x_{j-2}\ \ +c_{j-1}}^{U_{j-1}} dx_{j-1}\mathcal{P}_{j} \\
=\frac{1}{(n-j+1)!}  \int_{x_{j-2}\ \ +c_{j-1}}^{U_{j-1}} dx_{j-1}  (U_{j-1}-x_{j-1})^{n-j+1}\\
=\frac{1}{(n-j+2)!} (U_{j-2}-x_{j-2})^{n-j+2}
\end{array}$$

Therefore the Lemma is verified.

$\rightarrow $ 
$P = n!\mathcal{P}_1 = (U_0-x_0)^n = (1-\sum_{i=1}c_i)^n $

$\rightarrow $  QED

b) 

$\rightarrow $ Denote $g(\rho,\theta)$ represent the density probability that the shortest length is $\rho$ and the shortest one is the $\theta$-th piece.

$\rightarrow $  From a), Let's set $c_1 = c_2=c_3 =\cdots =c_{n+1} = x$, then 


$$Eq1:\ \ \ \ \ P(V_1\geq x,  V_2\geq x,\cdots V_{n+1}\geq x)= [1-(n+1)x]^n $$

If set $c_1 = x-dx$, with others unchanged,  in the case $dx\to 0^+$, we have 

$$Eq2:\ \ \ P(V_1\geq x-dx,  V_2\geq x,\cdots V_{n+1}\geq x)=[1-(n+1)x]^n -  n [1-(n+1)x]^{n-1}dx$$

If  substract Eq1 by Eq2, which is actual the case that $V_1$ is the shortest and value is x. then 

$$ g(\rho =x,\theta = 1) = n [1-(n+1)x]^{n-1}$$

$\rightarrow $ The step above could be applied to any other case that $j$-th is shortest and have length x,  then we will always have 

$$ g(\rho =x,\theta = 1) =g(\rho =x,\theta = 2) \cdots =g(\rho =x,\theta = n+1) = n [1-(n+1)x]^{n-1}$$

$\rightarrow $ Now let's drop $\theta$, and denote $g(x)$ represents the shortest length is $x$, but the shorted piece is not specified, then 

$$g(x) =n (n+1)[1-(n+1)x]^{n-1}$$

Besides, the largest feasible value of x  satisfies that $(n+1)x = 1$, i.e. $x = 1/(n+1)$.

$\rightarrow $ Let $ y = (n+1)x$, therefore 

$$ f(y) = n [1-y]^{n-1}$$

which is actually a beta distribution with $\alpha = 1$, $\beta = n$

Then $$E[X]  = \frac{E[Y] }{n+1} =  \frac{1}{(n+1)^2} $$

3.

$\rightarrow $ For this distribution generating  data,  we have $$ E[X] = np=70 , \ \ \ \ Var[X] = np(1-p) = 21$$

$\rightarrow $ From the CENTRAL LIMIT THEOREM,

$$\begin{array}{l} P(30\leq X\leq 40) = P(X\leq 40) -P(X\leq 30) \\
\approx  P(\frac{X-70}{\sqrt{21} }\leq -\frac{30}{\sqrt{21} }) - P(\frac{X-70}{\sqrt{21} }\leq -\frac{40}{\sqrt{21} }) \\
= \Phi(-\frac{30}{\sqrt{21} }) - \Phi(-\frac{40}{\sqrt{21} }) \end{array}$$

4

$\rightarrow $ For the distribution described, the CDF is $1-\exp [- x]$

$\rightarrow $  The CDF of $X_n$  is directly 

$$ F(x) = (1-e^{-x})^n$$

 $\rightarrow $ The question is to ask  how to define $\{a_n\}$ such that 
 
$$\lim_{n\to \infty}  F(x-a_n) =\lim_{n\to \infty}  (1-e^{-x-a_n})^n$$
has a limit. 

 $\rightarrow $ An easy solution is $a_n =  log(n)$, therefore  
$$\lim_{n\to \infty}  F(x-a_n)  =\lim_{n\to \infty}  (1-\frac{e^{-x}}{n})^n = e^{-e^{-x}}$$
