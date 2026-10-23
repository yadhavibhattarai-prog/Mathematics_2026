### Exercise 6. Parameter and Invertibility
For

$$
A(t)=
\begin{pmatrix}
t & 1 \\
2 & t \\
\end{pmatrix}
$$

find all values of $t$ for which the matrix is not invertible. Explain how your answer is related to the determinant being zero.

> **Why this exercise:** shows how the determinant can be used to study a family of matrices depending on a parameter.

## Solution

### 1. Computation of the Determinant

For the given $2\times 2$ matrix $A(t)$:

$$
A(t)=
\begin{pmatrix}
t & 1 \\
2 & t \\
\end{pmatrix}
$$

The determinant is

$$
\det A(t) = t\cdot t - 1\cdot 2 = t^2 - 2
$$

### 2. Values of $t$ for Noninvertibility

A square matrix is not invertible (singular) if and only if its determinant is zero:

$$
\det A(t) = 0
$$

Setting the determinant to zero:

$$
t^2 - 2 = 0 \iff t^2 = 2
$$

This yields two values: $t = \sqrt{2}$ and $t = -\sqrt{2}$.

Thus, the matrix $A(t)$ is not invertible precisely when $t \in \{-\sqrt{2}, \sqrt{2}\}$.

### 3. Relation Between Noninvertibility and Zero Determinant

1. **Existence of the Inverse Formula:**
The inverse of an invertible $2\times 2$ matrix $M$ is given by

$$
M^{-1} = \frac{1}{\det M}
\begin{pmatrix}
d & -b \\
-c & a \\
\end{pmatrix}
$$

When $\det M = 0$, division by zero is undefined, and no inverse matrix exists.

2. **Linear Dependence of Rows and Columns:**
A zero determinant means the rows and columns of the matrix are linearly dependent:
- When $t = \sqrt{2}$, row 2 is $(2, \sqrt{2}) = \sqrt{2}(\sqrt{2}, 1) = \sqrt{2}R_1$.
- When $t = -\sqrt{2}$, row 2 is $(2, -\sqrt{2}) = -\sqrt{2}(-\sqrt{2}, 1) = -\sqrt{2}R_1$.

In both cases, the rows are scalar multiples of each other, so the matrix has rank $1 < 2$.

3. **Loss of Injectivity:**
Because the columns are linearly dependent, the equation $A(t)x = 0$ admits nonzero solutions $x \neq 0$. A linear transformation with a nontrivial kernel is not bijective, hence not invertible.
