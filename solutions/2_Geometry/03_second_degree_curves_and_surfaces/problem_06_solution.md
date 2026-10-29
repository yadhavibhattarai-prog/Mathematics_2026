# Exercise 6. Shifted Ellipse

Reduce

$$
4x^2+9y^2-16x+18y-11=0
$$

to canonical form. Give the center and semiaxis lengths. Check that substituting the coordinates of the center into the left-hand side gives a value consistent with the form you obtained.

> **Why this exercise:** reinforces completing the square and recognizing a shift of the coordinate system.

## Solution

### 1. Reduction to Canonical Form

Group terms by variable:

$$
(4x^2 - 16x) + (9y^2 + 18y) - 11 = 0
$$

Factor out the leading coefficients:

$$
4(x^2 - 4x) + 9(y^2 + 2y) - 11 = 0
$$

Complete the square inside each bracket:

$$
\begin{aligned}
x^2 - 4x &= (x - 2)^2 - 4 \\
y^2 + 2y &= (y + 1)^2 - 1
\end{aligned}
$$

Substitute back into the equation:

$$
4\left[(x - 2)^2 - 4\right] + 9\left[(y + 1)^2 - 1\right] - 11 = 0
$$

Expand and gather constant terms:

$$
4(x - 2)^2 - 16 + 9(y + 1)^2 - 9 - 11 = 0
$$

$$
4(x - 2)^2 + 9(y + 1)^2 = 36
$$

Divide both sides by $36$:

$$
\frac{(x - 2)^2}{9} + \frac{(y + 1)^2}{4} = 1
$$

### 2. Center and Semiaxis Lengths

Comparing with the canonical form $\frac{(x - x_0)^2}{a^2} + \frac{(y - y_0)^2}{b^2} = 1$:

- **Center:** $S = (x_0, y_0) = (2, -1)$.
- **Major semiaxis (horizontal):** $a = \sqrt{9} = 3$.
- **Minor semiaxis (vertical):** $b = \sqrt{4} = 2$.

### 3. Check with Center Coordinates

Let $f(x, y) = 4x^2 + 9y^2 - 16x + 18y - 11$ be the left-hand side of the original equation.

Substitute the center coordinates $(2, -1)$:

$$
\begin{aligned}
f(2, -1) &= 4(2)^2 + 9(-1)^2 - 16(2) + 18(-1) - 11 \\
&= 4(4) + 9(1) - 32 - 18 - 11 \\
&= 16 + 9 - 32 - 18 - 11 \\
&= 25 - 61 \\
&= -36
\end{aligned}
$$

In the completed-square form before division by 36:

$$
4(x - 2)^2 + 9(y + 1)^2 - 36 = f(x, y)
$$

At the center $(x, y) = (2, -1)$, both squared terms vanish:

$$
4(2 - 2)^2 + 9(-1 + 1)^2 - 36 = 0 + 0 - 36 = -36
$$

This matches $f(2, -1) = -36$ exactly, confirming that the reduction and center coordinates are correct.

