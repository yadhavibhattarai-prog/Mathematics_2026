# Exercise 8. Two Systems with the Same Coefficient Matrix

Solve by elimination the two systems

$$
\begin{cases}
2x+y=5, \\
x-y=1,
\end{cases}
$$

$$
\begin{cases}
2x+y=1, \\
x-y=4.
\end{cases}
$$

Compare the successive elimination steps. Which part of the calculation is the same in both cases, and why?

## Solution

For the first system, add the equations to eliminate $y$:

$$
3x=6,\qquad x=2.
$$

Then $x-y=1$ gives $y=1$, so $(x,y)=(2,1)$.

For the second system, the same addition eliminates $y$:

$$
3x=5,\qquad x=\frac53.
$$

Then $x-y=4$ gives $y=x-4=-\frac73$, so $(x,y)=(\frac53,-\frac73)$.

The elimination operation and resulting left-hand side $3x$ are the same because the coefficient matrices are identical. Only the right-hand sides change, so the resulting constants differ.