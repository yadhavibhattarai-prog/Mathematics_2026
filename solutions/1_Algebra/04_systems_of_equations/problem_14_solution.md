# Exercise 14. A Small Change in the Right-Hand Side

Compare the systems

$$
\begin{cases}
x+y=2, \\
2x-y=1, \\
3x=3
\end{cases}
$$

and

$$
\begin{cases}
x+y=2, \\
2x-y=1, \\
3x=3.1.
\end{cases}
$$

Check the consistency of each system and explain why a small change in one number can change the type of the system.

## Solution

Adding the first two equations in either system gives $3x=3$, hence $x=1$ and then $y=1$. In the first system, the third equation agrees with this result, so the system is consistent with the unique solution $(1,1)$.

In the second system, the first two equations still force $x=1$, while the third requires $x=3.1/3=31/30$. These conditions contradict each other, so the system is inconsistent.

The first two equations already determine a single point. The third equation is compatible with that point in the first system but not in the second; even a small change in its right-hand side can therefore turn a consistent system into an inconsistent one.