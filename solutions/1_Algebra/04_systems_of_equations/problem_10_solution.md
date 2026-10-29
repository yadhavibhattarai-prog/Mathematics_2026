# Exercise 10. A Polynomial Through Three Points

Find a polynomial $p(x)=ax^2+bx+c$ whose graph passes through $(0,1)$, $(1,3)$, and $(2,9)$. Reduce the problem to a system of equations and check the result by substituting all three points.

## Solution

Substituting the three $x$-coordinates gives

$$
\begin{cases}
c=1,\\
a+b+c=3,\\
4a+2b+c=9.
\end{cases}
$$

From $c=1$, the other equations reduce to $a+b=2$ and $2a+b=4$. Subtracting gives $a=2$, and then $b=0$. Thus

$$
p(x)=2x^2+1.
$$

Checking: $p(0)=1$, $p(1)=3$, and $p(2)=9$, as required.