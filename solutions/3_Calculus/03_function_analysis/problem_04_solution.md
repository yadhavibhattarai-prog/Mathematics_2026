# Problem 4. A Function with Two Vertical Asymptotes

Analyze

$$
f(x)=\frac1{x^2-1}.
$$

Determine the domain, asymptotes, sign, and monotonicity on the intervals of the domain. Explain why each interval must be analyzed separately.

> **Why this problem:** it practices the analysis of a function on several disjoint intervals.

## Solution

### 1. Domain of the Function

The denominator must not vanish:

$$
x^2 - 1 \neq 0 \iff (x - 1)(x + 1) \neq 0 \iff x \neq \pm 1
$$

The domain is the union of three disjoint open intervals:

$$
D_f = (-\infty, -1) \cup (-1, 1) \cup (1, \infty)
$$

The function is even, since $f(-x) = \frac{1}{(-x)^2 - 1} = \frac{1}{x^2 - 1} = f(x)$, so its graph is symmetric with respect to the $y$-axis.

---

### 2. Asymptotes

#### Vertical Asymptotes
Examine the one-sided limits at the two points of discontinuity:
- **At $x = 1$:**

$$
\lim_{x\to1^+}\frac{1}{x^2 - 1} = \frac{1}{0^+} = +\infty, \qquad \lim_{x\to1^-}\frac{1}{x^2 - 1} = \frac{1}{0^-} = -\infty
$$

- **At $x = -1$:**

$$
\lim_{x\to-1^+}\frac{1}{x^2 - 1} = \frac{1}{0^-} = -\infty, \qquad \lim_{x\to-1^-}\frac{1}{x^2 - 1} = \frac{1}{0^+} = +\infty
$$

The lines $x = -1$ and $x = 1$ are **vertical asymptotes**.

#### Horizontal Asymptote
Compute the limit as $x \to \pm\infty$:

$$
\lim_{x\to\pm\infty}\frac{1}{x^2 - 1} = 0
$$

The horizontal line $y = 0$ ($x$-axis) is a **horizontal asymptote** both as $x \to +\infty$ and as $x \to -\infty$.

---

### 3. Sign of the Function

The numerator is always $1 > 0$. Therefore, the sign of $f(x)$ is determined entirely by $x^2 - 1$:
- On $(-\infty, -1)$: $x^2 > 1 \implies x^2 - 1 > 0 \implies f(x) > 0$.
- On $(-1, 1)$: $x^2 < 1 \implies x^2 - 1 < 0 \implies f(x) < 0$.
- On $(1, \infty)$: $x^2 > 1 \implies x^2 - 1 > 0 \implies f(x) > 0$.

The function has no zeros because the numerator is never zero.

---

### 4. Derivative and Monotonicity

Differentiate $f(x) = (x^2 - 1)^{-1}$ using the chain rule:

$$
f'(x) = -1(x^2 - 1)^{-2} \cdot (2x) = \frac{-2x}{(x^2 - 1)^2}
$$

The denominator $(x^2 - 1)^2$ is strictly positive for all $x \in D_f$. The sign of $f'(x)$ is determined entirely by the numerator $-2x$:

- **On $(-\infty, -1)$:**
  $x < 0 \implies -2x > 0 \implies f'(x) > 0$.
  The function is strictly increasing on $(-\infty, -1)$.

- **On $(-1, 0)$:**
  $x < 0 \implies -2x > 0 \implies f'(x) > 0$.
  The function is strictly increasing on $(-1, 0]$.

- **At $x = 0$:**
  $f'(0) = 0$. Since $f'$ switches from positive to negative, $f$ has a **local maximum** at $x = 0$:

$$
f(0) = \frac{1}{0^2 - 1} = -1
$$

  The local maximum point is $(0, -1)$.

- **On $(0, 1)$:**
  $x > 0 \implies -2x < 0 \implies f'(x) < 0$.
  The function is strictly decreasing on $[0, 1)$.

- **On $(1, \infty)$:**
  $x > 0 \implies -2x < 0 \implies f'(x) < 0$.
  The function is strictly decreasing on $(1, \infty)$.

---

### 5. Why Each Interval Must Be Analyzed Separately

1. **Topological Disconnection of the Domain:**
   The domain $D_f = (-\infty, -1) \cup (-1, 1) \cup (1, \infty)$ is composed of three mutually disjoint intervals separated by the points of discontinuity $x = \pm 1$. Calculus theorems relating the sign of the derivative to monotonicity require the domain to be a connected interval.
2. **Failure of Global Monotonicity Across Asymptotes:**
   While $f'(x) > 0$ on $(-\infty, -1)$ and $f'(x) > 0$ on $(-1, 0)$, it is incorrect to conclude that $f$ is increasing on $(-\infty, -1) \cup (-1, 0)$.
   Indeed, choose $x_1 = -2$ and $x_2 = -0.5$:
   - $f(-2) = \frac{1}{4 - 1} = \frac{1}{3} > 0$.
   - $f(-0.5) = \frac{1}{0.25 - 1} = -\frac{4}{3} < 0$.
   Even though $x_1 < x_2$, we have $f(x_1) > f(x_2)$. The values plunge across the vertical asymptote from $+\infty$ to $-\infty$, violating the definition of an increasing function across the union. Monotonicity statements are valid only on each connected interval independently.
