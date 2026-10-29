# Problem 9. A Logarithm and the Chain Rule

For

$$
f(x)=\ln(x^2+1)
$$

compute the derivative. Then determine the sign of $f'(x)$ for $x<0$, $x=0$, and $x>0$, and describe qualitatively how the function behaves around zero.

> **Why this problem:** it connects differentiation with sign analysis and the behavior of a function.

## Solution

### 1. Computation of the Derivative

First note that for all real $x \in \mathbb{R}$, $x^2 \ge 0$, which ensures that

$$
x^2 + 1 \ge 1 > 0
$$

Thus, the argument of the logarithm is strictly positive everywhere, and the domain is $D_f = \mathbb{R}$.

To differentiate $f(x) = \ln(x^2 + 1)$, apply the chain rule with:
- Outer function: $g(u) = \ln u \implies g'(u) = \frac{1}{u}$
- Inner function: $u(x) = x^2 + 1 \implies u'(x) = 2x$

According to the chain rule:

$$
f'(x) = g'(u(x)) \cdot u'(x) = \frac{1}{x^2 + 1} \cdot 2x = \frac{2x}{x^2 + 1}
$$

---

### 2. Sign of $f'(x)$ on the Three Intervals

The denominator satisfies $x^2 + 1 > 0$ for every real number $x$. Therefore, the sign of the fraction $\frac{2x}{x^2+1}$ is identical to the sign of its numerator $2x$:

1. **For $x < 0$:**

$$
2x < 0 \implies f'(x) = \frac{2x}{x^2+1} < 0
$$

   The derivative is strictly negative.

2. **For $x = 0$:**

$$
2(0) = 0 \implies f'(0) = \frac{0}{0^2+1} = 0
$$

   The derivative is zero.

3. **For $x > 0$:**

$$
2x > 0 \implies f'(x) = \frac{2x}{x^2+1} > 0
$$

   The derivative is strictly positive.

---

### 3. Qualitative Behavior of the Function Around Zero

- **To the left of zero ($x < 0$):**
  Since $f'(x) < 0$ on $(-\infty, 0)$, the function is strictly decreasing as $x$ approaches $0$ from the left.
- **At the origin ($x = 0$):**
  Since $f'(0) = 0$, the tangent line to the graph at $x = 0$ is completely horizontal. The value of the function at this point is

$$
f(0) = \ln(0^2 + 1) = \ln(1) = 0
$$

- **To the right of zero ($x > 0$):**
  Since $f'(x) > 0$ on $(0, \infty)$, the function is strictly increasing as $x$ moves to the right of $0$.
- **Symmetry and Global Minimum:**
  Because $f(-x) = \ln((-x)^2 + 1) = \ln(x^2 + 1) = f(x)$, the function is even, meaning its graph is symmetric with respect to the $y$-axis.
  Because $f'(x)$ transitions from negative to positive across $x = 0$, the point $(0, 0)$ is the unique strict global minimum of the function. The curve resembles a smooth, U-shaped valley centered at the origin.

