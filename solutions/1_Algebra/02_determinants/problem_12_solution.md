### Exercise 12. A Parameter Revealed by a Row Operation
For

$$
A(t)=
\begin{pmatrix}
1 & 2 & 3 \\
2 & 4 & t \\
0 & 1 & 1 \\
\end{pmatrix}
$$

find the values of $t$ for which the matrix is not invertible.

Before computing the determinant, perform the operation

$$
R_2\leftarrow R_2-2R_1
$$

and use the resulting structure. At the end, explain what special thing happens to the rows for the value of the parameter you found.

> **Why this exercise:** combines a parameter, row operations, and recognition of dependence in one short argument.

## Solution

### 1. Performing the Row Operation

Starting with

$$
A(t)=
\begin{pmatrix}
1 & 2 & 3 \\
2 & 4 & t \\
0 & 1 & 1 \\
\end{pmatrix}
$$

apply the elementary row operation $R_2 \leftarrow R_2 - 2R_1$:

$$
R_2 - 2R_1 = (2 - 2(1), 4 - 2(2), t - 2(3)) = (0, 0, t - 6)
$$

Since row addition preserves the determinant,

$$
\det A(t) =
\det
\begin{pmatrix}
1 & 2 & 3 \\
0 & 0 & t - 6 \\
0 & 1 & 1 \\
\end{pmatrix}
$$

### 2. Computing the Determinant from the Structure

Expand along the first column of the simplified matrix:

$$
\det A(t) = 1\cdot \det
\begin{pmatrix}
0 & t - 6 \\
1 & 1 \\
\end{pmatrix}
- 0 + 0
$$

Evaluating the $2\times 2$ determinant:

$$
\det
\begin{pmatrix}
0 & t - 6 \\
1 & 1 \\
\end{pmatrix}
= 0\cdot 1 - (t - 6)\cdot 1 = -(t - 6) = 6 - t
$$

Thus:

$$
\det A(t) = 6 - t
$$

### 3. Values of $t$ for Noninvertibility

A square matrix is not invertible if and only if its determinant is zero:

$$
\det A(t) = 0 \iff 6 - t = 0 \iff t = 6
$$

The matrix $A(t)$ is not invertible if and only if $t = 6$.

### 4. Structural Behavior of the Rows when $t = 6$

When $t = 6$:
- The second row of the original matrix becomes $R_2 = (2, 4, 6)$.
- The first row is $R_1 = (1, 2, 3)$.

Notice that

$$
R_2 = 2R_1
$$

The second row is an exact scalar multiple of the first row. The rows $R_1$ and $R_2$ are linearly dependent on their own. Under the row operation $R_2 \leftarrow R_2 - 2R_1$, the entire second row reduces to $(0, 0, 0)$, which immediately implies that the matrix has rank at most 2, has determinant 0, and is singular.

