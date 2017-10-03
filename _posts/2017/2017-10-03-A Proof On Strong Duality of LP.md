---
layout: post
title: A Proof on Strong Duality of LP
categories:
- Useful Formular
tags:
-  Optimal Control
---

### 1. Proof

#### 1.1 Revised Simplex
First, we know the following questions are same

$$ \begin{array}{cl}
min & c^Tx\\
s.t. & Ax\geq b\\
&x\geq 0\end{array} \Longleftrightarrow \begin{array}{cl}
min & (c^T, 0) \left(\begin{array}{c}x\\x_s \end{array}\right)\\
s.t. & [A, -I] \left(\begin{array}{c}x\\x_s \end{array}\right) =b\\
& x,x_s\geq 0\end{array}$$

Since there is a optimal and finite solution for the question above. Suppose there is basis change operation $R$ in the sapce of $\left(\begin{array}{c}x\\x_s \end{array}\right)$, and 

$$R\left(\begin{array}{c}x \\x_s \end{array}\right) = \left(\begin{array}{c}x_B\\x_S \end{array}\right),\ \ \ [A, - I]R^{-1}  = [B,N],\ \ \ (c_B^T,c_S^T) = (c^T,0) R^{-1}$$ 

 Also $Bx_B + N x_S=b$, the objective becomes 

$$ obj = c_B^TB^{-1} (b-Nx_S) +c_S^Tx_S=c_B^T B^{-1} b +(c_S^T - c_B^T B^{-1}N)x_S  $$

If in this basic bais, the solution is optimal, then $obj = c_B^TB^{-1}b$, with $c_S^T - c_B^T B^{-1}N\succeq 0$

Then

$$c_S^T - c_B^T B^{-1}N\succeq 0\text{ and }c_B^T - c_B^T B^{-1}B\succeq 0\ \ \Longrightarrow\ \ [c_B^T,c_S^T] \succeq c_B^T B^{-1}[B,N] \Longrightarrow\ \ [c_B^T,c_S^T]R \succeq c_B^T B^{-1}[B,N]R\\
\Longrightarrow\ \ [c^T,0] \succeq c_B^T B^{-1}[A,-I] \Longrightarrow\ \ c^T \succeq c_B^T B^{-1}A\\$$

#### 1.2 Dual Property

Let $$g(y) = \inf_x c^Tx + y^T(b-Ax) =\inf_x (c^T-y^TA) x +y^Tb$$

Then the dual will be 

$$\begin{array}{cl}
max & y^Tb\\
s.t. &  y^TA \leq c^T\\
&y\geq 0\end{array}$$

Then we immediately see $y^T = c_B^TB^{-1}$ is solution of function above. and the corresponding value is same as the primal question.

#### 1.3 Strong Duality

Since $g(y)$ is the infimum of the primal question, then $g(y)$ will always be smaller than the optimal value of function 1. However, we have found their values are equal now. Then they have to be equal.

Or in this way

$$y^Tb\leq y^TAx \leq c^Tx$$

If one of them has a finite optimal solution, so does the other.

### 2. Conclusion

$$\text{Primal Feasible finite optimal } \Longleftrightarrow \text{  Dual Feasible same finite optimal } $$

Note: the region may be open boundary.

$$\text{One is unbounded} \Rightarrow\text{ The other will be nonfeasible}$$


$$\text{One is nonfeasible} \Rightarrow\text{ The other will not be finite feasible optimal}$$

### 3. A Case
Note that 

(1)

$$ \begin{array}{cl}
min & x\\
s.t. & \left[ \begin{array}{c}
0\\
1
\end{array}\right] x \leq \left[ \begin{array}{c}
-1\\
1
\end{array}\right] \end{array}
 \ \ \ \ \Longleftrightarrow\ \ \ \  \begin{array}{cl}
max & z_1-z_2\\
s.t. & z_2+1=0\\
&z_1,z_2\geq 0 \end{array}$$

Both the primal and dual will be non-feasible.

(2)

Finite optimal with open boundary 
$$ \begin{array}{cl}
min & x_1+2x_2+x_3\\
s.t. & x_1+x_2\geq 2\\
&x_2+x_3\geq 2 \end{array}$$


