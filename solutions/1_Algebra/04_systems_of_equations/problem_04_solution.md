## Question

### Exercise 4. Infinitely Many Solutions

Solve

$$
\begin{cases}
x+y+z=2, \\
2x+2y+2z=4, \\
x-y+z=0.
\end{cases}
$$

Give the solution in parametric form, identify a free variable, and for one chosen parameter value check that the resulting point really satisfies the system.

> **Why this exercise:** shows the case of multiple solutions and teaches a simple parametric description.

## Solution

### 1. Setting Up the Augmented Matrix

Let the variables be $x$, $y$, and $z$. The system of equations is:

$$
\begin{cases}
x + y + z = 2, \\
2x + 2y + 2z = 4, \\
x - y + z = 0.
\end{cases}
$$

The augmented matrix $(A \mid \mathbf{b})$ is:

$$
(A \mid \mathbf{b}) =
\begin{pmatrix}
1 & 1 & 1 & \mid & 2 \\
2 & 2 & 2 & \mid & 4 \\
1 & -1 & 1 & \mid & 0 \\
\end{pmatrix}
$$

---

### 2. Systematic Gaussian Elimination

#### Step 2.1: Eliminate $x$ from Rows 2 and 3
Apply the row operations $R_2 \leftarrow R_2 - 2R_1$ and $R_3 \leftarrow R_3 - R_1$:

- For Row 2:

$$
(2, 2, 2 \mid 4) - 2(1, 1, 1 \mid 2) = (0, 0, 0 \mid 0)
$$

- For Row 3:

$$
(1, -1, 1 \mid 0) - (1, 1, 1 \mid 2) = (0, -2, 0 \mid -2)
$$

The matrix becomes:

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 2 \\
0 & 0 & 0 & \mid & 0 \\
0 & -2 & 0 & \mid & -2 \\
\end{pmatrix}
$$

#### Step 2.2: Swap Rows to Obtain Row Echelon Form
Swap Row 2 and Row 3 ($R_2 \leftrightarrow R_3$) to place the non-zero row above the zero row:

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 2 \\
0 & -2 & 0 & \mid & -2 \\
0 & 0 & 0 & \mid & 0 \\
\end{pmatrix}
$$

#### Step 2.3: Scale Row 2
Multiply Row 2 by $-\frac{1}{2}$ ($R_2 \leftarrow -\frac{1}{2}R_2$):

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 2 \\
0 & 1 & 0 & \mid & 1 \\
0 & 0 & 0 & \mid & 0 \\
\end{pmatrix}
$$

This is the **row echelon form** (REF) of the augmented matrix.

---

### 3. Identifying Pivots, Rank, and Free Variable

Look at the leading entries (pivots) in the echelon matrix:
- **Row 1:** Pivot is $1$ in **Column 1** (variable $x$).
- **Row 2:** Pivot is $1$ in **Column 2** (variable $y$).
- **Row 3:** All entries are zero, so there is no pivot.

Thus:
- **Pivot (basic) variables:** $x$ and $y$.
- **Free variable:** Column 3 has no pivot, so **$z$ is the free variable**.

#### Why There Are Infinitely Many Solutions
- Number of unknowns: $n = 3$ ($x, y, z$).
- Rank of coefficient matrix: $r = \mathrm{rank}(A) = 2$.
- Rank of augmented matrix: $\mathrm{rank}(A \mid \mathbf{b}) = 2$.

Since $\mathrm{rank}(A) = \mathrm{rank}(A \mid \mathbf{b})$, the system is consistent.
Because the rank $r = 2$ is strictly less than the number of unknowns $n = 3$, the system has:

$$
n - r = 3 - 2 = 1
$$

free variable. Since the free variable can be chosen as any real number, the system possesses **infinitely many solutions**.

---

### 4. Back-Substitution and Parametric Form

Translate the non-zero rows of the echelon matrix back into equations:

- From Row 2:

$$
y = 1
$$

- Assign the free parameter $t \in \mathbb{R}$ to the free variable $z$:

$$
z = t, \qquad t \in \mathbb{R}
$$

- From Row 1:

$$
x + y + z = 2
$$

