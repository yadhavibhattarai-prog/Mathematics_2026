### Exercise 2. Determinant of a 3×3 Matrix
For

$$
A=
\begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 4 \\
2 & 1 & 5 \\
\end{pmatrix}
$$

compute $\det A$ using Sarrus' rule. Then perform one simple check using a chosen property of the determinant.

> **Why this exercise:** teaches a basic method for $3\times3$ matrices and builds the habit of checking the result without adding a second full solution.

## Solution

### 1. Computation using Sarrus' Rule

For a $3\times 3$ matrix

$$
A=
\begin{pmatrix}
a_{11} & a_{12} & a_{13} \\
a_{21} & a_{22} & a_{23} \\
a_{31} & a_{32} & a_{33} \\
\end{pmatrix}
$$

Sarrus' rule computes the determinant by summing products along the three main diagonals and subtracting products along the three anti-diagonals:

$$
\det A = a_{11}a_{22}a_{33} + a_{12}a_{23}a_{31} + a_{13}a_{21}a_{32} - a_{13}a_{22}a_{31} - a_{11}a_{23}a_{32} - a_{12}a_{21}a_{33}
$$

Sum of the downward diagonal products:

$$
(1)(3)(5) + (2)(4)(2) + (-1)(0)(1) = 15 + 16 + 0 = 31
$$

Sum of the upward diagonal products:

$$
(-1)(3)(2) + (1)(4)(1) + (2)(0)(5) = -6 + 4 + 0 = -2
$$

Subtracting the second sum from the first gives

$$
\det A = 31 - (-2) = 31 + 2 = 33
$$

### 2. Check using Determinant Properties

Property: Adding a scalar multiple of one row to another row does not change the determinant.

Apply the elementary row operation $R_3 \leftarrow R_3 - 2R_1$:

$$
A_1=
\begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 4 \\
0 & -3 & 7 \\
\end{pmatrix}
$$

Next, apply $R_3 \leftarrow R_3 + R_2$:

$$
U=
\begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 4 \\
0 & 0 & 11 \\
\end{pmatrix}
$$

The matrix $U$ is upper triangular. The determinant of an upper triangular matrix is the product of its diagonal entries:

$$
\det U = 1\cdot 3\cdot 11 = 33
$$

Since row addition preserves the determinant at each step, $\det A = \det U = 33$, which confirms the result obtained by Sarrus' rule.
