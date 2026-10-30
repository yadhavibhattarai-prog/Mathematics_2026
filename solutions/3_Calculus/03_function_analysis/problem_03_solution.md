# Problem 3. A Rational Function

Analyze the domain, zeros, asymptotes, and monotonicity of

$$
f(x)=\frac{x+1}{x-2}.
$$

Finally, sketch a graph consistent with all the information obtained.

> **Why this problem:** it teaches how to combine the domain, limits, and derivative in the analysis of a rational function.

## Solution

### 1. Domain of the Function

The function is a rational expression. Division by zero is undefined, so the denominator must be non-zero:

$$
x - 2 \neq 0 \implies x \neq 2
$$

The domain is

$$
D_f = \mathbb{R} \setminus \{2\} = (-\infty, 2) \cup (2, \infty)
$$

---

### 2. Zeros and Intercepts

- **Zero of the Function ($x$-intercept):**
  Set $f(x) = 0$:

$$
\frac{x + 1}{x - 2} = 0 \iff x + 1 = 0 \implies x = -1
$$

  Since $-1 \in D_f$, the unique zero is $x = -1$, giving the $x$-intercept $(-1, 0)$.

- **$y$-intercept:**
  Evaluate at $x = 0$:

$$
f(0) = \frac{0 + 1}{0 - 2} = -\frac{1}{2} = -0.5
$$

  The $y$-intercept is $(0, -0.5)$.

---

### 3. Asymptotes

#### Vertical Asymptote
Investigate the behavior as $x$ approaches the domain boundary $x_0 = 2$:
- Right-hand limit ($x \to 2^+$):

$$
\lim_{x\to2^+}\frac{x + 1}{x - 2} = \frac{3}{0^+} = +\infty
$$

- Left-hand limit ($x \to 2^-$):

$$
\lim_{x\to2^-}\frac{x + 1}{x - 2} = \frac{3}{0^-} = -\infty
$$

Therefore, the vertical line

$$
x = 2
$$

is a two-sided vertical asymptote.

#### Horizontal Asymptote
Compute the limits as $x \to \pm\infty$:

$$
\lim_{x\to\pm\infty}\frac{x + 1}{x - 2} = \lim_{x\to\pm\infty}\frac{1 + \frac{1}{x}}{1 - \frac{2}{x}} = \frac{1 + 0}{1 - 0} = 1
$$

Therefore, the horizontal line

$$
y = 1
$$

is a horizontal asymptote as $x \to +\infty$ and as $x \to -\infty$.

---

### 4. Derivative and Monotonicity

Differentiate $f(x)$ using the quotient rule:

$$
\begin{aligned}
f'(x) &= \frac{(1)(x - 2) - (x + 1)(1)}{(x - 2)^2} \\
&= \frac{x - 2 - x - 1}{(x - 2)^2} \\
&= \frac{-3}{(x - 2)^2}
\end{aligned}
$$

For all $x \in D_f$, the square in the denominator is strictly positive: $(x - 2)^2 > 0$.
Because the numerator is $-3 < 0$:

$$
f'(x) < 0 \quad (x \in D_f)
$$

The derivative is strictly negative on its entire domain. Consequently:
- $f$ is strictly decreasing on $(-\infty, 2)$,
- $f$ is strictly decreasing on $(2, \infty)$.
There are no critical points ($f'(x) \neq 0$ everywhere) and no local extrema.

---

### 5. Summary Table

| Interval / Point | $(-\infty, -1)$ | $x = -1$ | $(-1, 2)$ | $x = 2$ | $(2, \infty)$ |
|:---:|:---:|:---:|:---:|:---:|:---:|
| $f'(x)$ | $-$ | $-$ | $-$ | undefined | $-$ |
| $f(x)$ | $+$ | $0$ | $-$ | undefined | $+$ |
| Monotonicity | $\searrow$ | $\searrow$ | $\searrow$ | vertical asymptote | $\searrow$ |

---

### 6. Geometric Features for the Graph

Rewriting by polynomial division:

$$
f(x) = \frac{(x - 2) + 3}{x - 2} = 1 + \frac{3}{x - 2}
$$

The graph is a standard rectangular hyperbola $y = \frac{3}{x}$ shifted:
- $2$ units to the right ($x = 2$ is the vertical asymptote),
- $1$ unit upwards ($y = 1$ is the horizontal asymptote).

The curve has two disconnected branches:
- **Left branch ($x < 2$):** Lies below the asymptote $y = 1$, crosses $(-1, 0)$ and $(0, -0.5)$, plunging to $-\infty$ as $x \to 2^-$.
- **Right branch ($x > 2$):** Comes down from $+\infty$ along $x = 2$, remaining strictly above the line $y = 1$ and leveling off toward $y = 1$ as $x \to +\infty$.

