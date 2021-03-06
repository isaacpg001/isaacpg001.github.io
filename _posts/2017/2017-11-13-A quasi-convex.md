---
layout: post
title:  A quasi-convex
tags:
-  optimal control
---

### Theorem：

$f(x)$ and $g(x)$ are differentiable. $f'(x)\geq 0$, $g'(x)>0$ and $g(x)>0$. 

Then 
$$\frac{f}{g} \text{ is a quasi-convex, when } \frac{f'}{g'}\text{ is a nondecreasing function}$$ 

 g is increasing function, which is a one-to-one mapping. Let's denote that $$W(x) = \frac{f(x)}{g(x)}  = \frac{f[(g^{-1}(y)]}{y}= \frac{F(y)}{y}= w(y)$$

Then $\frac{f'(x)}{g'(x)}= F'(y)$.

From the fact $f'/g'$ is nondecreasing, we have  $$\frac{d}{dx}\frac{f'}{g'} = g' \frac{d}{dy}\frac{f'}{g'} = g'\frac{d}{dy} F'(y) = g'F''(y)\geq 0$$

As $g'>0$ always hold we have $F''(y)\geq 0$, then F is a convex function in y.



Suppose $W(x_1)\leq \alpha $ and $W(x_2)\leq \alpha $. Then W is quasi-convex if $W(x)\leq \alpha$, where $x\in [x_1,x_2]$. As g is 1-to-1 map, this statement is equvilent to $w(y)\leq \alpha$, when $y\in [g(x_1),g(x_2)]$. Let y = tg(x_1)+(1-t)g(x_2), where $t = \frac{y-g(x_1)}{g(x_2)-g(x_1)}$. Then $t\in [0,1]$.

$$w(y)=w[tg(x_1)+(1-t)g(x_2)] =  \frac{F[tg(x_1)+(1-t)g(x_2)]}{tg(x_1)+(1-t)g(x_2)} \leq \frac{tF[g(x_1)]+(1-t)F[g(x_2)]}{tg(x_1)+(1-t)g(x_2)}\leq \alpha$$

### Application:

$$\underset{r\geq 0,Q\geq 1}{\inf}\ \frac{AD+\sum_{y=r+1}^{r+Q} c(y)}{Q}=\underset{Q\geq 1}{\inf}F[Q] = \underset{Q\geq 1}{\inf}\underset{r\geq 0}{\inf} \ \frac{AD+\sum_{y=r+1}^{r+Q} c(y)}{Q}$$

We first take the minimum when fixed Q, when $Q$ increase uniformly, the numerator increases larger $c(y)$, considering that $c(y)$ is quasi-convex. Therefore,  F[Q] is quasi-convex.
