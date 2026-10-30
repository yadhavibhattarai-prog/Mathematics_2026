# Problem 12. A Function with an Absolute Value

Analyze

$$
f(x)=|x^2-4|.
$$

First sketch $x^2-4$, then explain the effect of the absolute value. Indicate the points where the derivative does not exist and justify the reason geometrically.

> **Why this problem:** it shows the limits of mechanical application of calculus and the importance of the geometry of the graph.

## Solution

### 1. Analysis of the Base Parabola $g(x) = x^2 - 4$

Consider the underlying quadratic function without the absolute value:

$$
g(x) = x^2 - 4
$$

- **Shape:** An upward-opening parabola with axis of symmetry $x = 0$.
- **Vertex:** $(0, -4)$, which is the global minimum.
- **Zeros ($x$-intercepts):** $x^2 - 4 = 0 \iff x = \pm 2$.
- **Sign Behavior:**
  - $g(x) \ge 0$ for $|x| \ge 2$, i.e. on $(-\infty, -2] \cup [2, \infty)$.
  - $g(x) < 0$ for $|x| < 2$, i.e. on $(-2, 2)$.

---

### 2. Effect of the Absolute Value

The absolute value operator $f(x) = |g(x)|$ acts piecewise according to the sign of $g(x)$:

$$
f(x) = |x^2 - 4| =
\begin{cases}
x^2 - 4, & x \le -2, \\
-(x^2 - 4) = 4 - x^2, & -2 < x < 2, \\
x^2 - 4, & x \ge 2.
\end{cases}
$$

#### Geometric Transformation
- On the outer intervals $(-\infty, -2]$ and $[2, \infty)$, $g(x) \ge 0$, so $|g(x)| = g(x)$. The graph remains completely unchanged.
- On the central interval $(-2, 2)$, $g(x) < 0$. The absolute value negates these values, geometrically reflecting the portion of the parabola that dipped below the $x$-axis across the $x$-axis into the upper half-plane.
- The original vertex $(0, -4)$ is flipped upward to $(0, 4)$, becoming a local maximum of $f(x)$.

---

### 3. Points Where the Derivative Does Not Exist

The points of non-differentiability occur precisely where the expression inside the absolute value changes sign, namely at the roots:

$$
x = -2, \qquad x = 2
$$

#### Analytical Proof via One-Sided Derivatives at $x = 2$
- **Right-hand derivative ($x \to 2^+$):**
  For $x > 2$, $f(x) = x^2 - 4$:

$$
f'_+(2) = \lim_{x\to2^+}\frac{f(x) - f(2)}{x - 2} = \lim_{x\to2^+}\frac{(x^2 - 4) - 0}{x - 2} = \lim_{x\to2^+}(x + 2) = 4
$$

- **Left-hand derivative ($x \to 2^-$):**
  For $-2 < x < 2$, $f(x) = 4 - x^2$:

$$
f'_-(2) = \lim_{x\to2^-}\frac{f(x) - f(2)}{x - 2} = \lim_{x\to2^-}\frac{(4 - x^2) - 0}{x - 2} = \lim_{x\to2^-}-(x + 2) = -4
$$

Because the one-sided derivatives are not equal:

$$
f'_-(2) = -4 \neq 4 = f'_+(2)
$$

the derivative $f'(2)$ **does not exist**.

By symmetry, at $x = -2$:

$$
f'_+(-2) = 4 \neq -4 = f'_-(-2)
$$

so the derivative $f'(-2)$ **does not exist**.

---

### 4. Geometric Justification

1. **Abrupt Direction Change:**
   At $x = 2$, approaching from the left, the curve plunges into the $x$-axis with a downward slope of $-4$. Immediately at $x = 2$, the reflection bounces the curve upward, leaving the point with a slope of $+4$.
2. **Sharp Corner (Cusp / Kink):**
   The graph forms a sharp V-shaped corner at $(2, 0)$ and at $(-2, 0)$. A tangent line cannot be defined unambiguously at a sharp corner because any straight line passing through $(2, 0)$ with a slope between $-4$ and $+4$ touches the curve without crossing it locally.
3. **Extrema at Singular Points:**
   Even though the derivative does not exist at $x = \pm 2$, these points are genuine **global minima** of $f(x)$, since $f(\pm 2) = 0 \le f(x)$ for all $x \in \mathbb{R}$.
   This highlights why critical points must include not only points where $f'(x) = 0$, but also points in the domain where $f'(x)$ fails to exist.
