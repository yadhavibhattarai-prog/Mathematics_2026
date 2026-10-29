# Exercise 11. A Parameter in a System of Three Equations

Analyze the number of solutions depending on $t$:

$$
\begin{cases}
x+y+z=1, \\
x+ty+z=2, \\
x+y+tz=3.
\end{cases}
$$

Use elimination and separately analyze the parameter values for which a standard calculation step ceases to be valid.

## Solution

Subtract the first equation from the second and third:

$$
(t-1)y=1,\qquad (t-1)z=2.
$$

If $t=1$, these become $0=1$ and $0=2$, so the system is inconsistent and has no solution. This is precisely the value at which dividing by the elimination coefficient $t-1$ is not valid.

If $t\ne1$, then

$$
y=\frac{1}{t-1},\qquad z=\frac{2}{t-1},\qquad
x=1-y-z=1-\frac{3}{t-1}.
$$

Thus for every $t\ne1$ there is exactly one solution, namely

$$
\left(1-\frac{3}{t-1},\frac{1}{t-1},\frac{2}{t-1}\right).
$$