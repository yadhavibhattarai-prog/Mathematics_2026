# Exercise 4. Infinitely Many Solutions

Solve

$$
\begin{cases}
x+y+z=2, \\
2x+2y+2z=4, \\
x-y+z=0.
\end{cases}
$$

Give the solution in parametric form, identify a free variable, and for one chosen parameter value check that the resulting point really satisfies the system.

## Solution

The second equation is twice the first, so it adds no new condition. Subtract the third equation from the first:

$$
2y=2,\qquad\text{so }y=1.
$$

Substituting into the first gives $x+z=1$. Let the free variable be $z=t$. Then

$$
(x,y,z)=(1-t,1,t),\qquad t\in\mathbb{R}.
$$

For example, with $t=0$ the point is $(1,1,0)$. Substitution gives $1+1+0=2$, $2+2+0=4$, and $1-1+0=0$, so it satisfies all equations.