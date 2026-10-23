### Exercise 9. Matrix Equation
Given

$$
A=
\begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
3 & 1 \\
2 & 4 \\
\end{pmatrix}.
$$

Solve the equation $AX=B$ for $X$. Before calculating, decide on which side of the equation $A^{-1}$ must be used. Then check the result by computing $AX$.

> **Why this exercise:** teaches that order matters in matrix equations and must guide the solution.

## Solution

### 1. Determining Which Side to Multiply by $A^{-1}$

In the matrix equation

$$
AX = B
$$

the matrix $A$ appears to the left of the unknown matrix $X$.

Because matrix multiplication is non-commutative in general ($A^{-1}AX \neq XA^{-1}A$), we must multiply both sides of the equation from the left by $A^{-1}$:

$$
A^{-1}(AX) = A^{-1}B \implies (A^{-1}A)X = A^{-1}B \implies IX = A^{-1}B \implies X = A^{-1}B
$$

Multiplying from the right would yield $AXA^{-1} = BA^{-1}$, which does not simplify to isolate $X$.

### 2. Computation of $A^{-1}$

For the upper triangular matrix

$$
A=
\begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix}
$$

the determinant is $\det A = 1\cdot 1 - 2\cdot 0 = 1$.

Using the $2\times 2$ inverse formula:

$$
A^{-1} =
\begin{pmatrix}
1 & -2 \\
0 & 1 \\
\end{pmatrix}
$$

### 3. Solving for $X = A^{-1}B$

Multiplying $A^{-1}$ by $B$:

$$
\begin{aligned}
X &= A^{-1}B \\
&=
\begin{pmatrix}
1 & -2 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
3 & 1 \\
2 & 4 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
1\cdot 3 + (-2)\cdot 2 & 1\cdot 1 + (-2)\cdot 4 \\
0\cdot 3 + 1\cdot 2 & 0\cdot 1 + 1\cdot 4 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
3 - 4 & 1 - 8 \\
2 & 4 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
-1 & -7 \\
2 & 4 \\
\end{pmatrix}
\end{aligned}
$$

### 4. Verification by Computing $AX$

Check the product $AX$:

$$
\begin{aligned}
AX &=
\begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
-1 & -7 \\
2 & 4 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
1\cdot (-1) + 2\cdot 2 & 1\cdot (-7) + 2\cdot 4 \\
0\cdot (-1) + 1\cdot 2 & 0\cdot (-7) + 1\cdot 4 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
-1 + 4 & -7 + 8 \\
2 & 4 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
3 & 1 \\
2 & 4 \\
\end{pmatrix} \\
&= B
\end{aligned}
$$

The product confirms $AX = B$. The unique solution is

$$
X =
\begin{pmatrix}
-1 & -7 \\
2 & 4 \\
\end{pmatrix}
$$
