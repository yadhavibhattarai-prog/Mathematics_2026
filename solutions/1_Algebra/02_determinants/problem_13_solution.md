### Exercise 13. Determinant by Elimination
Compute the determinant

$$
A=
\begin{pmatrix}
1 & 2 & 3 \\
2 & 5 & 7 \\
1 & 0 & 2 \\
\end{pmatrix}
$$

using elimination. Record the effect of every row operation used on the value of the determinant.

> **Why this exercise:** reinforces organizing a determinant calculation through row operations without introducing an unnecessary second procedure.

## Solution

Gaussian elimination transforms matrix $A$ into an upper triangular matrix $U$ using elementary row operations:

$$
A=
\begin{pmatrix}
1 & 2 & 3 \\
2 & 5 & 7 \\
1 & 0 & 2 \\
\end{pmatrix}
$$

### 1. Step-by-Step Elimination

**Step 1:** Clear the entries in column 1 below the pivot $a_{11} = 1$:

- Apply $R_2 \leftarrow R_2 - 2R_1$:
  *New row 2:* $(2 - 2(1), 5 - 2(2), 7 - 2(3)) = (0, 1, 1)$.
  *Effect on determinant:* Type III operation (row replacement) leaves the determinant unchanged (multiplier $= 1$).

- Apply $R_3 \leftarrow R_3 - R_1$:
  *New row 3:* $(1 - 1, 0 - 2, 2 - 3) = (0, -2, -1)$.
  *Effect on determinant:* Type III operation leaves the determinant unchanged (multiplier $= 1$).

The resulting matrix is

$$
A_1=
\begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
0 & -2 & -1 \\
\end{pmatrix}
$$

with $\det A = \det A_1$.

**Step 2:** Clear the entry in column 2 below the pivot $a_{22} = 1$:

- Apply $R_3 \leftarrow R_3 + 2R_2$:
  *New row 3:* $(0 + 2(0), -2 + 2(1), -1 + 2(1)) = (0, 0, 1)$.
  *Effect on determinant:* Type III operation leaves the determinant unchanged (multiplier $= 1$).

The resulting matrix is in upper triangular form:

$$
U=
\begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
0 & 0 & 1 \\
\end{pmatrix}
$$

with $\det A = \det U$.

### 2. Summary of Row Operation Effects

| Step | Operation | Operation Type | Multiplier on Determinant |
| :--- | :--- | :--- | :--- |
| 1 | $R_2 \leftarrow R_2 - 2R_1$ | Row addition | $1$ |
| 1 | $R_3 \leftarrow R_3 - R_1$ | Row addition | $1$ |
| 2 | $R_3 \leftarrow R_3 + 2R_2$ | Row addition | $1$ |

### 3. Computation of the Determinant

The determinant of the triangular matrix $U$ is the product of its diagonal entries:

$$
\det U = 1\cdot 1\cdot 1 = 1
$$

Since the cumulative product of multipliers from all row operations is $1\cdot 1\cdot 1 = 1$:

$$
\det A = \det U = 1
$$

