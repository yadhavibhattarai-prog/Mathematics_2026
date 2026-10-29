# Exercise 11. An n-th Root

Compute

$$
\lim_{n\to\infty}\sqrt[n]{5^n+2^n}.
$$

Explain which term dominates and why the transformation looks different from the case of a quotient of polynomials.

> **Why this exercise:** extends the idea of dominance to exponential expressions.

## Solution

### 1. Calculation of the Limit

The expression contains two exponential terms with different bases: $5^n$ and $2^n$. Because $5 > 2$, the term $5^n$ grows much faster than $2^n$.

Factor out the dominant term $5^n$ from inside the radical:

$$
\sqrt[n]{5^n + 2^n} = \sqrt[n]{5^n\left(1 + \frac{2^n}{5^n}\right)} = \sqrt[n]{5^n} \cdot \sqrt[n]{1 + \left(\frac{2}{5}\right)^n}
$$

Since $5 > 0$ and $n \in \mathbb{N}$, the root of the first factor simplifies directly:

$$
\sqrt[n]{5^n} = 5
$$

So the expression becomes

$$
\sqrt[n]{5^n + 2^n} = 5 \cdot \left(1 + \left(\frac{2}{5}\right)^n\right)^{1/n}
$$

Now examine the behavior as $n \to \infty$:
- Since $0 < \frac{2}{5} < 1$, the geometric term decays to zero:

$$
\lim_{n\to\infty}\left(\frac{2}{5}\right)^n = 0
$$

- Therefore, the base inside the bracket tends to $1$:

$$
1 + \left(\frac{2}{5}\right)^n \to 1 + 0 = 1
$$

- Meanwhile, the exponent satisfies:

$$
\lim_{n\to\infty}\frac{1}{n} = 0
$$

By continuity of the exponential-logarithmic function (or via the Squeeze Theorem):

$$
\lim_{n\to\infty}\left(1 + \left(\frac{2}{5}\right)^n\right)^{1/n} = 1^0 = 1
$$

Therefore:

$$
\lim_{n\to\infty}\sqrt[n]{5^n+2^n} = 5 \cdot 1 = 5
$$

---

### 2. Alternative Derivation via the Squeeze Theorem

For all $n \ge 1$, since $2^n > 0$ and $2^n < 5^n$, we have the sharp bounds:

$$
5^n < 5^n + 2^n < 5^n + 5^n = 2 \cdot 5^n
$$

Taking the $n$-th root of all three sides preserves the inequalities:

$$
\sqrt[n]{5^n} < \sqrt[n]{5^n + 2^n} < \sqrt[n]{2 \cdot 5^n}
$$

$$
5 < \sqrt[n]{5^n + 2^n} < 5 \cdot \sqrt[n]{2}
$$

Compute the limits of the lower and upper bounds:

$$
\lim_{n\to\infty} 5 = 5
$$

$$
\lim_{n\to\infty}\left(5 \cdot \sqrt[n]{2}\right) = 5 \cdot 1 = 5
$$

By the Squeeze Theorem:

$$
\lim_{n\to\infty}\sqrt[n]{5^n+2^n} = 5
$$

---

### 3. Which Term Dominates and Why the Transformation Differs from Polynomial Quotients

#### Dominance of $5^n$
The term $5^n$ dominates because the ratio of the subdominant term to the dominant term tends to zero exponentially:

$$
\frac{2^n}{5^n} = \left(\frac{2}{5}\right)^n \to 0 \quad (n\to\infty)
$$

The contribution of $2^n$ relative to $5^n$ becomes negligible as $n$ grows.

#### Why the Transformation Differs from Polynomial Quotients
1. **Factoring Under a Radical of Variable Order:**
   In a quotient of polynomials $\frac{P(n)}{Q(n)}$, we divide numerator and denominator by a fixed power of $n$ (such as $n^2$), turning lower terms into fractions $\frac{c}{n^k} \to 0$.
   Here, the expression is a single sum inside an $n$-th root whose index grows with $n$. Instead of dividing two separate polynomials, we extract the factor $5^n$ outside the $n$-th root:

$$
\sqrt[n]{5^n} = (5^n)^{1/n} = 5
$$

2. **The Effect of the $n$-th Root on Bounded Factors:**
   The remaining bracket $1 + (2/5)^n$ is bounded between $1$ and $2$. Because the root index $n \to \infty$, taking the $n$-th root of any positive bounded number always tends to $1$:

$$
\lim_{n\to\infty}\sqrt[n]{C} = 1 \quad (C > 0)
$$

   Thus, the subdominant term inside the radical cannot alter the leading base $5$. In general, for any positive numbers $a_1, a_2, \dots, a_k > 0$:

$$
\lim_{n\to\infty}\sqrt[n]{a_1^n + a_2^n + \dots + a_k^n} = \max(a_1, a_2, \dots, a_k)
$$

