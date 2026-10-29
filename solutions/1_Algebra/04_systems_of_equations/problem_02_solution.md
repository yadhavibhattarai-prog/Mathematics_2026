# Exercise 2. Gaussian Elimination — One Solution

Solve using Gaussian elimination:

$$
\begin{cases}
x+y+z=6, \\
2x-y+z=3, \\
x+2y-z=2.
\end{cases}
$$

After solving, substitute the result into all equations and check consistency.

## Solution

Start with the augmented matrix and eliminate below the first pivot:

$$
\left(
\begin{array}{ccc|c}
1&1&1&6\\
2&-1&1&3\\
1&2&-1&2
\end{array}
\right)
\xrightarrow{R_2\leftarrow R_2-2R_1,\;R_3\leftarrow R_3-R_1}
\left(
\begin{array}{ccc|c}
1&1&1&6\\
0&-3&-1&-9\\
0&1&-2&-4
\end{array}
\right).
$$

Swap the last two rows, then eliminate the $y$-entry in the third row:

$$
\left(
\begin{array}{ccc|c}
1&1&1&6\\
0&1&-2&-4\\
0&-3&-1&-9
\end{array}
\right)
\xrightarrow{R_3\leftarrow R_3+3R_2}
\left(
\begin{array}{ccc|c}
1&1&1&6\\
0&1&-2&-4\\
0&0&-7&-21
\end{array}
\right).
$$

Thus $z=3$, then $y-2z=-4$ gives $y=2$, and $x+y+z=6$ gives $x=1$. The solution is $(x,y,z)=(1,2,3)$. Checking:

$$
1+2+3=6,\qquad 2(1)-2+3=3,\qquad 1+2(2)-3=2.
$$

All three equations are satisfied.