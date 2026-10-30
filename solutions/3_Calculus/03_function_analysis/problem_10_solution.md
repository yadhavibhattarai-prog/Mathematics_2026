# Problem 10. Complete Function Analysis

Perform a complete analysis of

$$
f(x)=\frac{x}{x^2+1}.
$$

Include the domain, symmetry, zeros, limits, monotonicity, extrema, and convexity. Finally, produce a sketch based only on this information.

> **Why this problem:** it combines all the basic elements of function analysis into one organized process.

## Solution

### 1. Domain, Symmetry, and Zeros

- **Domain:**
  Because $x^2 \ge 0$ for all real $x$, the denominator satisfies $x^2 + 1 \ge 1 > 0$. The denominator never vanishes, so

$$
D_f = \mathbb{R}
$$

- **Symmetry:**
  Substitute $-x$ for $x$:

$$
f(-x) = \frac{-x}{(-x)^2 + 1} = -\frac{x}{x^2 + 1} = -f(x)
$$

  The function is **odd**, meaning its graph is symmetric with respect to the origin $(0, 0)$.

- **Zeros and Intercepts:**
  Set $f(x) = 0$:

$$
\frac{x}{x^2 + 1} = 0 \iff x = 0
$$

  The unique intercept with both coordinate axes is the origin $(0, 0)$.

---

### 2. Limits and Asymptotes

Because $f$ is continuous on all of $\mathbb{R}$, there are no vertical asymptotes.

Compute the limits at positive and negative infinity:

$$
\lim_{x\to\infty}\frac{x}{x^2 + 1} = \lim_{x\to\infty}\frac{\frac{1}{x}}{1 + \frac{1}{x^2}} = \frac{0}{1 + 0} = 0
$$

$$
\lim_{x\to-\infty}\frac{x}{x^2 + 1} = 0
$$

Therefore, the horizontal line

$$
y = 0
$$

($x$-axis) is a two-sided **horizontal asymptote**.

---

### 3. First Derivative, Monotonicity, and Extrema

Differentiate $f(x)$ using the quotient rule:

$$
\begin{aligned}
f'(x) &= \frac{(1)(x^2 + 1) - x(2x)}{(x^2 + 1)^2} \\
&= \frac{x^2 + 1 - 2x^2}{(x^2 + 1)^2} \\
&= \frac{1 - x^2}{(x^2 + 1)^2} = \frac{(1 - x)(1 + x)}{(x^2 + 1)^2}
\end{aligned}
$$

The denominator $(x^2 + 1)^2$ is strictly positive for all $x \in \mathbb{R}$.
The critical points occur where $1 - x^2 = 0$:

$$
x_1 = -1, \qquad x_2 = 1
$$

Sign of $f'(x)$ and intervals of monotonicity:
- **On $(-\infty, -1)$:** $1 - x^2 < 0 \implies f'(x) < 0$. The function is strictly decreasing.
- **On $(-1, 1)$:** $1 - x^2 > 0 \implies f'(x) > 0$. The function is strictly increasing.
- **On $(1, \infty)$:** $1 - x^2 < 0 \implies f'(x) < 0$. The function is strictly decreasing.

#### Local and Global Extrema
- **At $x = -1$:**
  $f'$ changes sign from negative to positive. Local and global **minimum**:

$$
f(-1) = \frac{-1}{(-1)^2 + 1} = -\frac{1}{2} = -0.5
$$

  Minimum point: $\left(-1, -\frac{1}{2}\right)$.

- **At $x = 1$:**
  $f'$ changes sign from positive to negative. Local and global **maximum**:

$$
f(1) = \frac{1}{1^2 + 1} = \frac{1}{2} = 0.5
$$

  Maximum point: $\left(1, \frac{1}{2}\right)$.

Range of the function: $\left[-\frac{1}{2}, \frac{1}{2}\right]$.

---

### 4. Second Derivative, Convexity, and Inflection Points

Differentiate $f'(x) = \frac{1 - x^2}{(x^2 + 1)^2}$ using the quotient rule:

