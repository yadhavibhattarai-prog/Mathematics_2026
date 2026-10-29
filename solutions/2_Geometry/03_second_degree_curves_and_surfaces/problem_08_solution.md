# Exercise 8. Sphere

Reduce

$$
x^2+y^2+z^2-4x+2y-6z-2=0
$$

to canonical form. Find the center and radius. Give two points on the sphere and check them in the equation.

> **Why this exercise:** transfers the technique known from circles from two dimensions to three.

## Solution

### 1. Reduction to Canonical Form

Group the terms by variables:

$$
(x^2 - 4x) + (y^2 + 2y) + (z^2 - 6z) - 2 = 0
$$

Complete the square for each variable:

$$
\begin{aligned}
x^2 - 4x &= (x - 2)^2 - 4 \\
y^2 + 2y &= (y + 1)^2 - 1 \\
z^2 - 6z &= (z - 3)^2 - 9
\end{aligned}
$$

Substitute these into the equation:

$$
(x - 2)^2 - 4 + (y + 1)^2 - 1 + (z - 3)^2 - 9 - 2 = 0
$$

Move the constant terms to the right-hand side:

$$
(x - 2)^2 + (y + 1)^2 + (z - 3)^2 = 4 + 1 + 9 + 2 = 16
$$

Writing $16$ as $4^2$, the canonical form of the sphere is

$$
(x - 2)^2 + (y + 1)^2 + (z - 3)^2 = 4^2
$$

### 2. Center and Radius

The canonical equation of a sphere with center $S = (x_0, y_0, z_0)$ and radius $R$ is

$$
(x - x_0)^2 + (y - y_0)^2 + (z - z_0)^2 = R^2
$$

Comparing with the obtained form:

- Center: $S = (2, -1, 3)$
- Radius: $R = \sqrt{16} = 4$

### 3. Choosing Two Points on the Sphere

By moving along the coordinate directions by distance $R = 4$ from the center $S = (2, -1, 3)$:

- **First point $P_1$:** Shift along the $x$-direction:
  
$$
P_1 = (2 + 4, -1, 3) = (6, -1, 3)
$$

- **Second point $P_2$:** Shift along the $z$-direction:
  
$$
P_2 = (2, -1, 3 + 4) = (2, -1, 7)
$$

### 4. Verification in Both Equations

- **Verification for $P_1 = (6, -1, 3)$:**
  - In canonical form:

$$
(6 - 2)^2 + (-1 + 1)^2 + (3 - 3)^2 = 4^2 + 0^2 + 0^2 = 16
$$

  - In general form:

$$
6^2 + (-1)^2 + 3^2 - 4(6) + 2(-1) - 6(3) - 2 = 36 + 1 + 9 - 24 - 2 - 18 - 2 = 46 - 46 = 0
$$

- **Verification for $P_2 = (2, -1, 7)$:**
  - In canonical form:

$$
(2 - 2)^2 + (-1 + 1)^2 + (7 - 3)^2 = 0^2 + 0^2 + 4^2 = 16
$$

  - In general form:

$$
2^2 + (-1)^2 + 7^2 - 4(2) + 2(-1) - 6(7) - 2 = 4 + 1 + 49 - 8 - 2 - 42 - 2 = 54 - 54 = 0
$$

Both points satisfy both forms of the equation.

