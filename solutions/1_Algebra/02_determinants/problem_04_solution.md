### Exercise 4. Triangular Matrix
Without expanding the determinant, compute

$$
\det
\begin{pmatrix}
2 & 4 & 1 \\
0 & -3 & 5 \\
0 & 0 & 7 \\
\end{pmatrix}.
$$

State the rule for an arbitrary triangular matrix and explain it using this example.

> **Why this exercise:** reinforces an important property of triangular matrices.

## Solution

### 1. Computation of the Determinant

The given matrix is upper triangular because all entries below the main diagonal are zero:

$$
T=
\begin{pmatrix}
2 & 4 & 1 \\
0 & -3 & 5 \\
0 & 0 & 7 \\
\end{pmatrix}
$$

The determinant is the product of the entries on the main diagonal:

$$
\det T = 2\cdot (-3)\cdot 7 = -42
$$

### 2. Rule for an Arbitrary Triangular Matrix

Let $T = (t_{ij})$ be an $n\times n$ matrix that is upper triangular ($t_{ij} = 0$ for all $i > j$) or lower triangular ($t_{ij} = 0$ for all $i < j$).

The determinant of $T$ is the product of its diagonal entries:

$$
\det T = \prod_{i=1}^n t_{ii} = t_{11}t_{22}\cdots t_{nn}
$$

This property also applies to diagonal matrices, which are both upper and lower triangular.

### 3. Explanation using the Example

This rule follows from successive cofactor expansions:

1. Expand along the first column of $T$. Because the second and third entries in column 1 are zero, only the diagonal entry $t_{11} = 2$ contributes:

$$
\det T = 2\cdot \det
\begin{pmatrix}
-3 & 5 \\
0 & 7 \\
\end{pmatrix}
$$

2. The remaining $2\times 2$ matrix is also upper triangular. Expanding along its first column (or applying the $2\times 2$ formula $(-3)\cdot 7 - 5\cdot 0$):

$$
\det
\begin{pmatrix}
-3 & 5 \\
0 & 7 \\
\end{pmatrix}
= (-3)\cdot 7
$$

3. Combining these steps gives

$$
\det T = 2\cdot (-3)\cdot 7 = -42
$$

In an $n\times n$ triangular matrix, repeating this reduction $n$ times always isolates one diagonal entry per step until only the product of all $n$ diagonal entries remains.

