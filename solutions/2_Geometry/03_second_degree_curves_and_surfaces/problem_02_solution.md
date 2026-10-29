# Exercise 2. Circle by Completing the Square

Reduce

$$
x^2+y^2-6x+4y-3=0
$$

to canonical form. Find the center and radius, then substitute two simple points from the circle into both forms of the equation.

> **Why this exercise:** practices completing the square as a transition from a general equation to the geometry of the object.

## Solution

### 1. Reduction to Canonical Form

Group the terms by variables:

$$
(x^2 - 6x) + (y^2 + 4y) - 3 = 0
$$

Complete the square for both $x$ and $y$:

$$
\begin{aligned}
x^2 - 6x &= (x - 3)^2 - 9 \\
y^2 + 4y &= (y + 2)^2 - 4
\end{aligned}
$$

Substitute these expressions into the equation:

$$
(x - 3)^2 - 9 + (y + 2)^2 - 4 - 3 = 0
$$

Move the constant terms to the right-hand side:

$$
(x - 3)^2 + (y + 2)^2 = 3 + 9 + 4 = 16
$$

Writing $16$ as $4^2$, the canonical form of the circle is

$$
(x - 3)^2 + (y + 2)^2 = 4^2
$$

### 2. Center and Radius

Comparing with the standard equation of a circle $(x - x_0)^2 + (y - y_0)^2 = R^2$:

- Center: $S = (x_0, y_0) = (3, -2)$
- Radius: $R = \sqrt{16} = 4$

### 3. Choosing Two Points on the Circle

- **First point $P_1$:** Setting $y = -2$:

$$
(x - 3)^2 + (-2 + 2)^2 = 16 \implies (x - 3)^2 = 16 \implies x = 3 + 4 = 7
$$

  This yields $P_1 = (7, -2)$.

- **Second point $P_2$:** Setting $x = 3$:

$$
(3 - 3)^2 + (y + 2)^2 = 16 \implies (y + 2)^2 = 16 \implies y = -2 + 4 = 2
$$

  This yields $P_2 = (3, 2)$.

### 4. Verification in Both Equations

- **Verification for $P_1 = (7, -2)$:**
  - In canonical form:

$$
(7 - 3)^2 + (-2 + 2)^2 = 4^2 + 0^2 = 16
$$

  - In general form:

$$
7^2 + (-2)^2 - 6(7) + 4(-2) - 3 = 49 + 4 - 42 - 8 - 3 = 53 - 53 = 0
$$

- **Verification for $P_2 = (3, 2)$:**
  - In canonical form:

$$
(3 - 3)^2 + (2 + 2)^2 = 0^2 + 4^2 = 16
$$

  - In general form:

$$
3^2 + 2^2 - 6(3) + 4(2) - 3 = 9 + 4 - 18 + 8 - 3 = 21 - 21 = 0
$$

Both points satisfy both forms of the equation.

