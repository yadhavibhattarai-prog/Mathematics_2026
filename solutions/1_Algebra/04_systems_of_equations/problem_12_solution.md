# Exercise 12. Homogeneous System

Solve

$$
\begin{cases}
x+2y-z=0, \\
2x+4y-2z=0, \\
x-y+2z=0.
\end{cases}
$$

Give all solutions in parametric form and explain why $(0,0,0)$ always satisfies a homogeneous system.

## Solution

The second equation is twice the first, so use the first and third equations. From the first, $x=z-2y$. Substitute into the third:

$$
(z-2y)-y+2z=0
\quad\Longrightarrow\quad
3z-3y=0
\quad\Longrightarrow\quad z=y.
$$

Let $y=t$. Then $z=t$ and $x=-t$, so all solutions are

$$
(x,y,z)=(-t,t,t),\qquad t\in\mathbb{R}.
$$

In any homogeneous system the right-hand side is zero. Setting every variable to zero makes every left-hand side zero as well, so the zero vector always satisfies the system.