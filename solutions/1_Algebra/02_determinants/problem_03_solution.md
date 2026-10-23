### Exercise 3. Swapping Two Rows
For

$$
A=
\begin{pmatrix}
1 & 2 & 0 \\
0 & 3 & 1 \\
2 & 1 & 1 \\
\end{pmatrix}
$$

compute $\det A$. Then form a matrix $B$ by swapping the first and second rows of $A$.

First predict $\det B$ using a determinant property, and then verify your prediction by calculation.

> **Why this exercise:** gives a second classical calculation with a $3\times3$ determinant while teaching the precise effect of a row swap on the sign of the determinant.

## Solution

### 1. Computation of $\det A$

Expanding along the first column of $A$:

$$
\det A = 1\cdot \det
\begin{pmatrix}
3 & 1 \\
1 & 1 \\
\end{pmatrix}
- 0\cdot \det
\begin{pmatrix}
2 & 0 \\
1 & 1 \\
\end{pmatrix}
+ 2\cdot \det
\begin{pmatrix}
2 & 0 \\
3 & 1 \\
\end{pmatrix}
$$

Evaluating the $2\times 2$ determinants:

$$
\det
\begin{pmatrix}
3 & 1 \\
1 & 1 \\
\end{pmatrix}
= 3\cdot 1 - 1\cdot 1 = 2
$$

$$
\det
\begin{pmatrix}
2 & 0 \\
3 & 1 \\
\end{pmatrix}
= 2\cdot 1 - 0\cdot 3 = 2
$$

Thus:

$$
\det A = 1\cdot 2 + 2\cdot 2 = 2 + 4 = 6
$$

### 2. Formation of Matrix $B$ and Prediction

Swapping the first and second rows of $A$ ($R_1 \leftrightarrow R_2$) gives

$$
B=
\begin{pmatrix}
0 & 3 & 1 \\
1 & 2 & 0 \\
2 & 1 & 1 \\
\end{pmatrix}
$$

**Prediction:**
An elementary row operation of type I (swapping two rows) reverses the sign of the determinant. Therefore:

$$
\det B = -\det A = -6
$$

### 3. Verification by Direct Calculation

Expanding along the first column of $B$:

$$
\det B = 0\cdot \det
\begin{pmatrix}
2 & 0 \\
1 & 1 \\
\end{pmatrix}
- 1\cdot \det
\begin{pmatrix}
3 & 1 \\
1 & 1 \\
\end{pmatrix}
+ 2\cdot \det
\begin{pmatrix}
3 & 1 \\
2 & 0 \\
\end{pmatrix}
$$

Evaluating the nonzero terms:

$$
\det
\begin{pmatrix}
3 & 1 \\
1 & 1 \\
\end{pmatrix}
= 3\cdot 1 - 1\cdot 1 = 2
$$

$$
\det
\begin{pmatrix}
3 & 1 \\
2 & 0 \\
\end{pmatrix}
= 3\cdot 0 - 1\cdot 2 = -2
$$

Substituting these values into the expansion gives

$$
\det B = -1\cdot 2 + 2\cdot (-2) = -2 - 4 = -6
$$

The direct calculation verifies the prediction: $\det B = -6$.

