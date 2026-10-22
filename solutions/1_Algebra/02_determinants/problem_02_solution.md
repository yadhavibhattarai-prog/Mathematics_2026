### Exercise 2. Determinant of a 3×3 Matrix
For

$$
A=
\begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 4 \\
2 & 1 & 5 \\
\end{pmatrix}
$$

compute $\det A$ using Sarrus' rule. Then perform one simple check using a chosen property of the determinant.

> **Why this exercise:** teaches a basic method for $3\times3$ matrices and builds the habit of checking the result without adding a second full solution.
>
> ### Exercise 2. Determinant of a 3×3 Matrix

Given

$$
A=
\begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 4 \\
2 & 1 & 5
\end{pmatrix},
$$

compute $\det A$ using Sarrus' rule and check the result.

## Solution Using Sarrus' Rule

Repeat the first two columns to the right:

$$
\begin{array}{ccc|cc}
1 & 2 & -1 & 1 & 2 \\
0 & 3 & 4  & 0 & 3 \\
2 & 1 & 5  & 2 & 1
\end{array}
$$

Sum the products along the diagonals that go down and to the right:

$$
(1)(3)(5)+(2)(4)(2)+(-1)(0)(1)
=15+16+0=31.
$$

Sum the products along the diagonals that go up and to the right:

$$
(2)(3)(-1)+(1)(4)(1)+(5)(0)(2)
=-6+4+0=-2.
$$

Subtract the second sum from the first:

$$
\det(A)=31-(-2)=\boxed{33}.
$$

## Check Using a Row-Operation Property

Adding a multiple of one row to another does not change the determinant. Apply the operation $R_3\leftarrow R_3-2R_1$:

$$
\begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 4 \\
2 & 1 & 5
\end{pmatrix}
\longrightarrow
\begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 4 \\
0 & -3 & 7
\end{pmatrix}.
$$

Expand the new determinant along the first column:

$$
\det(A)
=
\begin{vmatrix}
3 & 4 \\
-3 & 7
\end{vmatrix}
=(3)(7)-(4)(-3)=21+12=33.
$$

The check agrees with Sarrus' rule. Therefore,

$$
\boxed{\det(A)=33}.
$$