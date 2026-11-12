## Question

### Exercise 6. A System with a Parameter — Which Cases Actually Occur?

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

### 1. Intuitive Algebraic Analysis (Direct Substitution)

Consider the given system of two equations:

$$
\begin{cases}
x + y = 2, \\
ax + ay = 4.
\end{cases}
$$

Factor out the parameter $a$ from the left-hand side of the second equation:

$$
a(x + y) = 4
$$

From the first equation, we know that $x + y = 2$. Substituting this into the second equation gives:

$$
a(2) = 4 \implies 2a = 4
$$

This simple relation immediately reveals the entire behavior of the system:

- If $2a = 4$ (that is, $a = 2$), the equation becomes $4 = 4$, which is always true. The second equation provides no new constraint beyond $x + y = 2$.
- If $2a \neq 4$ (that is, $a \neq 2$), the equation requires $2a = 4$, which is a contradiction. No pair $(x, y)$ can satisfy both equations simultaneously.

---

### 2. Systematic Solution via Gaussian Elimination (Augmented Matrix)

To analyze the system systematically, write it in augmented matrix form $(A \mid \mathbf{b})$:

$$
(A \mid \mathbf{b}) =
\begin{pmatrix}
1 & 1 & \mid & 2 \\
a & a & \mid & 4 \\
\end{pmatrix}
$$

Eliminate the variable $x$ from the second row using the elementary row operation $R_2 \leftarrow R_2 - aR_1$:

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

The resulting row echelon form corresponds to the system:

$$
\begin{cases}
x + y = 2, \\
0 \cdot x + 0 \cdot y = 4 - 2a.
\end{cases}
$$

The second equation simplifies to:

$$
0 = 4 - 2a
$$

The solvability of the system depends entirely on whether the right-hand side $4 - 2a$ is zero or non-zero.

---

### 3. Detailed Case-by-Case Analysis

#### Case 1: $a = 2$ (Infinitely Many Solutions)

When $a = 2$, the quantity $4 - 2a$ equals $0$:

$$
4 - 2(2) = 0
$$

The augmented matrix becomes:

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
0 & 0 & \mid & 0 \\
\end{pmatrix}
$$

- The second row $0 = 0$ is a true identity for all values of $x$ and $y$.
- The rank of the coefficient matrix equals the rank of the augmented matrix:

$$
\mathrm{rank}(A) = \mathrm{rank}(A \mid \mathbf{b}) = 1
$$

- Since the rank ($1$) is less than the number of unknowns ($2$), there is $2 - 1 = 1$ free variable.
- The system reduces to the single linear equation:

$$
x + y = 2
$$

Choose $x = t$ as the free parameter, where $t$ is any real number ($t \in \mathbb{R}$). Solving for $y$:

$$
y = 2 - t
$$

The solution set consists of all points of the form:

$$
(x, y) = (t, 2 - t), \qquad t \in \mathbb{R}
$$

In vector form, this is:

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

**Conclusion for $a = 2$:** The system is consistent and has **infinitely many solutions**.

---

#### Case 2: $a \neq 2$ (No Solution)

When $a \neq 2$, the quantity $4 - 2a$ is non-zero:

$$
4 - 2a \neq 0
$$

The second row of the echelon matrix reads:

$$
0 \cdot x + 0 \cdot y = 4 - 2a
$$

Since the left-hand side is identically $0$ while the right-hand side is non-zero, this equation is impossible:

$$
0 \neq 4 - 2a
$$

- The rank of the coefficient matrix is $1$, while the rank of the augmented matrix is $2$:

$$
\mathrm{rank}(A) = 1, \qquad \mathrm{rank}(A \mid \mathbf{b}) = 2
$$

- Because $\mathrm{rank}(A) < \mathrm{rank}(A \mid \mathbf{b})$, the Rouché-Capelli Theorem confirms that the system is inconsistent.

To see this clearly in terms of equations:
- If $a \neq 0$, dividing the second equation $ax + ay = 4$ by $a$ gives:

