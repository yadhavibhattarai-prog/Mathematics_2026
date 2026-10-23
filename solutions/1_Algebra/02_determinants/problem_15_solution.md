### Exercise 15. Combining Determinant Properties
Let $A$ and $B$ be invertible $2\times2$ matrices with

$$
\det A=-2,\qquad \det B=3.
$$

Without finding the entries of the matrices, compute

$$
\det\left(B^{-1}A^TB\right).
$$

State the determinant properties you use in order and explain why the factors involving $B$ eventually cancel.

> **Why this exercise:** tests the transfer of several known properties into one short problem instead of checking a single property again with numbers.

## Solution

Let $A$ and $B$ be invertible $2\times 2$ matrices with $\det A = -2$ and $\det B = 3$.

### 1. Determinant Properties Used (in Order)

1. **Multiplicative Property (Determinant of a Product):**
For square matrices $X, Y, Z$ of the same size,

$$
\det(XYZ) = (\det X)(\det Y)(\det Z)
$$

Applying this to $X = B^{-1}$, $Y = A^T$, and $Z = B$:

$$
\det\left(B^{-1}A^TB\right) = \det\left(B^{-1}\right)\cdot \det\left(A^T\right)\cdot \det B
$$

2. **Inverse Property (Determinant of an Inverse Matrix):**
Since $B$ is invertible, $B^{-1}B = I$, and because $\det I = 1$:

$$
\det\left(B^{-1}\right) = \frac{1}{\det B}
$$

3. **Transpose Property (Determinant of a Transpose):**
Transposing a matrix does not change its determinant:

$$
\det\left(A^T\right) = \det A
$$

### 2. Computation

Substituting the properties into the factored determinant expression:

$$
\begin{aligned}
\det\left(B^{-1}A^TB\right) &= \left(\frac{1}{\det B}\right)\cdot (\det A)\cdot (\det B) \\
&= \frac{1}{3}\cdot (-2)\cdot 3 \\
&= -2
\end{aligned}
$$

### 3. Explanation of Why Factors Involving $B$ Cancel

The cancellation can be understood in two complementary ways:

1. **Commutativity of Scalar Multiplication:**
Although matrix multiplication is non-commutative (in general, $B^{-1}A^TB \neq A^T$), the determinants $\det(B^{-1})$, $\det(A^T)$, and $\det B$ are real numbers (scalars). Because multiplication in $\mathbb{R}$ is commutative and associative:

$$
\left(\frac{1}{\det B}\right)\cdot (\det A)\cdot (\det B) = (\det A)\cdot \left(\frac{1}{\det B}\cdot \det B\right) = (\det A)\cdot 1 = \det A
$$

The scalar $\det(B^{-1}) = \frac{1}{\det B}$ and the scalar $\det B$ are multiplicative inverses in $\mathbb{R}$, so their product is $1$.

2. **Invariance Under Matrix Similarity:**
The product $B^{-1}A^TB$ is a similarity transformation of $A^T$. Similar matrices represent the same linear operator under different bases and always share the same determinant. Hence:

$$
\det\left(B^{-1}A^TB\right) = \det\left(A^T\right) = \det A = -2
$$

