

Suppose 

$$ X = \left[\begin{array}{cc} 
A&B \\
B^T&C\end{array}
\right]
$$


If $X$ is positive definite and  we know , for arbitary vector $\vec{r} = \left(\begin{array}{c} 
u \\
v\end{array}
\right)
$ should should satisfy that $  \vec{r}^T X\vec{r} > 0$, i.e.

$$ f(u,v) = u^T Au + 2v^TB^Tu+v^TCv >0$$

(1) if $v = \vec{0}$, it requires that $A$ must be positive definite.
(2) if $A$ is positive definite, for specified v, $f(u,v)  $ minimizes at $u = - A^-1Bv$. then 

$$f(u,v) = v^TSv $$
where $S - C - B^TA^{-1}B$, then S should be positive definite.


