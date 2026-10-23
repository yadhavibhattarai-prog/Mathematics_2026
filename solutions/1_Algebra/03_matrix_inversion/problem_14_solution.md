### Exercise 14. A Matrix That Is Its Own Inverse
Assume that a square matrix $A$ satisfies

$$
A^2=I.
$$

Show that

$$
A^{-1}=A.
$$

Then give an example of a $2\times2$ matrix different from $I$ and $-I$ that satisfies this condition, and verify it by multiplication.

> **Why this exercise:** requires using the definition of the inverse in a short argument and constructing an example independently, without introducing a new topic.

## Solution

### 1. Proof that $A^{-1} = A$

By definition of the power of a matrix:

$$
A^2 = A \cdot A
$$

The problem assumes that

$$
A \cdot A = I
$$

Recall the definition of the inverse matrix: for any square matrix $A$, a matrix $B$ is the inverse of $A$ if and only if

$$
A B = I \qquad \text{and} \qquad B A = I
$$

Since the equation $A \cdot A = I$ shows that multiplying $A$ by $A$ yields the identity matrix from both the left and the right, and because the inverse of a square matrix is unique, it follows directly from the definition that

$$
A^{-1} = A
$$

A matrix that equals its own inverse is called an **involutory matrix**.

### 2. Constructing an Involutory $2\times 2$ Matrix

We require a matrix $A$ satisfying $A^2 = I_2$ such that $A \neq I_2$ and $A \neq -I_2$.

Geometrically, reflection across a line in $\mathbb{R}^2$ is an involution: applying the reflection twice returns every point to its original position.

Consider the reflection across the line $y = x$, which interchanges the standard coordinates $(x_1, x_2) \mapsto (x_2, x_1)$:

$$
A=
\begin{pmatrix}
0 & 1 \\
1 & 0 \\
\end{pmatrix}
$$

Clearly, $A \neq I_2$ and $A \neq -I_2$.

*(Another standard example is reflection across the horizontal axis: $A = \begin{pmatrix} 1 & 0 \\ 0 & -1 \\ \end{pmatrix}$.)*

### 3. Verification by Multiplication

Evaluate $A^2$:

$$
\begin{aligned}
A^2 &=
\begin{pmatrix}
0 & 1 \\
1 & 0 \\
\end{pmatrix}
\begin{pmatrix}
0 & 1 \\
1 & 0 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
0\cdot 0 + 1\cdot 1 & 0\cdot 1 + 1\cdot 0 \\
1\cdot 0 + 0\cdot 1 & 1\cdot 1 + 0\cdot 0 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix} \\
&= I_2
\end{aligned}
$$

Because $A^2 = I_2$, this matrix satisfies $A^{-1} = A$.

