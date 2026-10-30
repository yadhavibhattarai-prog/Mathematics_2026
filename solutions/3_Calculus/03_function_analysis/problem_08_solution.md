# Problem 8. The Second Derivative

For

$$
f(x)=x^4-4x^2
$$

find the local extrema, intervals of convexity and concavity, and inflection points. Sketch the graph and mark all the identified features on it.

> **Why this problem:** it introduces the second derivative as a tool for describing the curvature of a graph.

## Solution

### 1. Domain and Symmetry

The function is a polynomial, so its domain is all real numbers:

$$
D_f = \mathbb{R}
$$

Because $f(-x) = (-x)^4 - 4(-x)^2 = x^4 - 4x^2 = f(x)$, the function is **even**, meaning its graph is symmetric with respect to the $y$-axis.

Its zeros are:

$$
x^2(x^2 - 4) = 0 \implies x = 0, \quad x = -2, \quad x = 2
$$

---

### 2. First Derivative and Local Extrema

Compute the first derivative:

$$
f'(x) = \frac{d}{dx}(x^4 - 4x^2) = 4x^3 - 8x = 4x(x^2 - 2) = 4x(x + \sqrt{2})(x - \sqrt{2})
$$

Critical points ($f'(x) = 0$):

$$
x_1 = -\sqrt{2}, \qquad x_2 = 0, \qquad x_3 = \sqrt{2}
$$

Determine the sign of $f'(x)$ on each interval:
- On $(-\infty, -\sqrt{2})$: $f'(x) < 0 \implies f$ is strictly decreasing.
- On $(-\sqrt{2}, 0)$: $f'(x) > 0 \implies f$ is strictly increasing.
- On $(0, \sqrt{2})$: $f'(x) < 0 \implies f$ is strictly decreasing.
- On $(\sqrt{2}, \infty)$: $f'(x) > 0 \implies f$ is strictly increasing.

#### Character of the Extrema
- **At $x = -\sqrt{2}$:**
  $f'$ changes from $-$ to $+$, so $x = -\sqrt{2}$ is a **local minimum**:

$$
f(-\sqrt{2}) = (-\sqrt{2})^4 - 4(-\sqrt{2})^2 = 4 - 8 = -4
$$

  Minimum point: $(-\sqrt{2}, -4)$.

- **At $x = 0$:**
  $f'$ changes from $+$ to $-$, so $x = 0$ is a **local maximum**:

$$
f(0) = 0
$$

  Maximum point: $(0, 0)$.

- **At $x = \sqrt{2}$:**
  $f'$ changes from $-$ to $+$, so $x = \sqrt{2}$ is a **local minimum**:

$$
f(\sqrt{2}) = (\sqrt{2})^4 - 4(\sqrt{2})^2 = 4 - 8 = -4
$$

  Minimum point: $(\sqrt{2}, -4)$.

---

### 3. Second Derivative, Convexity, and Concavity

Compute the second derivative:

$$
f''(x) = \frac{d}{dx}(4x^3 - 8x) = 12x^2 - 8 = 12\left(x^2 - \frac{2}{3}\right)
$$

Set $f''(x) = 0$ to find potential inflection points:

$$
x^2 = \frac{2}{3} \implies x = \pm\sqrt{\frac{2}{3}} = \pm\frac{\sqrt{6}}{3} \approx \pm 0.8165
$$

Determine the sign of $f''(x)$:
- **On $\left(-\infty, -\sqrt{2/3}\right)$:**
  $x^2 > 2/3 \implies f''(x) > 0$.
  The function is strictly **convex** (concave up).

- **On $\left(-\sqrt{2/3}, \sqrt{2/3}\right)$:**
  $x^2 < 2/3 \implies f''(x) < 0$.
  The function is strictly **concave** (concave down).

- **On $\left(\sqrt{2/3}, \infty\right)$:**
  $x^2 > 2/3 \implies f''(x) > 0$.
  The function is strictly **convex** (concave up).

---

### 4. Inflection Points

Because $f''(x)$ changes sign across both $x = -\sqrt{2/3}$ and $x = \sqrt{2/3}$, both points are **inflection points**.

Compute the corresponding $y$-coordinate using $x^2 = 2/3$:

$$
f\left(\pm\sqrt{\frac{2}{3}}\right) = \left(\frac{2}{3}\right)^2 - 4\left(\frac{2}{3}\right) = \frac{4}{9} - \frac{8}{3} = \frac{4 - 24}{9} = -\frac{20}{9} \approx -2.222
$$

The two inflection points are

$$
I_1 = \left(-\sqrt{\frac{2}{3}}, -\frac{20}{9}\right), \qquad I_2 = \left(\sqrt{\frac{2}{3}}, -\frac{20}{9}\right)
$$

---

### 5. Summary Table

| $x$ | $(-\infty, -\sqrt{2})$ | $-\sqrt{2}$ | $(-\sqrt{2}, -\sqrt{2/3})$ | $-\sqrt{2/3}$ | $(-\sqrt{2/3}, 0)$ | $0$ | $(0, \sqrt{2/3})$ | $\sqrt{2/3}$ | $(\sqrt{2/3}, \sqrt{2})$ | $\sqrt{2}$ | $(\sqrt{2}, \infty)$ |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| $f'(x)$ | $-$ | $0$ | $+$ | $+$ | $+$ | $0$ | $-$ | $-$ | $-$ | $0$ | $+$ |
| $f''(x)$ | $+$ | $+$ | $+$ | $0$ | $-$ | $-$ | $-$ | $0$ | $+$ | $+$ | $+$ |
| $f(x)$ | $\searrow$, conv | $-4$ (min) | $\nearrow$, conv | $-20/9$ (infl) | $\nearrow$, conc | $0$ (max) | $\searrow$, conc | $-20/9$ (infl) | $\searrow$, conv | $-4$ (min) | $\nearrow$, conv |

---

### 6. Description of the Graph

The curve has the classic symmetric "W" shape:
1. It descends from $+\infty$ convexly through the zero at $x = -2$ to reach the global minimum $(-1.414, -4)$.
2. It ascends convexly until the inflection point $(-0.816, -2.222)$, where curvature flips from concave-up to concave-down.
3. It rounds out the central local peak at $(0, 0)$ with a horizontal tangent line $y = 0$.
4. By symmetry, it descends concavely to the inflection point $(0.816, -2.222)$, switches back to convex, bottoms out at $(\sqrt{2}, -4)$, passes through the zero at $x = 2$, and climbs to $+\infty$.

