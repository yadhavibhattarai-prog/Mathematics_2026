### Exercise 11. Parameter and Invertibility
For

$$
A(t)=
\begin{pmatrix}
1 & t \\
t & 1 \\
\end{pmatrix}
$$

find all $t$ for which the matrix is invertible, and then give a formula for $A(t)^{-1}$. Explain what happens to this formula at the excluded values.

> **Why this exercise:** combines a parameter, determinant, and an explicit inverse formula in one problem.

## Solution

### 1. Invertibility Condition for $A(t)$

For the parametric matrix

$$
A(t)=
\begin{pmatrix}
1 & t \\
t & 1 \\
\end{pmatrix}
$$

compute the determinant:

$$
\det A(t) = 1\cdot 1 - t\cdot t = 1 - t^2
$$

A square matrix is invertible if and only if its determinant is nonzero:

$$
\det A(t) \neq 0 \iff 1 - t^2 \neq 0 \iff t^2 \neq 1
$$

This requires $t \neq 1$ and $t \neq -1$.

Therefore, the matrix $A(t)$ is invertible for all real numbers $t \in \mathbb{R} \setminus \{-1, 1\}$.

### 2. Formula for the Inverse $A(t)^{-1}$

For $t \neq \pm 1$, applying the $2\times 2$ inverse formula yields

$$
A(t)^{-1} = \frac{1}{\det A(t)}
\begin{pmatrix}
1 & -t \\
-t & 1 \\
\end{pmatrix}
= \frac{1}{1 - t^2}
\begin{pmatrix}
1 & -t \\
-t & 1 \\
\end{pmatrix}
$$

or in entry-by-entry form:

$$
A(t)^{-1} =
\begin{pmatrix}
\frac{1}{1 - t^2} & -\frac{t}{1 - t^2} \\
-\frac{t}{1 - t^2} & \frac{1}{1 - t^2} \\
\end{pmatrix}
$$

### 3. Analysis at the Excluded Values

At the excluded parameter values $t = 1$ and $t = -1$:

1. **Undefined Scalar Factor:**
   The denominator $1 - t^2$ becomes $0$. The scalar factor $\frac{1}{1 - t^2}$ involves division by zero, so the formula is undefined.

2. **Row and Column Linear Dependence:**
   - For $t = 1$:

$$
A(1)=
\begin{pmatrix}
1 & 1 \\
1 & 1 \\
\end{pmatrix}
$$

   Row 1 and Row 2 are identical ($R_1 = R_2$). The rank of $A(1)$ is $1 < 2$.

   - For $t = -1$:

$$
A(-1)=
\begin{pmatrix}
1 & -1 \\
-1 & 1 \\
\end{pmatrix}
$$

   Row 2 is the exact negation of Row 1 ($R_2 = -R_1$). The rank of $A(-1)$ is $1 < 2$.

In both cases, the rows and columns are linearly dependent, the matrix has rank $1$, and the transformation collapses the plane onto a one-dimensional line. Hence, no inverse matrix exists.