$$
\begin{aligned}
f''(x) &= \frac{(-2x)(x^2 + 1)^2 - (1 - x^2) \cdot 2(x^2 + 1)(2x)}{(x^2 + 1)^4} \\
&= \frac{-2x(x^2 + 1) - 4x(1 - x^2)}{(x^2 + 1)^3} \\
&= \frac{-2x^3 - 2x - 4x + 4x^3}{(x^2 + 1)^3} \\
&= \frac{2x^3 - 6x}{(x^2 + 1)^3} = \frac{2x(x^2 - 3)}{(x^2 + 1)^3}
\end{aligned}
$$

Find the roots of $f''(x) = 0$:

$$
2x(x^2 - 3) = 0 \implies x_1 = -\sqrt{3}, \quad x_2 = 0, \quad x_3 = \sqrt{3}
$$

Sign of $f''(x)$ and curvature:
- On $(-\infty, -\sqrt{3})$: $f''(x) < 0 \implies$ strictly **concave** (concave down).
- On $(-\sqrt{3}, 0)$: $f''(x) > 0 \implies$ strictly **convex** (concave up).
- On $(0, \sqrt{3})$: $f''(x) < 0 \implies$ strictly **concave** (concave down).
- On $(\sqrt{3}, \infty)$: $f''(x) > 0 \implies$ strictly **convex** (concave up).

Inflection points occur at $x = -\sqrt{3}, 0, \sqrt{3}$:

$$
f(\pm\sqrt{3}) = \frac{\pm\sqrt{3}}{3 + 1} = \pm\frac{\sqrt{3}}{4} \approx \pm 0.433
$$

The three inflection points are

$$
I_1 = \left(-\sqrt{3}, -\frac{\sqrt{3}}{4}\right), \qquad I_2 = (0, 0), \qquad I_3 = \left(\sqrt{3}, \frac{\sqrt{3}}{4}\right)
$$

---

### 5. Summary Table

| $x$ | $(-\infty, -\sqrt{3})$ | $-\sqrt{3}$ | $(-\sqrt{3}, -1)$ | $-1$ | $(-1, 0)$ | $0$ | $(0, 1)$ | $1$ | $(1, \sqrt{3})$ | $\sqrt{3}$ | $(\sqrt{3}, \infty)$ |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| $f'(x)$ | $-$ | $-$ | $-$ | $0$ | $+$ | $+$ | $+$ | $0$ | $-$ | $-$ | $-$ |
| $f''(x)$ | $-$ | $0$ | $+$ | $+$ | $+$ | $0$ | $-$ | $-$ | $-$ | $0$ | $+$ |
| $f(x)$ | $\searrow$, conc | $-\frac{\sqrt{3}}{4}$ | $\searrow$, conv | $-\frac{1}{2}$ (min) | $\nearrow$, conv | $0$ (infl) | $\nearrow$, conc | $\frac{1}{2}$ (max) | $\searrow$, conc | $\frac{\sqrt{3}}{4}$ | $\searrow$, conv |

---

### 6. Description of the Graph

1. As $x \to -\infty$, the curve emerges from just below the horizontal asymptote $y = 0$, sloping downwards concavely.
2. At the inflection point $\left(-\sqrt{3}, -\frac{\sqrt{3}}{4}\right)$, the curve transitions to concave up, bottoming out at the global minimum $\left(-1, -\frac{1}{2}\right)$ with a horizontal tangent line.
3. The curve ascends convexly through the origin $(0, 0)$, where the tangent line has slope $f'(0) = 1$, and inflection switches the curve to concave down.
4. It reaches the global maximum $\left(1, \frac{1}{2}\right)$ with a horizontal tangent line, then descends concavely to the third inflection point $\left(\sqrt{3}, \frac{\sqrt{3}}{4}\right)$.
5. After $\sqrt{3}$, it switches to concave up and glides along the positive $x$-axis from above, asymptotically approaching $y = 0$ as $x \to +\infty$.

