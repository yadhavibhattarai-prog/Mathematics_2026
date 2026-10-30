# Problem 1. A Cubic Polynomial

Analyze the monotonicity and extrema of

$$
f(x)=x^3-3x^2+2.
$$

Sketch the graph based on the results and mark the critical points.

> **Why this problem:** it teaches how to use the first derivative to describe the shape of a polynomial.

## Solution

### 1. Domain and Derivative

The function is a polynomial, so its domain is all real numbers:

$$
D_f = \mathbb{R}
$$

Differentiate $f(x)$ using the power and sum rules:

$$
f'(x) = \frac{d}{dx}(x^3 - 3x^2 + 2) = 3x^2 - 6x = 3x(x - 2)
$$

---

### 2. Critical Points

Find the stationary points by setting the first derivative to zero:

$$
f'(x) = 0 \iff 3x(x - 2) = 0
$$

This gives two critical points:

$$
x_1 = 0, \qquad x_2 = 2
$$

---

### 3. Sign of the Derivative and Monotonicity

The derivative $f'(x) = 3x^2 - 6x$ is an upward-opening parabola with roots at $x = 0$ and $x = 2$. Its sign is determined on the resulting three intervals:

- **Interval $(-\infty, 0)$:**
  For $x < 0$, both $x < 0$ and $x - 2 < 0$, so their product is positive:

$$
f'(x) > 0
$$

  The function $f$ is strictly increasing on $(-\infty, 0]$.

- **Interval $(0, 2)$:**
  For $0 < x < 2$, we have $x > 0$ and $x - 2 < 0$, so their product is negative:

$$
f'(x) < 0
$$

  The function $f$ is strictly decreasing on $[0, 2]$.

- **Interval $(2, \infty)$:**
  For $x > 2$, both $x > 0$ and $x - 2 > 0$, so their product is positive:

$$
f'(x) > 0
$$

  The function $f$ is strictly increasing on $[2, \infty)$.

---

### 4. Determination of Local Extrema

- **At $x = 0$:**
  The derivative changes sign from positive to negative as $x$ increases through $0$.
  Therefore, $f$ has a **local maximum** at $x = 0$.
  The maximum value is

$$
f(0) = 0^3 - 3(0)^2 + 2 = 2
$$

  The local maximum point is $(0, 2)$.

- **At $x = 2$:**
  The derivative changes sign from negative to positive as $x$ increases through $2$.
  Therefore, $f$ has a **local minimum** at $x = 2$.
  The minimum value is

$$
f(2) = 2^3 - 3(2)^2 + 2 = 8 - 12 + 2 = -2
$$

  The local minimum point is $(2, -2)$.

---

### 5. Summary Table

| Interval / Point | $(-\infty, 0)$ | $x = 0$ | $(0, 2)$ | $x = 2$ | $(2, \infty)$ |
|:---:|:---:|:---:|:---:|:---:|:---:|
| $f'(x)$ | $+$ | $0$ | $-$ | $0$ | $+$ |
| $f(x)$ | $\nearrow$ | $2$ (local max) | $\searrow$ | $-2$ (local min) | $\nearrow$ |

---

### 6. Additional Geometric Features for the Sketch

- **Inflection Point:**
  The second derivative is

$$
f''(x) = 6x - 6 = 6(x - 1)
$$

  Setting $f''(x) = 0$ gives $x = 1$. The inflection point is $(1, f(1)) = (1, 0)$, which is also a zero of the function.
- **Zeros of the Function:**
  Factoring $f(x) = (x - 1)(x^2 - 2x - 2) = 0$ yields three real roots:
  
$$
x = 1, \qquad x = 1 - \sqrt{3} \approx -0.73, \qquad x = 1 + \sqrt{3} \approx 2.73
$$

- **Graph Description:**
  The graph enters from the bottom-left ($f(x) \to -\infty$ as $x \to -\infty$), crosses the $x$-axis at $\approx -0.73$, reaches a local peak at $(0, 2)$, descends through the inflection point $(1, 0)$ to a local trough at $(2, -2)$, crosses the $x$-axis again at $\approx 2.73$, and rises towards $+\infty$ as $x \to +\infty$.

