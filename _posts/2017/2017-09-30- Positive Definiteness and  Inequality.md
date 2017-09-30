

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
$$f(u,v) = v^TSv $$

where $S = C - B^TA^{-1}B$


Conclusion:

As $A\succeq 0$ and $\det A\neq 0$,
$$ S\succ 0 \Longleftrightarrow X \succ 0$$

$$ S\succeq 0 \Longleftrightarrow X \succeq 0$$

