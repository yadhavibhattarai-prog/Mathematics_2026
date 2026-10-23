### Exercise 11. Shortening the Calculation with Row Operations
Compute

$$
\det
\begin{pmatrix}
1 & 2 & 3 \\
1 & 3 & 4 \\
1 & 4 & 6 \\
\end{pmatrix}
$$

by first performing row operations that create as many zeros as possible. State which operations do not change the determinant.

> **Why this exercise:** develops planning instead of mechanically repeating the same procedure.

## Solution

Let the given matrix be

$$
A=
\begin{pmatrix}
1 & 2 & 3 \\
1 & 3 & 4 \\
1 & 4 & 6 \\
\end{pmatrix}
$$

### 1. Operations that Do Not Change the Determinant

Row replacement operations of the form

$$
R_i \leftarrow R_i + cR_j \quad (i \neq j)
$$

where a scalar multiple of row $j$ is added to row $i$, leave the determinant completely unchanged.

### 2. Creating Zeros in the Matrix

**Step 1:** Use the first row to eliminate the leading entries in rows 2 and 3:

- Apply $R_2 \leftarrow R_2 - R_1$:
  $R_2 = (1 - 1, 3 - 2, 4 - 3) = (0, 1, 1)$.

- Apply $R_3 \leftarrow R_3 - R_1$:
  $R_3 = (1 - 1, 4 - 2, 6 - 3) = (0, 2, 3)$.

Both operations preserve the determinant, giving

$$
A_1=
\begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
0 & 2 & 3 \\
\end{pmatrix}
$$

with $\det A = \det A_1$.

**Step 2:** Use the second row to create a zero in row 3, column 2:

- Apply $R_3 \leftarrow R_3 - 2R_2$:
  $R_3 = (0 - 0, 2 - 2, 3 - 2) = (0, 0, 1)$.

This operation also preserves the determinant, producing the upper triangular matrix

$$
U=
\begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
0 & 0 & 1 \\
\end{pmatrix}
$$

with $\det A = \det U$.

### 3. Computation of the Determinant

The matrix $U$ is in upper triangular form. The determinant of an upper triangular matrix equals the product of its diagonal entries:

$$
\det U = 1\cdot 1\cdot 1 = 1
$$

Therefore:

$$
\det A = 1
$$

