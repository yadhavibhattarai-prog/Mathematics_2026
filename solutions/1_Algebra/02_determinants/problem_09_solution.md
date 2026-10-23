### Exercise 9. Area and the Determinant
The vectors

$$
u=
\begin{pmatrix}
3 \\
1 \\
\end{pmatrix},\qquad v=
\begin{pmatrix}
1 \\
4 \\
\end{pmatrix}
$$

span a parallelogram. Compute its area using a determinant. Then reverse the order of the vectors and explain what changes in the determinant and what does not change in the area.

> **Why this exercise:** gives the determinant a geometric interpretation and distinguishes its sign from the value of the area.

## Solution

### 1. Computation of Area using a Determinant

The geometric area of the parallelogram spanned by two column vectors $u, v \in \mathbb{R}^2$ equals the absolute value of the determinant of the matrix formed by placing the vectors as columns:

$$
M = (u \mid v) =
\begin{pmatrix}
3 & 1 \\
1 & 4 \\
\end{pmatrix}
$$

Computing the determinant:

$$
\det M = 3\cdot 4 - 1\cdot 1 = 12 - 1 = 11
$$

The area of the parallelogram is

$$
\mathrm{Area} = |\det M| = |11| = 11
$$

### 2. Reversing the Order of Vectors

Placing the vectors in the reverse order yields the matrix

$$
N = (v \mid u) =
\begin{pmatrix}
1 & 3 \\
4 & 1 \\
\end{pmatrix}
$$

Computing the determinant:

$$
\det N = 1\cdot 1 - 3\cdot 4 = 1 - 12 = -11
$$

### 3. Comparison of Determinant and Area

- **What changes in the determinant:**
  The determinant changes its sign from $+11$ to $-11$. Geometrically, the determinant computes the *oriented* (or signed) area. The ordered pair $(u, v)$ has positive (counterclockwise) orientation in the plane, whereas the reversed pair $(v, u)$ has negative (clockwise) orientation. Interchanging two columns corresponds to swapping two columns of a matrix, which multiplies the determinant by $-1$.

- **What does not change in the area:**
  The geometric area of the parallelogram is unchanged:

$$
\mathrm{Area} = |\det N| = |-11| = 11
$$

  Area is a geometric magnitude that depends only on the region enclosed by the two vectors, independent of the order in which the vectors are listed.

