# Exercise 3. Inconsistent System

Solve or show that the system is inconsistent:

$$
\begin{cases}
x+2y=3, \\
2x+4y=7.
\end{cases}
$$

Show how the contradiction appears in the matrix after elimination and interpret it in terms of equations.

## Solution

The augmented matrix is

$$
\left(
\begin{array}{cc|c}
1&2&3\\
2&4&7
\end{array}
\right)
\xrightarrow{R_2\leftarrow R_2-2R_1}
\left(
\begin{array}{cc|c}
1&2&3\\
0&0&1
\end{array}
\right).
$$

The second row represents $0x+0y=1$, or $0=1$, which is impossible. In equation form, the left-hand side of the second equation is twice the first equation's left-hand side, so its right-hand side would have to be $2(3)=6$, not $7$. Therefore the system has no solution.