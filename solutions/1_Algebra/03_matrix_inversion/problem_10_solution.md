### Exercise 10. Inverse of a Diagonal Matrix
Given

$$
D=
\begin{pmatrix}
2 & 0 & 0 \\
0 & -3 & 0 \\
0 & 0 & 5 \\
\end{pmatrix},\qquad E=
\begin{pmatrix}
2 & 0 & 0 \\
0 & 0 & 0 \\
0 & 0 & 5 \\
\end{pmatrix}.
$$

Without using Gauss–Jordan elimination, decide which matrix is invertible. For the invertible matrix, give the inverse and check the result by multiplication.

> **Why this exercise:** teaches how to recognize invertibility and the inverse without using a full procedure when the matrix structure gives the answer immediately.

## Solution

### 1. Invertibility Criterion for Diagonal Matrices

For any diagonal matrix

$$
M = \mathrm{diag}(d_1, d_2, \dots, d_n)
$$

its determinant is the product of its diagonal entries:

$$
\det M = d_1 d_2 \cdots d_n
$$

A diagonal matrix is invertible if and only if all of its diagonal entries are nonzero ($d_i \neq 0$ for all $i$).

- **For matrix $D$:**
  The diagonal entries are $2$, $-3$, and $5$. None of them are zero:

$$
\det D = 2\cdot (-3)\cdot 5 = -30 \neq 0
$$

  Therefore, $D$ is invertible.

- **For matrix $E$:**
  The entry in row 2, column 2 is $0$:

$$
\det E = 2\cdot 0\cdot 5 = 0
$$

  Because the entire second row is zero, the rank of $E$ is at most $2 < 3$, and its determinant is zero. Therefore, $E$ is not invertible.

### 2. Inverse of the Invertible Matrix $D$

For an invertible diagonal matrix, the inverse is formed simply by replacing each diagonal entry with its reciprocal:

$$
D^{-1} =
\begin{pmatrix}
\frac{1}{2} & 0 & 0 \\
0 & -\frac{1}{3} & 0 \\
0 & 0 & \frac{1}{5} \\
\end{pmatrix}
$$

### 3. Verification by Multiplication

Evaluate the product $D D^{-1}$:

$$
\begin{aligned}
D D^{-1} &=
\begin{pmatrix}
2 & 0 & 0 \\
0 & -3 & 0 \\
0 & 0 & 5 \\
\end{pmatrix}
\begin{pmatrix}
\frac{1}{2} & 0 & 0 \\
0 & -\frac{1}{3} & 0 \\
0 & 0 & \frac{1}{5} \\
\end{pmatrix} \\
&=
\begin{pmatrix}
2\cdot \frac{1}{2} & 0 & 0 \\
0 & (-3)\cdot\left(-\frac{1}{3}\right) & 0 \\
0 & 0 & 5\cdot \frac{1}{5} \\
\end{pmatrix} \\
&=
\begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1 \\
\end{pmatrix} \\
&= I_3
\end{aligned}
$$

Because $D D^{-1} = I_3$, the inverse is verified.

