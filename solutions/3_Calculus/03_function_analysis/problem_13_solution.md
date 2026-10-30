# Problem 13. A Logarithm and an Asymptote

Perform a complete analysis of

$$
f(x)=\frac{\ln x}{x},\qquad x>0.
$$

Find the maximum and the behavior at the ends of the domain. Explain which information is necessary for a correct sketch.

> **Why this problem:** it combines the domain, limits, and derivative in a less obvious example.

## Solution

### 1. Domain, Zeros, and Sign

- **Domain:**
  The problem specifies $x > 0$. The natural logarithm requires $x > 0$ and the denominator requires $x \neq 0$, so

$$
D_f = (0, \infty)
$$

- **Zero of the Function:**
  Set $f(x) = 0$:

$$
\frac{\ln x}{x} = 0 \iff \ln x = 0 \iff x = 1
$$

  The unique $x$-intercept is $(1, 0)$. There is no $y$-intercept because $x = 0 \notin D_f$.

- **Sign of the Function:**
  Because the denominator $x > 0$ for all $x \in D_f$, the sign of $f(x)$ is identical to the sign of $\ln x$:
  - For $0 < x < 1$: $\ln x < 0 \implies f(x) < 0$.
  - At $x = 1$: $f(1) = 0$.
  - For $x > 1$: $\ln x > 0 \implies f(x) > 0$.

---

### 2. Behavior at the Ends of the Domain and Asymptotes

#### Left Boundary ($x \to 0^+$)
As $x$ approaches $0$ from the right:

$$
\lim_{x\to0^+}\frac{\ln x}{x} = \frac{-\infty}{0^+} = -\infty
$$

Therefore, the vertical line

$$
x = 0
$$

($y$-axis) is a **vertical asymptote**.

#### Right Boundary ($x \to \infty$)
As $x \to \infty$, both $\ln x \to \infty$ and $x \to \infty$, giving an indeterminate form $\frac{\infty}{\infty}$. Applying l'Hôpital's rule:

$$
\lim_{x\to\infty}\frac{\ln x}{x} = \lim_{x\to\infty}\frac{\frac{1}{x}}{1} = \lim_{x\to\infty}\frac{1}{x} = 0
$$

Therefore, the horizontal line

$$
y = 0
$$

($x$-axis) is a **horizontal asymptote** as $x \to +\infty$.

---

### 3. First Derivative, Monotonicity, and Global Maximum

Differentiate $f(x) = \frac{\ln x}{x}$ using the quotient rule:

$$
f'(x) = \frac{\frac{1}{x} \cdot x - (\ln x)(1)}{x^2} = \frac{1 - \ln x}{x^2}
$$

Find the critical points by setting $f'(x) = 0$:

$$
1 - \ln x = 0 \iff \ln x = 1 \iff x = e \approx 2.7183
$$

The denominator $x^2 > 0$ for all $x > 0$. The sign of $f'(x)$ is determined entirely by $1 - \ln x$:
- **On $(0, e)$:**
  For $0 < x < e$, $\ln x < 1 \implies 1 - \ln x > 0 \implies f'(x) > 0$.
  The function $f$ is strictly increasing on $(0, e]$.

- **On $(e, \infty)$:**
  For $x > e$, $\ln x > 1 \implies 1 - \ln x < 0 \implies f'(x) < 0$.
  The function $f$ is strictly decreasing on $[e, \infty)$.

#### Global Maximum
Because $f$ strictly increases on $(0, e]$ and strictly decreases on $[e, \infty)$, the point $x = e$ is the **strict global maximum** on $(0, \infty)$.

Compute the maximum value:

$$
f(e) = \frac{\ln e}{e} = \frac{1}{e} \approx 0.3679
$$

The coordinates of the peak are $\left(e, \frac{1}{e}\right)$.

---

### 4. Second Derivative and Inflection Point

Differentiate $f'(x) = \frac{1 - \ln x}{x^2}$ using the quotient rule:

$$
\begin{aligned}
f''(x) &= \frac{\left(-\frac{1}{x}\right)x^2 - (1 - \ln x)(2x)}{x^4} \\
&= \frac{-x - 2x + 2x\ln x}{x^4} \\
&= \frac{-3x + 2x\ln x}{x^4} = \frac{2\ln x - 3}{x^3}
\end{aligned}
$$

Set $f''(x) = 0$:

$$
2\ln x - 3 = 0 \iff \ln x = \frac{3}{2} \iff x = e^{3/2} = e\sqrt{e} \approx 4.4817
$$

- For $0 < x < e^{3/2}$: $f''(x) < 0 \implies$ strictly **concave** (concave down).
- For $x > e^{3/2}$: $f''(x) > 0 \implies$ strictly **convex** (concave up).

The point where concavity changes is an **inflection point**:

$$
f\left(e^{3/2}\right) = \frac{3/2}{e^{3/2}} = \frac{3}{2e\sqrt{e}} \approx 0.3347
$$

Inflection point coordinates: $\left(e^{3/2}, \frac{3}{2e^{3/2}}\right)$.

---

### 5. Summary Table

| $x$ | $(0, 1)$ | $1$ | $(1, e)$ | $e$ | $(e, e^{3/2})$ | $e^{3/2}$ | $(e^{3/2}, \infty)$ |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| $f'(x)$ | $+$ | $+$ | $+$ | $0$ | $-$ | $-$ | $-$ |
| $f''(x)$ | $-$ | $-$ | $-$ | $-$ | $-$ | $0$ | $+$ |
| $f(x)$ | $-$ | $0$ | $+$ | $\frac{1}{e}$ (max) | $+$ | $\frac{3}{2e^{3/2}}$ (infl) | $+$ |
| Shape | $\nearrow$, conc | zero | $\nearrow$, conc | peak | $\searrow$, conc | infl point | $\searrow$, conv |

---

### 6. Information Necessary for a Correct Sketch

To draw an accurate sketch without guessing, five key features are essential:
1. **Vertical Asymptote at $x = 0$:** The graph plunges down into $-\infty$ hugging the $y$-axis from the right.
2. **Zero Crossing at $(1, 0)$:** The curve emerges from the negative quadrant and crosses the $x$-axis at $x = 1$.
3. **The Global Peak at $\left(e, \frac{1}{e}\right)$:** The curve reaches its highest elevation of $\approx 0.368$ at $x \approx 2.718$, with a horizontal tangent line $y = \frac{1}{e}$.
4. **Inflection Point at $\left(e^{3/2}, \frac{3}{2e^{3/2}}\right)$:** At $x \approx 4.48$, the curve ceases bending downwards and becomes convex.
5. **Horizontal Asymptote $y = 0$:** For $x > e^{3/2}$, the curve flattens out, staying strictly positive while asymptotically descending toward the $x$-axis as $x \to \infty$.

