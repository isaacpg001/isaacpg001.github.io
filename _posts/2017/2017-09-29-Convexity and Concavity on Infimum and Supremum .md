---
layout: post
title: Convexity and Concavity on Infimum and Supremum 
categories:
- Useful Formular
tags:
-  Optimal Control
---

$Lemma:$  <span style="color:blue;font-size: 1em;">the supremum(infimum) of the set of convex(concave) functions is convex(concave)</span>

####  1. infimum and supremum 
The infimum is the greatest lower bound of a set S. Consequently, the supremum is also referred to as the least upper bound (or LUB).

#### 2.Convexity and Concavity

If g is convex function,
$$ g(\alpha\lambda_1 + (1-\alpha)\lambda_2 ,x) \leq \alpha g(\lambda_1, x)  + (1-\alpha)g(\lambda_2, x) \leq \alpha g^+(\lambda_1)  + (1-\alpha)g^+(\lambda_2) $$ 

Since the statement holds for every x, we have 
$$g^+(\alpha\lambda_1 + (1-\alpha)\lambda_2)\leq \alpha g^+(\lambda_1)  + (1-\alpha)g^+(\lambda_2)$$

If g is concave function,
$$ g(\alpha\lambda_1 + (1-\alpha)\lambda_2 ,x) \geq \alpha g(\lambda_1, x)  + (1-\alpha)g(\lambda_2, x) \geq \alpha g^-(\lambda_1)  + (1-\alpha)g^-(\lambda_2) $$ 
From the same argument, we get
$$g^-(\alpha\lambda_1 + (1-\alpha)\lambda_2)\geq \alpha g^-(\lambda_1)  + (1-\alpha)g^-(\lambda_2)$$

#### 3. A case Study
An affine function takes this form

$$ F(x)=A x +b $$

which could be reagrded as a special case both in convex and concave functions.

The Lagrange dual function we will study latter will certainly be a concave,

$$g(\lambda,v) = \inf_{x\in D} f_0(x) + \sum_i \lambda_i f_i(x) + \sum_i v_i h_i(x)$$


#### 4. Besides 
If $f(x,\lambda) = x^2 -2\lambda x$, which is linear in $\lambda$, the infimum of $f(x,\lambda)$ is 

$$f^-(\lambda) = -\lambda^2$$

This tells even a function could be linear in some parameters, but its infimum or supremum may not be linear.
