### Exercise 4. Matrix Multiplication and Noncommutativity

Given:

$$
A=
\begin{pmatrix}
1 & 2 \\
0 & 1
\end{pmatrix},
\qquad
B=
\begin{pmatrix}
2 & 0 \\
3 & 1
\end{pmatrix}
$$

**Step 1: Calculate $AB$**

$$
AB=
\begin{pmatrix}
1 & 2 \\
0 & 1
\end{pmatrix}
\begin{pmatrix}
2 & 0 \\
3 & 1
\end{pmatrix}
$$

Multiply the rows of $A$ by the columns of $B$:

$$
AB=
\begin{pmatrix}
(1)(2)+(2)(3) & (1)(0)+(2)(1) \\
(0)(2)+(1)(3) & (0)(0)+(1)(1)
\end{pmatrix}
$$

Therefore,

$$
\boxed{
AB=
\begin{pmatrix}
8 & 2 \\
3 & 1
\end{pmatrix}
}
$$

**Step 2: Calculate $BA$**

$$
BA=
\begin{pmatrix}
2 & 0 \\
3 & 1
\end{pmatrix}
\begin{pmatrix}
1 & 2 \\
0 & 1
\end{pmatrix}
$$

Multiply the rows of $B$ by the columns of $A$:

$$
BA=
\begin{pmatrix}
(2)(1)+(0)(0) & (2)(2)+(0)(1) \\
(3)(1)+(1)(0) & (3)(2)+(1)(1)
\end{pmatrix}
$$

Therefore,

$$
\boxed{
BA=
\begin{pmatrix}
2 & 4 \\
3 & 7
\end{pmatrix}
}
$$

**Step 3: Compare $AB$ and $BA$**

We have:

$$
AB=
\begin{pmatrix}
8 & 2 \\
3 & 1
\end{pmatrix}
$$

$$
BA=
\begin{pmatrix}
2 & 4 \\
3 & 7
\end{pmatrix}
$$

Since the corresponding entries are different,

$$
\boxed{AB\neq BA}
$$

**Conclusion: Noncommutativity of Matrix Multiplication**

Noncommutativity means that changing the order of multiplication can produce a different result. In this example, $AB$ is not equal to $BA$.

Unlike ordinary multiplication of numbers, where $2\times3=3\times2$, matrix multiplication generally does not satisfy the commutative property.

Therefore, **matrix multiplication is generally noncommutative**, meaning that $AB\neq BA$ in many cases.
