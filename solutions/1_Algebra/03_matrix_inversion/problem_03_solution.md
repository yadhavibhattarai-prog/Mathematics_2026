### Exercise 3. When Does the Inverse Not Exist?
For

$$
A=
\begin{pmatrix}
2 & 4 \\
1 & 2 \\
\end{pmatrix}
$$

explain in two ways why $A^{-1}$ does not exist: using the determinant and using dependence between the rows.

> **Why this exercise:** connects two signs of noninvertibility instead of treating them as unrelated facts.

## Solution

### 1. Explanation Using the Determinant

For the given $2\times 2$ matrix

$$
A=
\begin{pmatrix}
2 & 4 \\
1 & 2 \\
\end{pmatrix}
$$

its determinant is

$$
\det A = 2\cdot 2 - 4\cdot 1 = 4 - 4 = 0
$$

By the Invertible Matrix Theorem, a square matrix $M$ is invertible if and only if $\det M \neq 0$. In the explicit inverse formula

$$
M^{-1} = \frac{1}{\det M}
\begin{pmatrix}
d & -b \\
-c & a \\
\end{pmatrix}
$$

a zero determinant requires division by zero, which is undefined. Therefore, $A^{-1}$ does not exist.

### 2. Explanation Using Row Dependence

Denote the row vectors of $A$ by $R_1 = (2, 4)$ and $R_2 = (1, 2)$.

Comparing the two rows:

$$
R_1 = (2, 4) = 2(1, 2) = 2R_2
$$

The first row is an exact scalar multiple of the second row, which gives the non-trivial linear relation

$$
R_1 - 2R_2 = (0, 0)
$$

This linear dependence between the rows implies:

1. **Rank Deficiency:** The row rank of $A$ is $1 < 2$, meaning $A$ does not have full rank.
2. **Loss of Bijectivity:** The linear transformation represented by $A$ collapses the two-dimensional plane $\mathbb{R}^2$ onto a one-dimensional line (the span of $(2, 1)^T$).
3. **Nontrivial Kernel:** There exist nonzero vectors $v \neq 0$ mapped to zero, such as $v = (2, -1)^T$:

$$
\begin{aligned}
Av &=
\begin{pmatrix}
2 & 4 \\
1 & 2 \\
\end{pmatrix}
\begin{pmatrix}
2 \\
-1 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
0 \\
0 \\
\end{pmatrix}
\end{aligned}
$$

Because $A$ is not one-to-one (not injective), no inverse function or inverse matrix can exist to reconstruct the original vectors.
