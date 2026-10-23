### Exercise 8. Determinant of a Product
Let $A,B$ be square matrices such that $\det A=3$ and $\det B=-5$. Compute $\det(AB)$, $\det(BA)$ and, if it exists, $\det(A^{-1}B)$. Explain why the first two results are equal even though usually $AB\neq BA$.

> **Why this exercise:** organizes how determinants behave with respect to products and inverses.

## Solution

Let $A$ and $B$ be $n\times n$ matrices with $\det A = 3$ and $\det B = -5$.

### 1. Computation of $\det(AB)$ and $\det(BA)$

By the multiplicative property of determinants:

$$
\det(AB) = (\det A)(\det B) = 3\cdot (-5) = -15
$$

Similarly:

$$
\det(BA) = (\det B)(\det A) = (-5)\cdot 3 = -15
$$

### 2. Computation of $\det(A^{-1}B)$

First, verify whether $A^{-1}$ exists:
A matrix has an inverse if and only if its determinant is nonzero. Since $\det A = 3 \neq 0$, the inverse $A^{-1}$ exists.

The determinant of the inverse matrix is given by

$$
\det(A^{-1}) = \frac{1}{\det A} = \frac{1}{3}
$$

Applying the product rule to $A^{-1}B$:

$$
\det(A^{-1}B) = \det(A^{-1})\cdot \det B = \frac{1}{3}\cdot (-5) = -\frac{5}{3}
$$

### 3. Explanation of Why $\det(AB) = \det(BA)$

Although matrix multiplication is non-commutative in general (that is, $AB \neq BA$ for most matrices), the determinant values $\det A$ and $\det B$ are ordinary scalar numbers (elements of $\mathbb{R}$).

Multiplication of real numbers is commutative:

$$
\det(AB) = (\det A)(\det B) = (\det B)(\det A) = \det(BA)
$$

Because the determinant operation maps matrix multiplication into scalar multiplication, the order of factors does not affect the determinant of their product.