Substitute $y = 1$ and $z = t$:

$$
x + 1 + t = 2 \implies x = 2 - 1 - t = 1 - t
$$

#### Parametric Form of the Solution
The general solution in coordinate form is:

$$
(x, y, z) = (1 - t, 1, t), \qquad t \in \mathbb{R}
$$

In parametric vector form:

$$
\begin{pmatrix}
x \\
y \\
z \\
\end{pmatrix}
= \begin{pmatrix}
1 - t \\
1 \\
t \\
\end{pmatrix}
= \begin{pmatrix}
1 \\
1 \\
0 \\
\end{pmatrix}
+ t \begin{pmatrix}
-1 \\
0 \\
1 \\
\end{pmatrix},
\qquad t \in \mathbb{R}
$$

Here:
- $\mathbf{x}_p = \begin{pmatrix} 1 \\ 1 \\ 0 \end{pmatrix}$ is a particular solution to the system (for $t = 0$).
- $\mathbf{v} = \begin{pmatrix} -1 \\ 0 \\ 1 \end{pmatrix}$ is the direction vector spanning the solution space of the associated homogeneous system.

---

### 5. Checking with a Chosen Parameter Value

The exercise specifically asks to choose one parameter value and verify that the resulting point satisfies all equations of the original system.

#### Choice of Parameter Value: $t = 2$
Substitute $t = 2$ into the parametric solution:

$$
x = 1 - 2 = -1
$$

$$
y = 1
$$

$$
z = 2
$$

This yields the candidate solution point:

$$
P = (-1, 1, 2)
$$

#### Step-by-Step Substitution into the Original System

Substitute $x = -1$, $y = 1$, and $z = 2$ into each of the three original equations:

1. **Check Equation 1:** $x + y + z = 2$

$$
(-1) + (1) + (2) = -1 + 1 + 2 = 2
$$

   Left-hand side equals $2$, which matches the right-hand side. Equation 1 is **satisfied**.

2. **Check Equation 2:** $2x + 2y + 2z = 4$

$$
2(-1) + 2(1) + 2(2) = -2 + 2 + 4 = 4
$$

   Left-hand side equals $4$, which matches the right-hand side. Equation 2 is **satisfied**.

3. **Check Equation 3:** $x - y + z = 0$

$$
(-1) - (1) + (2) = -1 - 1 + 2 = -2 + 2 = 0
$$

   Left-hand side equals $0$, which matches the right-hand side. Equation 3 is **satisfied**.

Since the point $P(-1, 1, 2)$ satisfies all three equations simultaneously, the correctness of the solution is verified.

---

### 6. Additional Check for $t = 0$ and Arbitrary $t$

- **For $t = 0$:** The point is $(1, 1, 0)$:
  - Equation 1: $1 + 1 + 0 = 2$ (True)
  - Equation 2: $2(1) + 2(1) + 2(0) = 4$ (True)
  - Equation 3: $1 - 1 + 0 = 0$ (True)

- **For any general $t \in \mathbb{R}$:**
  - Equation 1: $(1 - t) + 1 + t = 1 + 1 - t + t = 2$ (Identically true)
  - Equation 2: $2(1 - t) + 2(1) + 2(t) = 2 - 2t + 2 + 2t = 4$ (Identically true)
  - Equation 3: $(1 - t) - 1 + t = 1 - 1 - t + t = 0$ (Identically true)

---

### 7. Geometric Interpretation in $\mathbb{R}^3$

- The second equation $2x + 2y + 2z = 4$ is obtained by multiplying the first equation $x + y + z = 2$ by $2$. Thus, equations 1 and 2 represent the exact same plane $\Pi_1$.
- The third equation $x - y + z = 0$ represents a different plane $\Pi_2$.
- The normal vector of $\Pi_1$ is $\mathbf{n}_1 = (1, 1, 1)$ and the normal vector of $\Pi_2$ is $\mathbf{n}_2 = (1, -1, 1)$.
- Because $\mathbf{n}_1$ and $\mathbf{n}_2$ are not parallel, the two planes intersect along an infinite straight line in three dimensions.
- The parametric vector form gives precisely the line of intersection of these two planes.
