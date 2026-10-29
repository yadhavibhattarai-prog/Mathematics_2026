# Exercise 7. Classifying a Second-Degree Equation

Determine the type of object described by:

1. $4x^2+9y^2=36$,
2. $x^2-y^2=1$,
3. $x^2-4y=0$,
4. $x^2+y^2+1=0$.

In the last case, explain why there are no real points.

> **Why this exercise:** develops quick recognition of the curve type and checking whether real solutions exist.

## Solution

### 1. Classification of $4x^2+9y^2=36$

Divide both sides by $36$:

$$
\frac{x^2}{9} + \frac{y^2}{4} = 1
$$

- **Type of curve:** Ellipse.
- **Properties:** Centered at $(0, 0)$ with major horizontal semiaxis $a = 3$ and minor vertical semiaxis $b = 2$.

### 2. Classification of $x^2-y^2=1$

- **Type of curve:** Hyperbola (specifically, an equilateral or rectangular hyperbola).
- **Properties:** Centered at $(0, 0)$ with horizontal transverse axis, vertices at $(\pm 1, 0)$, semiaxes $a = b = 1$, and perpendicular asymptotes $y = \pm x$.

### 3. Classification of $x^2-4y=0$

Isolate $y$:

$$
x^2 = 4y \iff y = \frac{1}{4}x^2
$$

- **Type of curve:** Parabola.
- **Properties:** Vertical axis of symmetry $x = 0$, vertex at the origin $(0, 0)$, and opening upward along the positive $y$-axis.

### 4. Classification of $x^2+y^2+1=0$

Rewrite the equation by moving the constant to the right-hand side:

$$
x^2 + y^2 = -1
$$

- **Type of object:** The empty set (no real points / imaginary circle).

**Explanation for the absence of real points:**
For any real numbers $x, y \in \mathbb{R}$, squares of real numbers are non-negative:

$$
x^2 \ge 0 \qquad \mathrm{and} \qquad y^2 \ge 0
$$

Summing two non-negative numbers yields a non-negative sum:

$$
x^2 + y^2 \ge 0
$$

Adding $1$ to both sides gives:

$$
x^2 + y^2 + 1 \ge 1 > 0
$$

Because the expression $x^2 + y^2 + 1$ is strictly greater than or equal to $1$ for all $(x, y) \in \mathbb{R}^2$, it can never equal $0$. Consequently, no real coordinate pair $(x, y)$ satisfies the equation.

