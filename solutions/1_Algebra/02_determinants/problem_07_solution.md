### Exercise 7. Using Properties Instead of Recomputing
Suppose that for a $3\times3$ matrix, $\det A=-4$. Compute

$$
\det(2A),\qquad \det(A^T),\qquad \det(A^2),\qquad \det(-A).
$$

Justify each answer using the appropriate property.

> **Why this exercise:** teaches how to use determinant properties instead of repeating a full calculation.

## Solution

The matrix $A$ has size $n = 3$, and its determinant is $\det A = -4$.

### 1. Computation of $\det(2A)$

**Property:** For an $n\times n$ matrix $A$ and any scalar $c \in \mathbb{R}$,

$$
\det(cA) = c^n \det A
$$

*Justification:* Multiplying a matrix by a scalar $c$ multiplies each of its $n$ rows by $c$. Factoring $c$ out from each of the $n$ rows introduces a factor of $c^n$.

Here $n = 3$ and $c = 2$:

$$
\det(2A) = 2^3 \det A = 8\cdot (-4) = -32
$$

### 2. Computation of $\det(A^T)$

**Property:** For any square matrix $A$, the determinant of its transpose equals the determinant of $A$:

$$
\det(A^T) = \det A
$$

*Justification:* Transposition interchanges rows and columns without changing the set of products or permutation signs in the Leibniz formula for the determinant.

Therefore:

$$
\det(A^T) = -4
$$

### 3. Computation of $\det(A^2)$

**Property:** By the multiplicative property of determinants, for square matrices of the same size, $\det(AB) = (\det A)(\det B)$. Consequently, for any positive integer $k$,

$$
\det(A^k) = (\det A)^k
$$

*Justification:* Applying the product rule with $B = A$ yields $\det(A^2) = \det(A\cdot A) = (\det A)(\det A) = (\det A)^2$.

Therefore:

$$
\det(A^2) = (-4)^2 = 16
$$

### 4. Computation of $\det(-A)$

**Property:** Setting $c = -1$ in the scalar multiplication rule $\det(cA) = c^n \det A$:

$$
\det(-A) = (-1)^n \det A
$$

*Justification:* Each of the $n = 3$ rows is multiplied by $-1$, so the overall sign changes by $(-1)^3 = -1$.

Therefore:

$$
\det(-A) = (-1)^3 \det A = -1\cdot (-4) = 4
$$
