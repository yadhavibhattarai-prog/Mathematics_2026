# Exercise 5. Row Echelon Form and Number of Solutions

For the augmented matrix

$$
\begin{pmatrix}
1 & 2 & -1 & \mid & 3 \\
0 & 1 & 2 & \mid & 1 \\
0 & 0 & 0 & \mid & 0
\end{pmatrix}
$$

determine the number of solutions and write them in parametric form. Explain how you know how many variables may be chosen freely.

## Solution

The rows represent

$$
x+2y-z=3,\qquad y+2z=1,\qquad 0=0.
$$

There is no contradictory row. The pivot columns are those of $x$ and $y$, leaving $z$ free. Set $z=t$. Then $y=1-2t$, and the first equation gives $x+2(1-2t)-t=3$, so $x=1+5t$. Thus there are infinitely many solutions:

$$
(x,y,z)=(1+5t,\,1-2t,\,t),\qquad t\in\mathbb{R}.
$$

There are three variables and two pivot variables, so exactly one variable can be chosen freely.