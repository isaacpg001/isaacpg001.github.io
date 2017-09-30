

Suppose 

$$ X = \left[\begin{array}{cc} 
A&B \\
B^T&C\end{array}
\right]
$$

and function 

$$ f(u,v) =u^T Au + 2v^TB^Tu+v^TCv >0$$
which actually is $y^TXy$, with $y = \left(\begin{array}{c} 
u \\
v\end{array}
\right)
$.

If $A\succeq 0$ and $\det A\neq 0$, in the space spanned by $u$, f(u,v) minimizes at $u = - A^-1Bv$, followed by
$$f(u,v) = v^TSv $$

where $S = C - B^TA^{-1}B$


