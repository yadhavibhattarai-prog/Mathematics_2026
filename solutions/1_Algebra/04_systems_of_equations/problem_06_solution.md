# Exercise 6. A System with a Parameter — Which Cases Actually Occur?

Analyze, depending on the parameter $a$, the system

$$
\begin{cases}
x+y=2, \\
ax+ay=4.
\end{cases}
$$

Among the three possibilities — exactly one solution, infinitely many solutions, no solution — determine which actually occur and for which values of $a$. If one type cannot occur, explain why.

> **Why this exercise:** teaches how to analyze a parameter without assuming in advance that all theoretically possible cases must occur in a specific system.

## Solution

### 1. Matrix Representation of the System

The system can be written in matrix form $A\mathbf{x} = \mathbf{b}$:

$$
\begin{pmatrix}
1 & 1 \\
a & a \\
\end{pmatrix}
\begin{pmatrix}
x \\
y \\
\end{pmatrix}
= \begin{pmatrix}
2 \\
4 \\
\end{pmatrix}
$$

The coefficient matrix $A$ and the augmented matrix $(A \mid \mathbf{b})$ are:

$$
A =
\begin{pmatrix}
1 & 1 \\
a & a \\
\end{pmatrix},
\qquad
(A \mid \mathbf{b}) =
\begin{pmatrix}
1 & 1 & \mid & 2 \\
a & a & \mid & 4 \\
\end{pmatrix}
$$

---

### 2. Determinant Analysis and Why a Unique Solution Cannot Occur

Compute the determinant of the coefficient matrix $A$:

$$
\det A =
\begin{vmatrix}
1 & 1 \\
a & a \\
\end{vmatrix}
= 1 \cdot a - 1 \cdot a = 0
$$

The determinant is identically zero:

$$
\det A = 0 \qquad (a \in \mathbb{R})
$$

#### Consequence for the Number of Solutions
By Cramer's rule and the Invertible Matrix Theorem, a square linear system $A\mathbf{x} = \mathbf{b}$ has **exactly one solution** if and only if $\det A \neq 0$.

Because $\det A = 0$ for every real number $a$, the coefficient matrix is never invertible. The rows (and columns) of $A$ are always linearly dependent: the second row is simply $a$ times the first row.

Therefore:
- **Exactly one solution CANNOT occur for any value of $a$.**
- The only cases that can possibly occur are **infinitely many solutions** or **no solution**.

---

### 3. Row Reduction (Gaussian Elimination)

Apply the elementary row operation $R_2 \leftarrow R_2 - aR_1$ to the augmented matrix:

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
a & a & \mid & 4 \\
\end{pmatrix}
\xrightarrow{R_2 \leftarrow R_2 - aR_1}
\begin{pmatrix}
1 & 1 & \mid & 2 \\
0 & 0 & \mid & 4 - 2a \\
\end{pmatrix}
$$

The second row corresponds to the equation:

$$
0 \cdot x + 0 \cdot y = 4 - 2a
$$

or simply:

$$
0 = 4 - 2a
$$

The consistency of the system depends entirely on whether the right-hand side $4 - 2a$ vanishes.

---

### 4. Case-by-Case Analysis

#### Case 1: $4 - 2a = 0 \iff a = 2$ (Infinitely Many Solutions)

When $a = 2$, the row echelon form becomes:

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
0 & 0 & \mid & 0 \\
\end{pmatrix}
$$

- The second row $0 = 0$ is an identity satisfied by all $(x, y) \in \mathbb{R}^2$.
- The rank of the coefficient matrix equals the rank of the augmented matrix:

$$
\mathrm{rank}(A) = \mathrm{rank}(A \mid \mathbf{b}) = 1
$$

- Because the rank is $r = 1$ and the number of unknowns is $n = 2$, there is $n - r = 2 - 1 = 1$ free variable.
- The system reduces to the single independent equation:

$$
x + y = 2
$$

Setting $x = t$ where $t \in \mathbb{R}$ is an arbitrary parameter:

$$
y = 2 - t
$$

The solution set in parametric form is:

$$
(x, y) = (t, 2 - t), \qquad t \in \mathbb{R}
$$

or in vector form:

