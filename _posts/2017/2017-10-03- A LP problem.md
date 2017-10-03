
Q4. 

[Questions see here](https://github.com/isaacpg001/isaacpg001.github.io/blob/master/source/F100001123330637_1507007918549_113.jpg)
###  <center>Some Results on These Two Questions</center>
### Notation

Since the contraints of two questions are linear, the solutions are convex.  If both of them have feasible regions. it will be natural to write a feasible solution, with such a form

$$ x = x_0 + t v$$
where $x_0$ is a feasible solution and v is any unit directional vector from point $x_0$. The objective function could be
rewritten as 
 $$ z = c^T(x_0 + tv) = c^Tx_0 + tc^Tv $$
 and 
 
 $$ Ax-b = (Ax_0-b) + tAv$$
 
 #### Eq 1

For this question, without lossing generality, we setting $t\geq 0$. Then we shall see, if $\max z$ is unbounded then 

$$ Av \leq 0, \ \ \ \ \text{for some v satisfying }c^Tv>0$$


Since for any v' satisfying $c^Tv' \leq 0 $ and $t\geq 0$ we always have $c^Tx_0 + tc^Tv' \leq c^Tx_0$. Therefore we only consider the case that $c^Tv> 0$ to maximize the objective value.  we change the objective function as 

$$ \max\ z = \sup_{t\in [0,\infty), \ \ c^Tv>0 }c^Tx_0 + tc^Tv$$


Then if $\max\ z$ is unbounded, it requires that there exist some $v$, which satisfying $c^Tv>0$, and $x_0 + tv$ is feasible even $t\to \infty$. Since  b- Ax_0 $ tAv\leq b- Ax_0$ for $t\to \infty$, then  $Av\leq 0$. Conversely, if there is some v satisfying that $c^Tv >0$ and $Av\leq 0$,  in this direction, t could be $\infty$, then $\max\ z$ is unbounded.

The argument also requires that if $\max z$ is bounded with feasible solutions, then
$$\text{for any v with } c^Tv>0\text{. there shall be some component that }(Av)_j >0$$
As a result, t will always be limited  in this direction. Since $t$ is limited in every v with $c^Tv>0$, which means the objective is finite for all v, then the objective is finite. Conversely, if the objective value is finite, t should be limited for each direction that $c^Tv$=0, where limitation means some component of $Av$ is positive

In summary, $\textbf{if Eq1 is feasible}$,

$$ \text{Eq1 id unbounded above } \Longleftrightarrow  Av \leq 0, \ \ \ \ \text{for some v satisfying }c^Tv>0$$


$$ \text{Eq1 has a finite optimal solution } \Longleftrightarrow  \text{for any v with } c^Tv>0\text{. there shall be some component that }(Av)_j >0$$

#### Eq2

For this question, without lossing generality, we setting $t\leq 0$. Then we shall see, if $\min z$ is unbounded then 

$$ Av \leq 0, \ \ \ \ \text{for some v satisfying }c^Tv>0$$


Since for any v' satisfying $c^Tv' \leq 0 $  and $t\leq 0$ we always have $c^Tx_0 + tc^Tv' \geq c^Tx_0$. Therefore we only consider the case that $c^Tv> 0$ to maximize the objective value.  we change the objective function as 

$$ \min\ z = \inf_{t\in (-\infty,0] \ \ c^Tv>0 }c^Tx_0 + tc^Tv$$


Then if $\min\ z$ is unbounded, it requires that there exist some $v$, which satisfying $c^Tv>0$, and $x_0 + tv$ is feasible even $t\to \infty$. Since $ tAv\geq b- Ax_0$ for $t\to -\infty$, then  $Av\leq 0$. Conversely, if there is some v satisfying that $c^Tv >0$ and $Av\leq 0$,  in this direction, t could be $-\infty$, then $\min\ z$ is unbounded.

The argument also requires that if $\min z$ is bounded with feasible solutions, then
$$\text{for any v with } c^Tv>0\text{. there shall be some component that }(Av)_j >0$$
As a result, t will always be limited  in this direction. Since $t$ is limited in every v with $c^Tv>0$, which means the objective is finite for all v, then the objective is finite. Conversely, if the objective value is finite, t should be limited for each direction that $c^Tv$=0, where limitation means some component of $Av$ is positive

In summary, $\textbf{if Eq2 is feasible}$,

$$ \text{Eq2 is unbounded below } \Longleftrightarrow  Av \leq 0, \ \ \ \ \text{for some v satisfying }c^Tv>0$$

$$ \text{Eq2 has a finite optimal solution } \Longleftrightarrow  \text{for any v with } c^Tv>0\text{. there shall be some component that }(Av)_j >0$$

(1)

The Lagrange dual function of (1) is 

$$g_1(y) = \sup_x c^T x + y^T(b-Ax) = \sup_x (c^T -y^TA) x + y^T b  = \left\{\begin{array}{cl}
y^Tb, &  c^T -y^TA=0\\
+\infty, & otherwise\end{array}\right. $$
where $y$ must be positive. Then the dual function of (1) is


$$\begin{array}{cl}
\min& b^Ty\\
s.t. &y\in D\end{array}$$

where $ D =\{y\mid A^Ty=c,y\succeq 0\}$.

The Lagrange dual function of (2) is 

$$g_2(y) = \inf_x c^T x + y^T(b-Ax) = \inf_x\ (c^T -y^TA) x + y^T b  = \left\{\begin{array}{cl}
y^Tb, &  c^T -y^TA=0\\
-\infty, & otherwise\end{array}\right. $$
where $y$ must be positive. Then the dual function of (2) is

$$\begin{array}{cl}
\max& b^Ty\\
s.t. &y \in D\end{array}$$

(2) From the results we comment at the begining, if both are feasible and one of them has a finite optimal solution,  then $\text{for any v with } c^Tv>0\text{. there shall be some component that }(Av)_j >0$. Accordinly the other will also have a finite optimal value.

(3) If both are feasible, if Eq1 is unbounded above, then $Av \leq 0, \ \ \ \ \text{for some v satisfying }c^Tv>0$. Accordingly, the second objective is unbounded below. In same way, we could verify that if  the second objective is unbounded below, Eq1 is unbounded above.

(4) Suppose there exist solutions such that $c^Tx>c^T\hat{x}$, $Ax\leq b$, and $Ax\geq b$. Then we could construct a solution $y=e_{x-\hat{x}}$， which a unit vector along the dirction of $x-\hat{x}$. Then $c^Ty >0$ and $Ay \leq 0$. From the comments at the begining, this solution means that  both shall be unbounded, which are  in conflict to the assumption. Therefore, $c^Tx\leq c^T\hat{x}$

