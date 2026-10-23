### Exercise 7. Inverse of a Product
For

$$
A=
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
2 & 0 \\
0 & 3 \\
\end{pmatrix}
$$

compute $(AB)^{-1}$ and $B^{-1}A^{-1}$. Check that the results are the same and explain the meaning of the reversed order.

> **Why this exercise:** reinforces the inverse-of-a-product property and requires its interpretation.

## Solution

### 1. Computation of $(AB)^{-1}$

First, compute the product matrix $AB$:

$$
\begin{aligned}
AB &=
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
2 & 0 \\
0 & 3 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
1\cdot 2 + 1\cdot 0 & 1\cdot 0 + 1\cdot 3 \\
0\cdot 2 + 1\cdot 0 & 0\cdot 0 + 1\cdot 3 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
2 & 3 \\
0 & 3 \\
\end{pmatrix}
\end{aligned}
$$

Compute the determinant of $AB$:

$$
\det(AB) = 2\cdot 3 - 3\cdot 0 = 6
$$

Using the $2\times 2$ inverse formula:

$$
\begin{aligned}
(AB)^{-1} &= \frac{1}{6}
\begin{pmatrix}
3 & -3 \\
0 & 2 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
\frac{1}{2} & -\frac{1}{2} \\
0 & \frac{1}{3} \\
\end{pmatrix}
\end{aligned}
$$

### 2. Computation of $B^{-1}A^{-1}$

Compute $A^{-1}$:
The determinant is $\det A = 1\cdot 1 - 1\cdot 0 = 1$. Thus,

$$
A^{-1} =
\begin{pmatrix}
1 & -1 \\
0 & 1 \\
\end{pmatrix}
$$

Compute $B^{-1}$:
Since $B$ is diagonal with entries $2$ and $3$, its inverse is diagonal with reciprocal entries:

$$
B^{-1} =
\begin{pmatrix}
\frac{1}{2} & 0 \\
0 & \frac{1}{3} \\
\end{pmatrix}
$$

Now evaluate the product $B^{-1}A^{-1}$:

$$
\begin{aligned}
B^{-1}A^{-1} &=
\begin{pmatrix}
\frac{1}{2} & 0 \\
0 & \frac{1}{3} \\
\end{pmatrix}
\begin{pmatrix}
1 & -1 \\
0 & 1 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
\frac{1}{2}\cdot 1 + 0\cdot 0 & \frac{1}{2}\cdot (-1) + 0\cdot 1 \\
0\cdot 1 + \frac{1}{3}\cdot 0 & 0\cdot (-1) + \frac{1}{3}\cdot 1 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
\frac{1}{2} & -\frac{1}{2} \\
0 & \frac{1}{3} \\
\end{pmatrix}
\end{aligned}
$$

### 3. Comparison of Results

Comparing the two matrices:

$$
(AB)^{-1} =
\begin{pmatrix}
\frac{1}{2} & -\frac{1}{2} \\
0 & \frac{1}{3} \\
\end{pmatrix}
= B^{-1}A^{-1}
$$

Both calculations give the exact same matrix.

### 4. Meaning of the Reversed Order

When the product $AB$ acts on a vector $x$:

$$
(AB)x = A(Bx)
$$

The transformation $B$ is applied first, and the transformation $A$ is applied second.

To completely undo this composition:
1. The last applied operation, $A$, must be undone first by applying $A^{-1}$, yielding $A^{-1}(A(Bx)) = Bx$.
2. The initial operation, $B$, is then undone second by applying $B^{-1}$, yielding $B^{-1}(Bx) = x$.

Algebraically, multiplying $(AB)$ by $B^{-1}A^{-1}$ from the left produces the required cancellation:

$$
(B^{-1}A^{-1})(AB) = B^{-1}(A^{-1}A)B = B^{-1} I B = B^{-1}B = I
$$

If the order were not reversed, $A^{-1}B^{-1}AB$ would generally not simplify to $I$ because matrices do not commute.