$$
\begin{pmatrix}
x \\
y \\
\end{pmatrix}
= \begin{pmatrix}
0 \\
2 \\
\end{pmatrix}
+ t \begin{pmatrix}
1 \\
-1 \\
\end{pmatrix},
\qquad t \in \mathbb{R}
$$

Thus, for $a = 2$, the system is consistent and has **infinitely many solutions**.

---

#### Case 2: $4 - 2a \neq 0 \iff a \neq 2$ (No Solution)

When $a \neq 2$, the quantity $4 - 2a$ is non-zero. The second row yields:

$$
0 \cdot x + 0 \cdot y = 4 - 2a \neq 0
$$

This is a direct mathematical contradiction, since the left-hand side is $0$ while the right-hand side is non-zero ($0 \neq 4 - 2a$).

- The ranks of the coefficient matrix and augmented matrix are:

$$
\mathrm{rank}(A) = 1, \qquad \mathrm{rank}(A \mid \mathbf{b}) = 2
$$

- By the Rouché-Capelli (Kronecker-Capelli) Theorem, since $\mathrm{rank}(A) < \mathrm{rank}(A \mid \mathbf{b})$, the system is inconsistent.

We can inspect the two geometric sub-cases:
1. **Sub-case $a \neq 0$ and $a \neq 2$:**
   Dividing the second equation $ax + ay = 4$ by $a$ gives:

$$
x + y = \frac{4}{a}
$$

   The system requires $x + y$ to simultaneously equal $2$ and $\frac{4}{a}$. Since $a \neq 2$, $\frac{4}{a} \neq 2$, which is impossible for any point $(x, y)$.
2. **Sub-case $a = 0$:**
   The second equation becomes $0x + 0y = 4$, which is inherently false.

Thus, for all $a \in \mathbb{R} \setminus \{2\}$, the system has **no solution**.

---

### 5. Geometric Interpretation in the $xy$-Plane

In the Cartesian coordinate plane $\mathbb{R}^2$, each linear equation represents a straight line:

- **First equation:** $L_1: x + y = 2 \implies y = -x + 2$.
  This is a straight line with slope $m_1 = -1$ and $y$-intercept $(0, 2)$.
- **Second equation:** $L_2: ax + ay = 4$.
  - For $a \neq 0$, dividing by $a$ gives $x + y = \frac{4}{a} \implies y = -x + \frac{4}{a}$, which is a straight line with the identical slope $m_2 = -1$.
  - For $a = 0$, the equation $0 = 4$ describes the empty set in the plane.

Because both lines have normal vector $(1, 1)$ (or $(a, a) = a(1, 1)$), they are always parallel:
- When $a = 2$, the $y$-intercept $\frac{4}{2} = 2$ matches $L_1$. The two lines **coincide** ($L_1 = L_2$), so their intersection is the entire line (infinitely many points).
- When $a \neq 2$, the lines have the same slope but different $y$-intercepts ($\frac{4}{a} \neq 2$). The two lines are **parallel and distinct** ($L_1 \parallel L_2, L_1 \cap L_2 = \emptyset$), so they never intersect (no solution).
- Because two lines with identical slopes can never intersect at a single point, a **unique solution is geometrically impossible**.

---

### 6. Summary of Results

| Value of Parameter $a$ | Value of $4 - 2a$ | $\mathrm{rank}(A)$ | $\mathrm{rank}(A \mid \mathbf{b})$ | Nature of the System | Geometric Meaning | Number of Solutions |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| $a = 2$ | $0$ | $1$ | $1$ | Consistent dependent | Coincident lines | Infinitely many |
| $a \neq 2$ | $\neq 0$ | $1$ | $2$ | Inconsistent | Parallel distinct lines | None ($0$) |
| Any real $a$ | — | $\le 1$ | — | — | Lines never cross at one point | Exactly one cannot occur |

#### Final Conclusion
1. **Exactly one solution:** **Never occurs** for any $a \in \mathbb{R}$, because $\det A = 0$ for all $a$.
2. **Infinitely many solutions:** Occurs if and only if **$a = 2$**. The solutions are $(x, y) = (t, 2 - t)$ for all $t \in \mathbb{R}$.
3. **No solution:** Occurs for all **$a \neq 2$** (that is, $a \in (-\infty, 2) \cup (2, \infty)$).
