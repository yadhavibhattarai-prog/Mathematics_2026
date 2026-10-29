# Exercise 3. Ellipse

For

$$
\frac{x^2}{25}+\frac{y^2}{9}=1,
$$

find the semiaxis lengths, the intercepts with the coordinate axes, and make a sketch. Explain along which axis the ellipse is more stretched and how this is visible in the equation.

> **Why this exercise:** teaches how to read the size and orientation of an ellipse without additional conceptual machinery.

## Solution

### 1. Semiaxis Lengths

The equation is given in canonical form:

$$
\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1
$$

Comparing denominators:

$$
\begin{aligned}
a^2 &= 25 \implies a = 5 \\
b^2 &= 9 \implies b = 3
\end{aligned}
$$

The major (horizontal) semiaxis has length $a = 5$, and the minor (vertical) semiaxis has length $b = 3$.

### 2. Intercepts with the Coordinate Axes

- **Intercepts with the $x$-axis:** Set $y = 0$:

$$
\frac{x^2}{25} + 0 = 1 \implies x^2 = 25 \implies x = \pm 5
$$

  The vertices on the $x$-axis are $(-5, 0)$ and $(5, 0)$.

- **Intercepts with the $y$-axis:** Set $x = 0$:

$$
0 + \frac{y^2}{9} = 1 \implies y^2 = 9 \implies y = \pm 3
$$

  The co-vertices on the $y$-axis are $(0, -3)$ and $(0, 3)$.

### 3. Axis of Greater Stretch and Equation Interpretation

The ellipse is more stretched along the $x$-axis.

This is directly visible in the algebraic structure of the equation:
- The denominator beneath $x^2$ is $25$, whereas the denominator beneath $y^2$ is $9$.
- Since $25 > 9$, the maximum possible value of $|x|$ (attained when $y = 0$) is $\sqrt{25} = 5$, whereas the maximum possible value of $|y|$ (attained when $x = 0$) is only $\sqrt{9} = 3$.
- In any ellipse $\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1$, the variable with the larger denominator corresponds to the axis along which the curve is more extended.

