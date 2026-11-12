## Question

### Exercise 5. Row Echelon Form and Number of Solutions

For the augmented matrix

$$
\begin{pmatrix}
1 & 2 & -1 & \mid & 3 \\
0 & 1 & 2 & \mid & 1 \\
0 & 0 & 0 & \mid & 0 \\
\end{pmatrix}
$$

determine the number of solutions and write them in parametric form. Explain how you know how many variables may be chosen freely.

> **Why this exercise:** teaches how to read information about solutions directly from row echelon form.

## Solution

### 1. Understanding the Augmented Matrix

Let the three unknowns associated with the columns of the matrix be $x$, $y$, and $z$.
The given augmented matrix is already in **row echelon form** (REF):

$$
\begin{pmatrix}
1 & 2 & -1 & \mid & 3 \\
0 & 1 & 2 & \mid & 1 \\
0 & 0 & 0 & \mid & 0 \\
\end{pmatrix}
$$

Translating each row into an algebraic equation:

- **Row 1:** $1x + 2y - 1z = 3 \implies x + 2y - z = 3$
- **Row 2:** $0x + 1y + 2z = 1 \implies y + 2z = 1$
- **Row 3:** $0x + 0y + 0z = 0 \implies 0 = 0$

#### Consistency Check
Row 3 corresponds to the statement $0 = 0$, which is an identity satisfied by all triples $(x, y, z)$.
Because there is no contradictory row of the form $(0\ 0\ 0 \mid b)$ with $b \neq 0$, the system is **consistent** (solutions exist).

---

### 2. Identifying Pivots, Pivot Columns, and Free Variables

A **pivot** (leading entry) is the first non-zero number in a row of an echelon matrix:

- In Row 1, the pivot is $1$, located in **Column 1** (corresponding to $x$).
- In Row 2, the pivot is $1$, located in **Column 2** (corresponding to $y$).
- In Row 3, all entries are zero, so there is no pivot.

Thus:
- **Pivot columns (basic variables):** Column 1 ($x$) and Column 2 ($y$).
- **Non-pivot column (free variable):** Column 3 ($z$).

---

### 3. How to Know How Many Variables May Be Chosen Freely

The number of free variables in any consistent linear system is determined by the difference between the total number of unknowns and the rank of the coefficient matrix:

$$
n - r
$$

where:
- $n = 3$ is the total number of unknowns ($x, y, z$),
- $r = \mathrm{rank}(A) = 2$ is the number of pivots (linearly independent equations) in the coefficient matrix $A$.

Calculating:

$$
n - r = 3 - 2 = 1
$$

#### Explanation
Each pivot variable is uniquely determined once the variables in subsequent columns are specified. Because there are $3$ variables but only $2$ independent constraints, exactly **one variable can be chosen freely**.

Because Column 3 does not contain a pivot, the variable $z$ is not constrained by any leading position and can be assigned any real number $t \in \mathbb{R}$.

---

### 4. Number of Solutions

Since the system is consistent and possesses $1$ free variable that can take any value in the infinite set of real numbers $\mathbb{R}$:

- For each distinct real number assigned to the free variable, back-substitution yields a unique pair of values for $x$ and $y$.
- Because there are infinitely many real numbers, the system has **infinitely many solutions**.

---

### 5. Step-by-Step Back-Substitution (Parametric Form)

#### Step 5.1: Assign a parameter to the free variable
Let

$$
z = t, \qquad t \in \mathbb{R}
$$

#### Step 5.2: Express $y$ in terms of $t$
Substitute $z = t$ into Row 2:

$$
y + 2t = 1 \implies y = 1 - 2t
$$

#### Step 5.3: Express $x$ in terms of $t$
Substitute $y = 1 - 2t$ and $z = t$ into Row 1:

$$
x + 2(1 - 2t) - t = 3
$$

Expand and combine like terms:

$$
x + 2 - 4t - t = 3
$$

$$
x + 2 - 5t = 3
$$

Isolate $x$:

$$
x = 3 - 2 + 5t = 1 + 5t
$$

