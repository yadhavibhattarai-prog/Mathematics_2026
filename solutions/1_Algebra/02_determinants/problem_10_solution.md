### Exercise 10. Detecting Dependence
Without carrying out a full determinant calculation, explain why

$$
\det
\begin{pmatrix}
1 & 2 & 3 \\
2 & 4 & 6 \\
0 & 1 & 5 \\
\end{pmatrix}=0.
$$

Identify a specific dependence between the rows and connect it with noninvertibility of the matrix.

> **Why this exercise:** teaches how to recognize a zero determinant from the structure of a matrix.

## Solution

Let the given matrix be

$$
A=
\begin{pmatrix}
1 & 2 & 3 \\
2 & 4 & 6 \\
0 & 1 & 5 \\
\end{pmatrix}
$$

and denote its row vectors by $R_1 = (1, 2, 3)$, $R_2 = (2, 4, 6)$, and $R_3 = (0, 1, 5)$.

### 1. Specific Dependence Between the Rows

Comparing the first and second rows:

$$
R_2 = (2, 4, 6) = 2(1, 2, 3) = 2R_1
$$

The second row is an exact scalar multiple of the first row. This produces the nontrivial linear combination

$$
2R_1 - R_2 + 0R_3 = (0, 0, 0)
$$

which proves that the set of rows $\{R_1, R_2, R_3\}$ is linearly dependent.

### 2. Why the Determinant is Zero

1. **Property of Proportional Rows:** If two rows of a square matrix are proportional, the determinant is identically zero.
2. **Row Operation Perspective:** Applying the row operation $R_2 \leftarrow R_2 - 2R_1$ does not alter the determinant:

$$
\det A =
\det
\begin{pmatrix}
1 & 2 & 3 \\
0 & 0 & 0 \\
0 & 1 & 5 \\
\end{pmatrix}
$$

Any matrix with a row consisting entirely of zeros has determinant zero (expanding along the zero row yields $0$).

### 3. Connection with Noninvertibility

According to the Invertible Matrix Theorem, the following conditions are equivalent for an $n\times n$ matrix $A$:
- The matrix $A$ is invertible.
- The determinant $\det A$ is nonzero.
- The rows (and columns) of $A$ are linearly independent.
- The rank of $A$ equals $n$.

Because the rows of $A$ are linearly dependent:
- The rank of $A$ is at most $2 < 3$.
- The linear map $x \mapsto Ax$ is not injective; there exist nonzero vectors $x \neq 0$ such that $Ax = 0$.
- Because $\det A = 0$, the inverse matrix $A^{-1}$ does not exist.

