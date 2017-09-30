

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
$$ C - B^TA^{-1}B\succ 0 \Longleftrightarrow X \succ 0\ \text{under the condition }A\succeq 0 \det A\neq 0$$

$$ C - B^TA^{-1}B\succeq 0 \Longleftrightarrow X \succeq 0\ \text{under the condition }A\succeq 0 \det A\neq 0$$

