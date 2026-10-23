### Exercise 5. Row Operations
For

$$
A=
\begin{pmatrix}
1 & 2 & 3 \\
2 & 1 & 0 \\
-1 & 4 & 2 \\
\end{pmatrix}
$$

find $\det A$ by simplifying the matrix with row operations. At each step, indicate whether and how the determinant changes.

> **Why this exercise:** connects determinants with row operations and requires conscious tracking of every step.

## Solution

### 1. Effect of Elementary Row Operations on Determinants

- **Type I (Row Swap):** $R_i \leftrightarrow R_j$ multiplies the determinant by $-1$.
- **Type II (Row Scaling):** $R_i \leftarrow cR_i$ with $c \neq 0$ multiplies the determinant by $c$.
- **Type III (Row Addition):** $R_i \leftarrow R_i + cR_j$ with $i \neq j$ leaves the determinant unchanged.

### 2. Step-by-Step Row Simplification

Starting matrix:

$$
A=
\begin{pmatrix}
1 & 2 & 3 \\
2 & 1 & 0 \\
-1 & 4 & 2 \\
\end{pmatrix}
$$

**Step 1:** Eliminate the entries below the first pivot $a_{11} = 1$:

- Perform $R_2 \leftarrow R_2 - 2R_1$.
  *Determinant change:* None (Type III operation).
  *New row 2:* $(2 - 2, 1 - 4, 0 - 6) = (0, -3, -6)$.

- Perform $R_3 \leftarrow R_3 + R_1$.
  *Determinant change:* None (Type III operation).
  *New row 3:* $(-1 + 1, 4 + 2, 2 + 3) = (0, 6, 5)$.

The matrix becomes

$$
A_1=
\begin{pmatrix}
1 & 2 & 3 \\
0 & -3 & -6 \\
0 & 6 & 5 \\
\end{pmatrix}
$$

with $\det A_1 = \det A$.

**Step 2:** Eliminate the entry below the second pivot $a_{22} = -3$:

- Perform $R_3 \leftarrow R_3 + 2R_2$.
  *Determinant change:* None (Type III operation).
  *New row 3:* $(0 + 0, 6 + 2(-3), 5 + 2(-6)) = (0, 0, -7)$.

The matrix becomes upper triangular:

$$
U=
\begin{pmatrix}
1 & 2 & 3 \\
0 & -3 & -6 \\
0 & 0 & -7 \\
\end{pmatrix}
$$

with $\det U = \det A_1 = \det A$.

### 3. Evaluation of the Determinant

Since $U$ is upper triangular, its determinant equals the product of its diagonal entries:

$$
\det U = 1\cdot (-3)\cdot (-7) = 21
$$

Because every row operation performed was of Type III, the determinant was preserved at each step:

$$
\det A = 21
$$