---

### 6. Writing the Solution Set

#### Form 1: Coordinate Triple Form
The solution set is:

$$
(x, y, z) = (1 + 5t, 1 - 2t, t), \qquad t \in \mathbb{R}
$$

#### Form 2: Parametric Vector Form
Decomposing into a particular solution vector and a homogeneous direction vector:

$$
\begin{pmatrix}
x \\
y \\
z \\
\end{pmatrix}
= \begin{pmatrix}
1 + 5t \\
1 - 2t \\
t \\
\end{pmatrix}
= \begin{pmatrix}
1 \\
1 \\
0 \\
\end{pmatrix}
+ t \begin{pmatrix}
5 \\
-2 \\
1 \\
\end{pmatrix},
\qquad t \in \mathbb{R}
$$

- $\mathbf{x}_p = \begin{pmatrix} 1 \\ 1 \\ 0 \end{pmatrix}$ is a particular solution to the non-homogeneous system (obtained by setting $t = 0$).
- $\mathbf{v} = \begin{pmatrix} 5 \\ -2 \\ 1 \end{pmatrix}$ is the direction vector spanning the 1-dimensional null space (kernel) of the coefficient matrix.

---

### 7. Alternative Method: Reduced Row Echelon Form (RREF)

We can also read the solution even more directly by performing Jordan elimination above the second pivot ($R_1 \leftarrow R_1 - 2R_2$):

$$
\begin{pmatrix}
1 & 2 & -1 & \mid & 3 \\
0 & 1 & 2 & \mid & 1 \\
0 & 0 & 0 & \mid & 0 \\
\end{pmatrix}
\xrightarrow{R_1 \leftarrow R_1 - 2R_2}
\begin{pmatrix}
1 & 0 & -5 & \mid & 1 \\
0 & 1 & 2 & \mid & 1 \\
0 & 0 & 0 & \mid & 0 \\
\end{pmatrix}
$$

The rows of the RREF decoupled matrix give:
- $x - 5z = 1 \implies x = 1 + 5z$
- $y + 2z = 1 \implies y = 1 - 2z$

Setting $z = t$ immediately yields $x = 1 + 5t$ and $y = 1 - 2t$ without any intermediate algebraic rearrangement.

---

### 8. Geometric Interpretation in $\mathbb{R}^3$

In three-dimensional space:
- The first equation $x + 2y - z = 3$ represents a plane $\Pi_1$ with normal vector $\mathbf{n}_1 = (1, 2, -1)$.
- The second equation $y + 2z = 1$ represents a plane $\Pi_2$ with normal vector $\mathbf{n}_2 = (0, 1, 2)$.

Because the normal vectors are not parallel ($\mathbf{n}_1 \times \mathbf{n}_2 = (5, -2, 1) \neq \mathbf{0}$), the two planes are not parallel and intersect along a **straight line** in $\mathbb{R}^3$.

The solution set is precisely this line of intersection, passing through the point $(1, 1, 0)$ with direction vector $(5, -2, 1)$.

---

### 9. Verification of the Solution

Test the parametric solution in both non-trivial equations for two specific values of $t$:

1. **For $t = 0$ (point $(1, 1, 0)$):**
   - Row 1: $1 + 2(1) - (0) = 1 + 2 - 0 = 3$ (Satisfied)
   - Row 2: $1 + 2(0) = 1 + 0 = 1$ (Satisfied)

2. **For $t = 1$ (point $(6, -1, 1)$):**
   - Row 1: $6 + 2(-1) - (1) = 6 - 2 - 1 = 3$ (Satisfied)
   - Row 2: $-1 + 2(1) = -1 + 2 = 1$ (Satisfied)

3. **General check for any $t \in \mathbb{R}$:**
   - Row 1: $(1 + 5t) + 2(1 - 2t) - (t) = 1 + 5t + 2 - 4t - t = 3 + (5 - 4 - 1)t = 3$
   - Row 2: $(1 - 2t) + 2(t) = 1 - 2t + 2t = 1$

Both equations hold identically for every real number $t$.
