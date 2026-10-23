### Exercise 2. Formula for a 2×2 Matrix
Find the inverse of

$$
A=
\begin{pmatrix}
3 & 2 \\
5 & 4 \\
\end{pmatrix}
$$

using the formula for a $2\times2$ matrix. At the end, check the result by computing one product with $A$.

> **Why this exercise:** teaches the simplest explicit formula for an inverse and requires verification using the definition.

## Solution

### 1. General Formula for the Inverse of a $2\times 2$ Matrix

For a general $2\times 2$ matrix

$$
M=
\begin{pmatrix}
a & b \\
c & d \\
\end{pmatrix}
$$

its determinant is $\det M = ad - bc$. If $\det M \neq 0$, the inverse matrix is given by

$$
M^{-1} = \frac{1}{\det M}
\begin{pmatrix}
d & -b \\
-c & a \\
\end{pmatrix}
= \frac{1}{ad - bc}
\begin{pmatrix}
d & -b \\
-c & a \\
\end{pmatrix}
$$

### 2. Computation of the Inverse of $A$

For the matrix

$$
A=
\begin{pmatrix}
3 & 2 \\
5 & 4 \\
\end{pmatrix}
$$

the coefficients are $a = 3$, $b = 2$, $c = 5$, and $d = 4$.

Evaluating the determinant:

$$
\det A = 3\cdot 4 - 2\cdot 5 = 12 - 10 = 2
$$

Since $\det A = 2 \neq 0$, the inverse exists. Applying the formula:

$$
\begin{aligned}
A^{-1} &= \frac{1}{2}
\begin{pmatrix}
4 & -2 \\
-5 & 3 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
2 & -1 \\
-\frac{5}{2} & \frac{3}{2} \\
\end{pmatrix}
\end{aligned}
$$

### 3. Verification by Multiplication

Checking the product $A A^{-1}$:

$$
\begin{aligned}
A A^{-1} &=
\begin{pmatrix}
3 & 2 \\
5 & 4 \\
\end{pmatrix}
\left[\frac{1}{2}
\begin{pmatrix}
4 & -2 \\
-5 & 3 \\
\end{pmatrix}\right] \\
&= \frac{1}{2}
\begin{pmatrix}
3\cdot 4 + 2\cdot (-5) & 3\cdot (-2) + 2\cdot 3 \\
5\cdot 4 + 4\cdot (-5) & 5\cdot (-2) + 4\cdot 3 \\
\end{pmatrix} \\
&= \frac{1}{2}
\begin{pmatrix}
12 - 10 & -6 + 6 \\
20 - 20 & -10 + 12 \\
\end{pmatrix} \\
&= \frac{1}{2}
\begin{pmatrix}
2 & 0 \\
0 & 2 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix} \\
&= I_2
\end{aligned}
$$

Because $A A^{-1} = I_2$, the computed matrix is verified to be the correct inverse:

$$
A^{-1}=
\begin{pmatrix}
2 & -1 \\
-\frac{5}{2} & \frac{3}{2} \\
\end{pmatrix}
$$
