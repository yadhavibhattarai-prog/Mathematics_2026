# Problem 9. An Oblique Asymptote

Analyze the asymptotes of

$$
f(x)=\frac{x^2+1}{x-1}.
$$

Perform polynomial division and explain why the remainder term vanishes for large $|x|$.

> **Why this problem:** it teaches how to recognize an oblique asymptote and interpret the decomposition of a function.

## Solution

### 1. Domain and Vertical Asymptote

The function is undefined when the denominator is zero:

$$
x - 1 = 0 \implies x = 1
$$

Thus, the domain is $D_f = \mathbb{R} \setminus \{1\} = (-\infty, 1) \cup (1, \infty)$.

Investigate the one-sided limits at $x_0 = 1$:
- Right-hand limit ($x \to 1^+$):

$$
\lim_{x\to1^+}\frac{x^2 + 1}{x - 1} = \frac{1^2 + 1}{0^+} = \frac{2}{0^+} = +\infty
$$

- Left-hand limit ($x \to 1^-$):

$$
\lim_{x\to1^-}\frac{x^2 + 1}{x - 1} = \frac{1^2 + 1}{0^-} = \frac{2}{0^-} = -\infty
$$

Because both one-sided limits are infinite, the vertical line

$$
x = 1
$$

is a two-sided **vertical asymptote**.

---

### 2. Polynomial Division

Because the degree of the numerator ($2$) exceeds the degree of the denominator ($1$) by exactly $1$, the function has an oblique (slant) asymptote.

Perform long division of polynomials, dividing $x^2 + 1$ by $x - 1$:

$$
\begin{aligned}
x^2 + 1 &= x(x - 1) + x + 1 \\
        &= x(x - 1) + 1(x - 1) + 2 \\
        &= (x + 1)(x - 1) + 2
\end{aligned}
$$

Dividing through by $x - 1$:

$$
f(x) = \frac{x^2 + 1}{x - 1} = x + 1 + \frac{2}{x - 1}
$$

The polynomial division yields:
- Quotient polynomial: $Q(x) = x + 1$
- Remainder: $R = 2$
- Proper fractional decomposition: $f(x) = (x + 1) + \frac{2}{x - 1}$

---

### 3. Derivation of the Oblique Asymptote

A straight line $y = mx + b$ is an oblique asymptote of $f(x)$ as $x \to \pm\infty$ if and only if

$$
\lim_{x\to\pm\infty} [f(x) - (mx + b)] = 0
$$

Consider the linear candidate $y = x + 1$ obtained from the quotient polynomial.
Subtract this linear function from $f(x)$:

$$
f(x) - (x + 1) = \left(x + 1 + \frac{2}{x - 1}\right) - (x + 1) = \frac{2}{x - 1}
$$

Evaluate the limit as $x \to \infty$ and as $x \to -\infty$:

$$
\lim_{x\to+\infty}[f(x) - (x + 1)] = \lim_{x\to+\infty}\frac{2}{x - 1} = 0
$$

$$
\lim_{x\to-\infty}[f(x) - (x + 1)] = \lim_{x\to-\infty}\frac{2}{x - 1} = 0
$$

Because the vertical difference approaches zero, the straight line

$$
y = x + 1
$$

is an **oblique asymptote** of the curve both as $x \to +\infty$ and as $x \to -\infty$.

---

### 4. Why the Remainder Term Vanishes for Large $|x|$

The remainder term in the decomposed form is

$$
\frac{2}{x - 1}
$$

1. **Fixed Numerator vs Unbounded Denominator:**
   The numerator is a fixed constant ($2$). As $|x|$ becomes arbitrarily large, the denominator $|x - 1|$ grows without bound:

$$
\lim_{|x|\to\infty}|x - 1| = \infty
$$

   Dividing a fixed finite constant by an arbitrarily large quantity produces a fraction whose absolute value shrinks toward zero:

$$
\left|\frac{2}{x - 1}\right| \to 0 \quad (|x|\to\infty)
$$

2. **Geometric Significance of Relative Position:**
   - For $x > 1$: $\frac{2}{x - 1} > 0$, so $f(x) > x + 1$. The graph lies strictly **above** the oblique asymptote.
   - For $x < 1$: $\frac{2}{x - 1} < 0$, so $f(x) < x + 1$. The graph lies strictly **below** the oblique asymptote.
   As $|x| \to \infty$, the curve gets infinitely close to the line $y = x + 1$, confirming that for large distances from the origin, the behavior of the rational function is indistinguishable from that of the linear function $y = x + 1$.

