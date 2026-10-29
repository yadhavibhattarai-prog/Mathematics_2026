# Exercise 6. From a Sequence to a Function — Limit at Infinity

Compute

$$
\lim_{x\to\infty}\frac{3x^2-x+1}{5x^2+4x-2}.
$$

Compare the method with Exercise 1. Explain what changes when moving from $n$ to a real variable $x$, and what stays the same.

> **Why this exercise:** deliberately transfers a technique from sequence limits to function limits.

## Solution

### 1. Calculation of the Limit

The expression is a rational function where both numerator and denominator have degree $2$. Factor out the highest power, $x^2$, for $x > 0$:

$$
\frac{3x^2-x+1}{5x^2+4x-2} = \frac{x^2\left(3 - \frac{1}{x} + \frac{1}{x^2}\right)}{x^2\left(5 + \frac{4}{x} - \frac{2}{x^2}\right)} = \frac{3 - \frac{1}{x} + \frac{1}{x^2}}{5 + \frac{4}{x} - \frac{2}{x^2}}
$$

For any real constant $c$ and power $k \ge 1$:

$$
\lim_{x\to\infty}\frac{c}{x^k} = 0
$$

Applying this to each term:

$$
\lim_{x\to\infty}\left(3 - \frac{1}{x} + \frac{1}{x^2}\right) = 3 - 0 + 0 = 3
$$

$$
\lim_{x\to\infty}\left(5 + \frac{4}{x} - \frac{2}{x^2}\right) = 5 + 0 - 0 = 5
$$

Since the denominator's limit is non-zero ($5 \neq 0$), apply the quotient rule:

$$
\lim_{x\to\infty}\frac{3x^2-x+1}{5x^2+4x-2} = \frac{3}{5}
$$

---

### 2. Comparison with Exercise 1

- In Exercise 1, we computed the sequence limit:

$$
\lim_{n\to\infty}\frac{4n^2-3n+1}{2n^2+5n-7} = \frac{4}{2} = 2
$$

- In both exercises, the calculation proceeds by factoring out the highest power of the variable ($n^2$ in Exercise 1, $x^2$ in Exercise 6) and observing that all lower-degree terms decay to zero.
- The resulting limit in both cases equals the ratio of the leading coefficients: $\frac{4}{2} = 2$ in Exercise 1, and $\frac{3}{5}$ in Exercise 6.

---

### 3. What Stays the Same and What Changes

#### What Stays the Same
1. **Algebraic Manipulation:**
   The technique of dividing numerator and denominator by the highest power of the argument ($x^2$ vs $n^2$) is identical.
2. **Dominant Terms Principle:**
   The asymptotic behavior for large arguments is governed exclusively by the terms with the highest exponent. Lower-degree terms become negligible as the argument grows.
3. **Limit Laws:**
   The algebraic limit theorems for sums, products, scalar multiples, and quotients with non-zero denominators apply in the exact same manner.

#### What Changes
1. **Nature of the Domain:**
   - For a sequence, the variable $n$ belongs to the discrete set of natural numbers $\mathbb{N} = \{1, 2, 3, \dots\}$. The argument takes discrete jumps of size $1$.
   - For a function, the variable $x$ belongs to the continuous set of real numbers $\mathbb{R}$ and can assume any real value on an interval $[x_0, \infty)$.
2. **Definition of the Limit (Heine vs Cauchy):**
   - For sequences, $\lim_{n\to\infty} a_n = L$ means that for every $\varepsilon > 0$, there exists an integer $N$ such that $|a_n - L| < \varepsilon$ for all integers $n > N$.
   - For functions, $\lim_{x\to\infty} f(x) = L$ requires that $f(x)$ be within $\varepsilon$ of $L$ for **all** real numbers $x > M$. By Heine's theorem, this holds if and only if for every sequence $(x_n)$ of real numbers tending to $+\infty$, the sequence $(f(x_n))$ converges to $L$.
3. **Differential Calculus Tools:**
   - Because $x \in \mathbb{R}$ is continuous, functions can be differentiated. When dealing with indeterminate forms such as $\frac{\infty}{\infty}$, continuous function limits can also be addressed with differential tools (such as l'Hôpital's rule), which have no direct discrete counterpart for sequences without extension to real variables.

