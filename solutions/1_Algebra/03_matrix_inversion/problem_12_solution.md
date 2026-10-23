### Exercise 12. Finding Inverses Without Starting from Scratch
It is known that

$$
A^{-1}=
\begin{pmatrix}
2 & -1 \\
-3 & 2 \\
\end{pmatrix}.
$$

Without finding $A$, compute $(3A)^{-1}$, $(A^T)^{-1}$, and $(A^2)^{-1}$. Justify each result using the appropriate property.

> **Why this exercise:** teaches how to use inverse properties instead of carrying out unnecessary full calculations.

## Solution

We are given the inverse matrix directly:

$$
A^{-1}=
\begin{pmatrix}
2 & -1 \\
-3 & 2 \\
\end{pmatrix}
$$

### 1. Computation of $(3A)^{-1}$

**Property:** For any invertible matrix $M$ and any nonzero scalar $c \neq 0$,

$$
(cM)^{-1} = \frac{1}{c} M^{-1}
$$

*Justification:* $(cM)\left(\frac{1}{c} M^{-1}\right) = \left(c \cdot \frac{1}{c}\right)(M M^{-1}) = 1 \cdot I = I$.

Applying this property with $c = 3$ and $M = A$:

$$
\begin{aligned}
(3A)^{-1} &= \frac{1}{3} A^{-1} \\
&= \frac{1}{3}
\begin{pmatrix}
2 & -1 \\
-3 & 2 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
\frac{2}{3} & -\frac{1}{3} \\
-1 & \frac{2}{3} \\
\end{pmatrix}
\end{aligned}
$$

### 2. Computation of $(A^T)^{-1}$

**Property:** Transposition and matrix inversion commute:

$$
(A^T)^{-1} = (A^{-1})^T
$$

*Justification:* Using the transpose-of-a-product rule $(MN)^T = N^T M^T$, we have $(A^{-1})^T A^T = (A A^{-1})^T = I^T = I$.

Applying this property:

$$
\begin{aligned}
(A^T)^{-1} &= (A^{-1})^T \\
&=
\begin{pmatrix}
2 & -1 \\
-3 & 2 \\
\end{pmatrix}^T \\
&=
\begin{pmatrix}
2 & -3 \\
-1 & 2 \\
\end{pmatrix}
\end{aligned}
$$

### 3. Computation of $(A^2)^{-1}$

**Property:** For any positive integer $k$, the inverse of a matrix power equals the power of the inverse:

$$
(A^k)^{-1} = (A^{-1})^k
$$

*Justification:* Applying the product inverse rule $(MN)^{-1} = N^{-1}M^{-1}$ with $M = N = A$ yields $(A^2)^{-1} = (A\cdot A)^{-1} = A^{-1}A^{-1} = (A^{-1})^2$.

Applying this property with $k = 2$:

$$
\begin{aligned}
(A^2)^{-1} &= (A^{-1})^2 \\
&=
\begin{pmatrix}
2 & -1 \\
-3 & 2 \\
\end{pmatrix}
\begin{pmatrix}
2 & -1 \\
-3 & 2 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
2\cdot 2 + (-1)\cdot (-3) & 2\cdot (-1) + (-1)\cdot 2 \\
(-3)\cdot 2 + 2\cdot (-3) & (-3)\cdot (-1) + 2\cdot 2 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
4 + 3 & -2 - 2 \\
-6 - 6 & 3 + 4 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
7 & -4 \\
-12 & 7 \\
\end{pmatrix}
\end{aligned}
$$
