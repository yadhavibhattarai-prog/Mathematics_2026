### Exercise 14. A System of Equations and the Determinant
Consider the system $Ax=b$, where

$$
A=
\begin{pmatrix}
1 & 2 \\
k & 4 \\
\end{pmatrix}.
$$

For which values of $k$ does the system have exactly one solution for every $b$? For the remaining value, give an example of a right-hand side $b$ for which the system has infinitely many solutions, and an example for which it has no solution.

> **Why this exercise:** connects the determinant with uniqueness of solutions and requires distinguishing the exceptional cases.

## Solution

### 1. Condition for a Unique Solution

The determinant of the coefficient matrix $A$ is

$$
\det A = 1\cdot 4 - 2\cdot k = 4 - 2k
$$

By Cramer's rule and the Invertible Matrix Theorem, the linear system $Ax = b$ has a unique solution for every right-hand side vector $b \in \mathbb{R}^2$ if and only if the matrix $A$ is invertible, which holds precisely when its determinant is nonzero:

$$
\det A \neq 0 \iff 4 - 2k \neq 0 \iff k \neq 2
$$

Therefore, the system has exactly one solution for every $b$ when $k \in \mathbb{R} \setminus \{2\}$. In this case, the solution is uniquely given by $x = A^{-1}b$.

### 2. Analysis of the Singular Case $k = 2$

For the remaining value $k = 2$, the determinant is zero ($\det A = 0$), and the matrix is

$$
A=
\begin{pmatrix}
1 & 2 \\
2 & 4 \\
\end{pmatrix}
$$

Let the right-hand side vector be

$$
b=
\begin{pmatrix}
b_1 \\
b_2 \\
\end{pmatrix}
$$

The system $Ax = b$ in equation form is

$$
\begin{cases}
x_1 + 2x_2 = b_1, \\
2x_1 + 4x_2 = b_2. \\
\end{cases}
$$

Multiplying the first equation by 2 yields the left-hand side of the second equation:

$$
2(x_1 + 2x_2) = 2x_1 + 4x_2
$$

Hence, the system is consistent if and only if $b_2 = 2b_1$.

### 3. Example with Infinitely Many Solutions

Choose a right-hand side vector satisfying $b_2 = 2b_1$, for example:

$$
b=
\begin{pmatrix}
1 \\
2 \\
\end{pmatrix}
$$

The system becomes

$$
\begin{cases}
x_1 + 2x_2 = 1, \\
2x_1 + 4x_2 = 2. \\
\end{cases}
$$

Dividing the second equation by 2 produces the first equation. Thus, the system reduces to the single linear equation $x_1 + 2x_2 = 1$. The solutions are given in parametric form by

$$
x_1 = 1 - 2t, \qquad x_2 = t, \qquad t \in \mathbb{R}
$$

which describes a line in $\mathbb{R}^2$ containing infinitely many solutions.

### 4. Example with No Solution

Choose a right-hand side vector where $b_2 \neq 2b_1$, for example:

$$
b=
\begin{pmatrix}
1 \\
0 \\
\end{pmatrix}
$$

The system becomes

$$
\begin{cases}
x_1 + 2x_2 = 1, \\
2x_1 + 4x_2 = 0. \\
\end{cases}
$$

Multiplying the first equation by 2 gives $2x_1 + 4x_2 = 2$. Comparing this with the second equation gives the contradiction $2 = 0$.

Therefore, this system is inconsistent and has no solution.

