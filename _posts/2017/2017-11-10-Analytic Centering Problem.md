---
layout: post
title:  Analytic Centering Problem
categories:
- Analysis
tags:
-  Optimal Control
---

### Analytic Centering Problem

$$ f = -\sum_i^m \log (b_i-a_i^T x),\ \ \textbf{dom}\ f = \{x\mid Ax\prec b\}$$

### Property:
Suppose $f$ is feasible. 

(1) f is bounded $\Longleftrightarrow$ f have global optimal $\Longleftrightarrow$ $L_\alpha =\{ x\mid f(x)\leq \alpha\}$ is a closed nonempty set for $\alpha \in [0,0^+)$.

(2) $\textbf{dom} f$ is bounded $\Longleftrightarrow$  f has unique global 

(3) Ax<b is same as $y\neq 0 ,y\geq 0,A^Ty=0,b^Ty\leq0$ have no solutions.

Remark: these conclusion are not apllied in general, just for this question. 


### Open Boundary and sublevel set

** If a convex function's sublevel let is closed from some high level, global minima must could be achived in this closed set.  **


### Unbounded

If we say f is unbounded, we must have a sequence  {$x_k$} such that  $\lim_{k\to \infty} f(x_k) \to -\infty$. If $x_0$ is feasible, from the convexity, we have that 
$$f(x_k) \geq f(x_0) + \nabla f(x_0)^T (x_k - x_0)$$

$\nabla f(x_0)^T (x_k - x_0)$ have to be $-\infty$ when $k\to \infty$.


### Some Comments:
Seperating plane is a good method, but sometimes we also use dual-primal to solve questions. 

Like $S=\{z|z>0, A^T z =0\}$, we construct a primal and dual as 

$$\begin{array}{clccl}
min& b & & max & 0\\
s.t.&z+be\geq 0 & &s.t. & y^Te =1\\
& A^Tz = 0&&& y\geq 0 \\
&&&& y = Av\\
\end{array}$$

If S is feasible, clearly we have that the primal is unbounded, then due to strong duality, the second should be infeasible. The condition could be represented as $Av\geq 0$ and $e^TAv=1$, since v is arbitary, this is same as "there is a v such that $Av\geq 0$ and $Av\neq 0$.

We know the primal is always feasible. For example, z =0 and b =0.  If S is unfeasible, $A^T$'s null space is null, then z=0,b=0 is the optimal solution. If $A^T$'s null space is not null, since S is unfeasible, for any solution, there is a $z_j\leq 0$. Since $z_j+b\geq 0$. Then $b\geq 0$. Therefore the optimal solution is 0. Due to strong duality, we have it lead to that there is v such that $Av\geq 0$ and $Av\neq 0$


Generally, we change the unstrict inequality to equality by adding some term.  In this method, the primal is often feasible. 


### Proof On Property

1) f is unbounded below. if and only if  $Av\preceq 0$ and $Av\neq 0$ have solution.

If f is unbounded below, 

$$\nabla f(x_0)^T (x_k - x_0) = m + \sum_{j} \frac{a_i^Tx_k - b_i}{b_i-a_i^Tx_0} $$

Then the vector that $\{\frac{a_i^Tx_k - b_i}{b_i-a_i^Tx_0}\}\prec 0$, and at least one of them could be $-\infty$(let assume j-th is a case), then for any $z\succ 0 $, we have $\sum_i z_i\frac{a_i^Tx_k - b_i}{b_i-a_i^Tx_0} \leq z_j\frac{a_j^Tx_k - b_j}{b_j-a_j^Tx_0} \leq -\infty $. 

If there exist a point z that $z\succ 0 $ and $Az=0$. Then we have that $\sum_i z_i\frac{a_i^Tx_k - b_i}{b_i-a_i^Tx_0} =  \sum_i\frac{ - z_i b_i}{b_i-a_i^Tx_0}  $, which must be bounded, in the contrasiction with its negitve infity requirements. Therefore if f is unbounded below, $z\succ 0 $ and $Az=0$ have no slution. Or $Av\preceq 0$ and $Av\neq 0$ have solutions. 


If $Av\preceq 0$ and $Av\neq 0$, we could also constrcut that $x = x_0 + tv$, where $t\geq 0$, then f could be unbounded. 

2) If f is bounded, then there will be no $Av\preceq 0$ and $Av\neq 0$, or there exist $z\succ 0$ and $A^Tz=0$.   Namly $A^T$ have a positive null vector.

Clearly . For any vector $f(x+v)$,$v\in Null_A$ and $x\notin Null_A$, we change it as $f(x)$, which doesnot change the objective value. Now we first consider the case that $f(x)$   $x^T Null_A =0$. Since each point could be represent as $x=x_0 + tv$,  $Av\neq 0$.

we have that $Ax_0 + tAv\prec b$ then $tAv \prec b - Ax_0$.  Set $Av/(b-Ax_0) = w$, then $wt<1$. Also, the objective function will becomes that 

$$f = constant - \sum_i \log (1-w_i t)$$

f is still bounded after transformation. Now let specify the conditions on w.  $w\neq0$ as required and $w_i$ could not be all nonnegtive or nonpositive otherwise $z\succ 0$ and $w^Tz=0$ have no solutions.  Then $\alpha = \max_{w_i >0}w_i$ and $\beta = \min_{w_i <0}w_i$. We see t is in the limit $[\frac{1}{\beta},\frac{1}{\alpha}]$. At these two limit extreme points, f becomes $+\infty$. Since f is a convex function. Then f(t) have closed sublevel set. Then f attains global optima in the set $Ax<b$ and $x^T Null_A =0$. Besides we see $\partial_t^2 f = \sum_i \frac{w_i^2}{1-w_it}>0$. f is a strcitly convex. the solution  is unique when  $x^T Null_A =0$

Then optimal solution could be represented as $x^*+N_A$  If this solution is unique, then we does not have $Ax=0$ and since there will be no $Av\preceq 0$ and $Av\neq 0$, namely $Ax\leq 0$ have no solution, the whole region will be bounded.

1) If feasible and bouned, then unique.

2) If feasible and $A^T$ have positive null vector, then optima exist， which is unique or not depends on whether A is full rank.

3) Projection of optimal solutions to the Range space of $A^T$ will be unique.


