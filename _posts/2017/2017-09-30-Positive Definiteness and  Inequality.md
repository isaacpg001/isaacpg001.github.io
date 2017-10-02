---
layout: post
title: Positive Definiteness and  Inequality
categories:
- Useful Formular
tags:
-  Optimal Control
---

Suppose 

$$ X = \left[\begin{array}{cc} 
A&B \\
B^T&C\end{array}
\right]
$$

and function 

$$ f(y) =y^TXy = u^T Au + 2v^TB^Tu+v^TCv >0$$

where $y = \left(\begin{array}{c} 
u \\
v\end{array}
\right)
$. If $A\succeq 0$ and $\det A\neq 0$, in the space spanned by $u$, f(u,v) minimizes at $u = - A^-1Bv$, followed by

$$f(u,v) = v^T(C - B^TA^{-1}B)v $$

Then, we could find that

$$A\succeq 0\ and\ \det A\neq 0:\ \ C - B^TA^{-1}B\succ 0 \Longleftrightarrow X \succ 0\ $$

$$A\succeq 0\ and\ \det A\neq 0:\ \ C - B^TA^{-1}B\succeq 0 \Longleftrightarrow X \succeq 0$$

#### 1. Schur complement

$C - B^TA^{-1}B$ is called the Schur complement of A in X.

#### 2. Application 


If x and y is matrix, and $S = \{(x,y,t) \mid y \succ 0\ and\ x^T y^{-1} x \leq t \}$ , then S is convex,

From the conclusion before, $C=t,\ B = X,\ A = Y$, therefore 

$$ \left[\begin{array}{cc} 
Y&x \\
x^T&t\end{array}
\right] \succeq 0
$$

Then, 

$$S = \{(x,y,t)\mid y\succ 0\ and\  \left[\begin{array}{cc} 
Y&x \\
x^T&t\end{array}
\right] \succeq 0\}$$

Because the condition above is linear in $x,y,t$ S must be convex set

#### 3. Comments

This result will be useful to change uqestions from an inequality to matrix definiteness related, or from quadratic terms to linear ones. 