$$
x + y = \frac{4}{a}
$$

  The system demands that $x + y = 2$ and $x + y = \frac{4}{a}$ hold simultaneously. Since $a \neq 2$, the number $\frac{4}{a}$ is strictly different from $2$, so no pair $(x, y)$ can add up to two distinct values at the same time.
- If $a = 0$, the second equation becomes $0 \cdot x + 0 \cdot y = 4$, which is impossible ($0 = 4$).

**Conclusion for $a \neq 2$:** The system has **no solution**.

---

### 4. Why Exactly One Solution Cannot Occur

A system of two linear equations in two unknowns $A\mathbf{x} = \mathbf{b}$ has a unique solution if and only if the coefficient matrix $A$ is invertible, which means its determinant must be non-zero ($\det A \neq 0$).

Compute the determinant of the coefficient matrix $A = \begin{pmatrix} 1 & 1 \\ a & a \end{pmatrix}$:

$$
\det A =
\begin{vmatrix}
1 & 1 \\
a & a \\
\end{vmatrix}
= (1)(a) - (1)(a) = a - a = 0
$$

The determinant is zero for **every** real value of $a$:

$$
\det A = 0 \qquad (a \in \mathbb{R})
$$

Because the two rows of the coefficient matrix are always proportional:

$$
(a, a) = a \cdot (1, 1)
$$

the matrix $A$ has linearly dependent rows and rank at most $1$ for all $a$. It is impossible for $A$ to have full rank $2$.

Therefore:
- **Exactly one solution can NEVER occur for any value of $a$.**

---

### 5. Geometric Interpretation (Lines in the Coordinate Plane)

Each equation in the system represents a straight line in $\mathbb{R}^2$:

- **Line 1 ($L_1$):** $x + y = 2 \implies y = -x + 2$.
  This line has slope $m_1 = -1$ and $y$-intercept $(0, 2)$.
- **Line 2 ($L_2$):** $ax + ay = 4$.
  - For $a \neq 0$, dividing by $a$ gives $y = -x + \frac{4}{a}$, which has the exact same slope $m_2 = -1$.
  - For $a = 0$, the equation $0 = 4$ represents no points in the plane (the empty set).

Since both lines share the identical slope $m = -1$, they are always parallel to each other:

1. **When $a = 2$:**
   The $y$-intercept of $L_2$ is $\frac{4}{2} = 2$, which coincides with $L_1$. The two lines are **identical (coincident)**:

$$
L_1 = L_2
$$

   Their intersection is the entire line, giving infinitely many intersection points.

2. **When $a \neq 2$:**
   The $y$-intercepts are different ($2 \neq \frac{4}{a}$). The two lines are **parallel and distinct**:

$$
L_1 \parallel L_2, \qquad L_1 \cap L_2 = \emptyset
$$

   Parallel distinct lines never intersect, so there is no point of intersection.

3. **Why a single intersection is impossible:**
   Two straight lines in the plane intersect at exactly one point if and only if they have different slopes ($m_1 \neq m_2$). Because both equations have normal vector $(1, 1)$, their slopes are locked at $-1$ regardless of $a$. Parallel lines either never meet or coincide completely; they can never cross at a single point.

---

### 6. Summary of Answers

| Possibility | Does it occur? | Parameter Values | Mathematical Explanation |
|:---:|:---:|:---:|:---:|
| **Exactly one solution** | **No** | None (no value of $a$) | The determinant $\det A = 0$ for all $a$; the lines always have equal slopes and cannot cross at a single point. |
| **Infinitely many solutions** | **Yes** | $a = 2$ | The two equations are dependent ($L_1 = L_2$); the solution set is $(x, y) = (t, 2 - t)$ for $t \in \mathbb{R}$. |
| **No solution** | **Yes** | $a \neq 2$ ($a \in \mathbb{R} \setminus \{2\}$) | The equations are contradictory ($0 \neq 4 - 2a$); geometrically, the lines are parallel and distinct ($L_1 \parallel L_2$). |
