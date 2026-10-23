### Exercise 6. Solving a System Using the Inverse
Solve

$$
Ax=b,
$$

where

$$
A=
\begin{pmatrix}
2 & 1 \\
1 & 3 \\
\end{pmatrix},\qquad b=
\begin{pmatrix}
5 \\
7 \\
\end{pmatrix},
$$

using $x=A^{-1}b$. Then substitute the resulting vector back into the equation and check the result.

> **Why this exercise:** shows the connection between inverse matrices and solving a linear system.

## Solution

### 1. Computation of the Inverse Matrix $A^{-1}$

For the matrix

$$
A=
\begin{pmatrix}
2 & 1 \\
1 & 3 \\
\end{pmatrix}
$$

compute the determinant:

$$
\det A = 2\cdot 3 - 1\cdot 1 = 6 - 1 = 5
$$

Since $\det A = 5 \neq 0$, the inverse exists and is given by the $2\times 2$ formula:

$$
A^{-1} = \frac{1}{\det A}
\begin{pmatrix}
d & -b \\
-c & a \\
\end{pmatrix}
= \frac{1}{5}
\begin{pmatrix}
3 & -1 \\
-1 & 2 \\
\end{pmatrix}
$$

### 2. Solving the System via $x = A^{-1}b$

Multiplying $A^{-1}$ by the right-hand side vector $b$:

$$
\begin{aligned}
x &= A^{-1}b \\
&= \frac{1}{5}
\begin{pmatrix}
3 & -1 \\
-1 & 2 \\
\end{pmatrix}
\begin{pmatrix}
5 \\
7 \\
\end{pmatrix} \\
&= \frac{1}{5}
\begin{pmatrix}
3\cdot 5 + (-1)\cdot 7 \\
(-1)\cdot 5 + 2\cdot 7 \\
\end{pmatrix} \\
&= \frac{1}{5}
\begin{pmatrix}
15 - 7 \\
-5 + 14 \\
\end{pmatrix} \\
&= \frac{1}{5}
\begin{pmatrix}
8 \\
9 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
\frac{8}{5} \\
\frac{9}{5} \\
\end{pmatrix}
\end{aligned}
$$

The solution to the system is

$$
x =
\begin{pmatrix}
\frac{8}{5} \\
\frac{9}{5} \\
\end{pmatrix}
$$

### 3. Verification by Substitution

Substitute $x$ back into the original matrix equation $Ax$:

$$
\begin{aligned}
Ax &=
\begin{pmatrix}
2 & 1 \\
1 & 3 \\
\end{pmatrix}
\begin{pmatrix}
\frac{8}{5} \\
\frac{9}{5} \\
\end{pmatrix} \\
&=
\begin{pmatrix}
2\left(\frac{8}{5}\right) + 1\left(\frac{9}{5}\right) \\
1\left(\frac{8}{5}\right) + 3\left(\frac{9}{5}\right) \\
\end{pmatrix} \\
&=
\begin{pmatrix}
\frac{16 + 9}{5} \\
\frac{8 + 27}{5} \\
\end{pmatrix} \\
&=
\begin{pmatrix}
\frac{25}{5} \\
\frac{35}{5} \\
\end{pmatrix} \\
&=
\begin{pmatrix}
5 \\
7 \\
\end{pmatrix} \\
&= b
\end{aligned}
$$

The substitution yields exactly $b$, confirming that the solution vector $x = \begin{pmatrix} \frac{8}{5} \\ \frac{9}{5} \\ \end{pmatrix}$ is correct.

