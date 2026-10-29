# Exercise 5. Hyperbola and Asymptotes

For

$$
\frac{x^2}{16}-\frac{y^2}{9}=1,
$$

find the intercepts with the $x$-axis, the asymptotes, and make a sketch. Explain why the asymptotes describe the behavior of the curve far from the center.

> **Why this exercise:** shows the role of asymptotes in understanding the global shape of a hyperbola.

## Solution

### 1. Intercepts with the $x$-Axis

To find the intercepts with the $x$-axis, set $y = 0$:

$$
\frac{x^2}{16} - 0 = 1 \implies x^2 = 16 \implies x = \pm 4
$$

The hyperbola intersects the $x$-axis at the vertices $(-4, 0)$ and $(4, 0)$.

*(Note: Setting $x = 0$ gives $-\frac{y^2}{9} = 1 \implies y^2 = -9$, which has no real solutions. Hence, there are no intercepts with the $y$-axis.)*

### 2. Equations of the Asymptotes

For a canonical hyperbola $\frac{x^2}{a^2} - \frac{y^2}{b^2} = 1$, the asymptotes are obtained by replacing the constant $1$ on the right-hand side with $0$:

$$
\frac{x^2}{16} - \frac{y^2}{9} = 0 \implies \frac{y^2}{9} = \frac{x^2}{16}
$$

Taking the square root gives the equations of the two asymptotes:

$$
y = \pm \frac{3}{4}x
$$

### 3. Why Asymptotes Describe the Behavior Far from the Center

Solve the hyperbola's equation for $y^2$:

$$
y^2 = 9\left(\frac{x^2}{16} - 1\right) = \frac{9}{16}x^2\left(1 - \frac{16}{x^2}\right)
$$

Taking the square root for $x \neq 0$:

$$
|y| = \frac{3}{4}|x|\sqrt{1 - \frac{16}{x^2}}
$$

As $|x| \to \infty$ (points moving far from the center along the branches of the hyperbola):

1. The term $\frac{16}{x^2}$ approaches $0$, so $\sqrt{1 - \frac{16}{x^2}} \to 1$.
2. The vertical difference between the hyperbola and its asymptote is

$$
\frac{3}{4}|x| - |y| = \frac{3}{4}|x|\left(1 - \sqrt{1 - \frac{16}{x^2}}\right) = \frac{3}{4}|x|\cdot \frac{\frac{16}{x^2}}{1 + \sqrt{1 - \frac{16}{x^2}}} = \frac{12}{|x|\left(1 + \sqrt{1 - \frac{16}{x^2}}\right)}
$$

As $|x| \to \infty$, this vertical distance approaches $0$.

Therefore, the hyperbola gets arbitrarily close to the straight lines $y = \pm \frac{3}{4}x$ without ever intersecting them, meaning the asymptotes dictate the direction and shape of the hyperbola at large scales.

