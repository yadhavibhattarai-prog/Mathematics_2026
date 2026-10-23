### Exercise 4. Gauss–Jordan
Find $A^{-1}$ using the Gauss–Jordan method for

$$
A=
\begin{pmatrix}
1 & 2 \\
3 & 5 \\
\end{pmatrix}.
$$

Show the augmented matrix $[A\mid I]$ after successive operations and explain why obtaining $I$ on the left gives the inverse on the right.

> **Why this exercise:** introduces the Gauss–Jordan method together with its meaning, not merely as a sequence of operations.

## Solution

### 1. The Initial Augmented Matrix

To find $A^{-1}$, form the augmented matrix $[A \mid I]$ by adjoining the $2\times 2$ identity matrix to $A$:

$$
\begin{pmatrix}
1 & 2 & \mid & 1 & 0 \\
3 & 5 & \mid & 0 & 1 \\
\end{pmatrix}
$$

### 2. Successive Row Operations

**Step 1:** Eliminate the entry below the pivot in the first column by applying $R_2 \leftarrow R_2 - 3R_1$:

$$
\begin{pmatrix}
1 & 2 & \mid & 1 & 0 \\
0 & -1 & \mid & -3 & 1 \\
\end{pmatrix}
$$

**Step 2:** Normalize the second pivot to $+1$ by applying $R_2 \leftarrow -R_2$:

$$
\begin{pmatrix}
1 & 2 & \mid & 1 & 0 \\
0 & 1 & \mid & 3 & -1 \\
\end{pmatrix}
$$

**Step 3:** Eliminate the entry above the second pivot by applying $R_1 \leftarrow R_1 - 2R_2$:

$$
\begin{pmatrix}
1 & 0 & \mid & -5 & 2 \\
0 & 1 & \mid & 3 & -1 \\
\end{pmatrix}
$$

The left block is now reduced to the identity matrix $I_2$. The right block is the inverse matrix:

$$
A^{-1}=
\begin{pmatrix}
-5 & 2 \\
3 & -1 \\
\end{pmatrix}
$$

### 3. Why Obtaining $I$ on the Left Yields $A^{-1}$ on the Right

Every elementary row operation corresponds to multiplying the matrix on the left by an elementary matrix $E_i$.

A sequence of $k$ row operations that transforms $A$ into $I$ corresponds to multiplying $A$ by the product matrix $E = E_k \cdots E_2 E_1$:

$$
E A = I
$$

By definition of the matrix inverse, if $E A = I$ for square matrices, then $E = A^{-1}$.

When the same row operations are performed simultaneously on the augmented block matrix $[A \mid I]$, the operation matrix $E$ multiplies both blocks:

$$
E [A \mid I] = [E A \mid E I] = [I \mid E] = [I \mid A^{-1}]
$$

Thus, transforming the left side into $I$ automatically produces $A^{-1}$ on the right side.
