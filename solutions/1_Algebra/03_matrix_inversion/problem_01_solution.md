### Exercise 1. Definition of the Inverse
For

$$
A=
\begin{pmatrix}
2 & 1 \\
1 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
1 & -1 \\
-1 & 2 \\
\end{pmatrix}
$$

check, without using a formula, whether $B=A^{-1}$. Compute $AB$ and $BA$ and relate the result to the definition of the inverse.

> **Why this exercise:** starts from the definition of the inverse through multiplication before any formulas or computational methods are introduced.

## Solution

### 1. Definition of the Inverse Matrix

Let $A$ be a square matrix of size $n\times n$. An $n\times n$ matrix $B$ is the inverse of $A$ (denoted $B = A^{-1}$) if and only if both products satisfy

$$
AB = I_n, \qquad BA = I_n
$$

where $I_n$ is the $n\times n$ identity matrix.

### 2. Computation of $AB$

Evaluating the product $AB$:

$$
\begin{aligned}
AB &=
\begin{pmatrix}
2 & 1 \\
1 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & -1 \\
-1 & 2 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
2\cdot 1 + 1\cdot (-1) & 2\cdot (-1) + 1\cdot 2 \\
1\cdot 1 + 1\cdot (-1) & 1\cdot (-1) + 1\cdot 2 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
2 - 1 & -2 + 2 \\
1 - 1 & -1 + 2 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}
\end{aligned}
$$

Thus, $AB = I_2$.

### 3. Computation of $BA$

Evaluating the product $BA$:

$$
\begin{aligned}
BA &=
\begin{pmatrix}
1 & -1 \\
-1 & 2 \\
\end{pmatrix}
\begin{pmatrix}
2 & 1 \\
1 & 1 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
1\cdot 2 + (-1)\cdot 1 & 1\cdot 1 + (-1)\cdot 1 \\
(-1)\cdot 2 + 2\cdot 1 & (-1)\cdot 1 + 2\cdot 1 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
2 - 1 & 1 - 1 \\
-2 + 2 & -1 + 2 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}
\end{aligned}
$$

Thus, $BA = I_2$.

### 4. Conclusion

Because both conditions

$$
AB = I_2, \qquad BA = I_2
$$

are fulfilled, matrix $B$ satisfies the definition of the inverse of $A$. Therefore, $B = A^{-1}$.
