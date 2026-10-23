### Exercise 15. Two Methods for Solving the Same System
For

$$
A=
\begin{pmatrix}
2 & 1 \\
1 & 3 \\
\end{pmatrix},\qquad b=
\begin{pmatrix}
7 \\
8 \\
\end{pmatrix}
$$

solve $Ax=b$ in two ways:

1. using $A^{-1}b$,
2. using Gaussian elimination.

Compare both solutions, the number of essential steps, and state which method was simpler in this example.

> **Why this exercise:** compares two known methods and prepares the student to choose a solution method consciously.

## Solution

We consider the linear system $Ax = b$ with

$$
A=
\begin{pmatrix}
2 & 1 \\
1 & 3 \\
\end{pmatrix},\qquad b=
\begin{pmatrix}
7 \\
8 \\
\end{pmatrix}
$$

### 1. Method 1: Using the Inverse Matrix $x = A^{-1}b$

**Step 1:** Compute the determinant of $A$:

$$
\det A = 2\cdot 3 - 1\cdot 1 = 6 - 1 = 5
$$

**Step 2:** Form the inverse matrix $A^{-1}$ using the $2\times 2$ formula:

$$
A^{-1} = \frac{1}{5}
\begin{pmatrix}
3 & -1 \\
-1 & 2 \\
\end{pmatrix}
$$

**Step 3:** Multiply $A^{-1}$ by $b$:

$$
\begin{aligned}
x &= A^{-1}b \\
&= \frac{1}{5}
\begin{pmatrix}
3 & -1 \\
-1 & 2 \\
\end{pmatrix}
\begin{pmatrix}
7 \\
8 \\
\end{pmatrix} \\
&= \frac{1}{5}
\begin{pmatrix}
3\cdot 7 + (-1)\cdot 8 \\
(-1)\cdot 7 + 2\cdot 8 \\
\end{pmatrix} \\
&= \frac{1}{5}
\begin{pmatrix}
21 - 8 \\
-7 + 16 \\
\end{pmatrix} \\
&= \frac{1}{5}
\begin{pmatrix}
13 \\
9 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
\frac{13}{5} \\
\frac{9}{5} \\
\end{pmatrix}
\end{aligned}
$$

### 2. Method 2: Using Gaussian Elimination

**Step 1:** Set up the augmented matrix $[A \mid b]$:

$$
\begin{pmatrix}
2 & 1 & \mid & 7 \\
1 & 3 & \mid & 8 \\
\end{pmatrix}
$$

**Step 2:** Swap $R_1 \leftrightarrow R_2$ to obtain a leading entry of $1$ in row 1:

$$
\begin{pmatrix}
1 & 3 & \mid & 8 \\
2 & 1 & \mid & 7 \\
\end{pmatrix}
$$

**Step 3:** Eliminate the entry below the pivot via $R_2 \leftarrow R_2 - 2R_1$:

$$
\begin{pmatrix}
1 & 3 & \mid & 8 \\
2 - 2(1) & 1 - 2(3) & \mid & 7 - 2(8) \\
\end{pmatrix}
=
\begin{pmatrix}
1 & 3 & \mid & 8 \\
0 & -5 & \mid & -9 \\
\end{pmatrix}
$$

**Step 4:** Perform back-substitution:
- From the second row:

$$
-5x_2 = -9 \implies x_2 = \frac{9}{5}
$$

- From the first row:

$$
x_1 + 3x_2 = 8 \implies x_1 = 8 - 3\left(\frac{9}{5}\right) = \frac{40 - 27}{5} = \frac{13}{5}
$$

This gives the solution vector

$$
x =
\begin{pmatrix}
\frac{13}{5} \\
\frac{9}{5} \\
\end{pmatrix}
$$

### 3. Comparison of the Methods

1. **Agreement:** Both methods yield identical solutions: $x_1 = \frac{13}{5}$ and $x_2 = \frac{9}{5}$.
2. **Computational Effort in this Example:**
   - **Inverse Matrix Method:** Requires finding the determinant, forming the adjugate matrix, and computing a matrix-vector product.
   - **Gaussian Elimination:** Requires one row swap, one row elimination, and two back-substitution calculations.
   In this $2\times 2$ example, Gaussian elimination is simpler and involves less overhead because it operates directly on the system constants without needing to construct an explicit full inverse matrix.
3. **General Recommendation:**
   - For solving a single system $Ax = b$, Gaussian elimination is faster and computationally cheaper (requiring roughly $\frac{1}{3}n^3$ operations versus $n^3$ operations for full matrix inversion).
   - The inverse matrix method $x = A^{-1}b$ is advantageous when the same coefficient matrix $A$ must be solved repeatedly for many different right-hand side vectors $b$.

