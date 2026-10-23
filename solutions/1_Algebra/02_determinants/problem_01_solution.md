### Exercise 1. Determinant of a 2×2 Matrix
Compute

$$
\det
\begin{pmatrix}
3 & -2 \\
5 & 4 \\
\end{pmatrix},\qquad \det
\begin{pmatrix}
1 & 7 \\
2 & 14 \\
\end{pmatrix}.
$$

Which matrix is invertible? Justify your answer.

> **Why this exercise:** introduces the simplest determinant calculation and immediately connects it with invertibility.

## Solution

### 1. Determinant of a $2\times 2$ Matrix

For a general $2\times 2$ matrix

$$
M=
\begin{pmatrix}
a & b \\
c & d \\
\end{pmatrix}
$$

the determinant is defined by the formula

$$
\det M = ad - bc
$$

### 2. Computation for the Given Matrices

For the first matrix:

$$
A=
\begin{pmatrix}
3 & -2 \\
5 & 4 \\
\end{pmatrix}
$$

Evaluating the determinant gives

$$
\det A = 3\cdot 4 - (-2)\cdot 5 = 12 - (-10) = 12 + 10 = 22
$$

For the second matrix:

$$
B=
\begin{pmatrix}
1 & 7 \\
2 & 14 \\
\end{pmatrix}
$$

Evaluating the determinant gives

$$
\det B = 1\cdot 14 - 7\cdot 2 = 14 - 14 = 0
$$

### 3. Invertibility

A square matrix is invertible if and only if its determinant is nonzero ($\det M \neq 0$).

- For matrix $A$: $\det A = 22 \neq 0$, so $A$ is invertible.
- For matrix $B$: $\det B = 0$, so $B$ is not invertible.

The noninvertibility of $B$ can also be seen from its rows: the second row is twice the first row ($R_2 = 2R_1$), which means the rows are linearly dependent.
