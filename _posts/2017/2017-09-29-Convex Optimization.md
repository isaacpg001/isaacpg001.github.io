---
layout: post
title: Convexity and Concavity on Infimum and Supremum 
categories:
- Useful Formular
tags:
-  Optimal Control
---

<center>$Lemma: $ <span style="color:blue;font-size: 1em;">the supremum(infimum) of the set of affine functions is convex(concave)</span></center>


####  1. infimum and supremum 
The infimum is the greatest lower bound of a set S. Consequently, the supremum is also referred to as the least upper bound (or LUB).

#### 2. Affine Function 

An affine function is a function composed of a linear function + a constant and its graph is a straight line. The general equation for an affine function in 1D is: $$y = Ax + c$$.  Or in arbitary dimensions

$$ F(\vec{x})=\sum_i a_i x_i +const $$


#### 3.Convexity and Concavity

Suppose g is an affine function on $\lambda$ space. 
$$g(\alpha\lambda_1 + (1-\alpha)\lambda_2 , x) = \alpha g(\lambda_1, x)  + (1-\alpha)g(\lambda_2, x) $$

Besides, we denote that $g^+(\lambda) := \sup_{x\in D}g(\lambda, x)$ and $g^-(\lambda) := \inf_{x\in D}g(\lambda, x)$ . 


$$
g(\alpha\lambda_1 + (1-\alpha)\lambda_2 , x) = \alpha g(\lambda_1, x)  + 
(1-\alpha)g(\lambda_2, x) = \left\{ 
\begin{array}{l}
\leq \alpha g^+ (\lambda_1) + (1-\alpha)g^+(\lambda_2)\\
\geq \alpha g^- (\lambda_1) + (1-\alpha)g^-(\lambda_2)\\
\end{array}\right.
$$

Since the inequlity above holds for every $x$, we could derive that 

$$
\begin{array}{l}
g^+(\alpha\lambda_1 + (1-\alpha)\lambda_2 ) \leq \alpha g^+ (\lambda_1) + (1-\alpha)g^+(\lambda_2)\\
g^-(\alpha\lambda_1 + (1-\alpha)\lambda_2 ) \geq \alpha g^- (\lambda_1) + (1-\alpha)g^-(\lambda_2)\\
\end{array}
$$