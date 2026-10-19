### Exercise 1. Determinant of a 2×2 Matrix
Compute

$$
\det
\begin{pmatrix}
3 & -2 \\
5 & 4 \\
\end{pmatrix},\qquad \det
\begin{pmatrix}
1 & 7 \\
2 & 14 \\
\end{pmatrix}.
$$

Which matrix is invertible? Justify your answer.

> **Why this exercise:** introduces the simplest determinant calculation and immediately connects it with invertibility.

### Solution to Exercise 1: Determinant of a 2×2 Matrix

For a 2×2 matrix
$$
\begin{pmatrix}
a & b \\
c & d
\end{pmatrix},
$$
the determinant is
$$
\det = ad - bc.
$$

#### 1) First matrix
$$
A=
\begin{pmatrix}
3 & -2 \\
5 & 4
\end{pmatrix}
$$

So,
$$
\det(A)=3\cdot 4-(-2)\cdot 5=12+10=22.
$$

#### 2) Second matrix
$$
B=
\begin{pmatrix}
1 & 7 \\
2 & 14
\end{pmatrix}
$$

So,
$$
\det(B)=1\cdot 14-7\cdot 2=14-14=0.
$$

#### Which matrix is invertible?
A matrix is invertible if and only if its determinant is nonzero.

- $\det(A)=22 \neq 0$, so matrix $A$ is invertible.
- $\det(B)=0$, so matrix $B$ is not invertible.

Therefore, the matrix
$$
\begin{pmatrix}
3 & -2 \\
5 & 4
\end{pmatrix}
$$
is invertible, while
$$
\begin{pmatrix}
1 & 7 \\
2 & 14
\end{pmatrix}
$$
