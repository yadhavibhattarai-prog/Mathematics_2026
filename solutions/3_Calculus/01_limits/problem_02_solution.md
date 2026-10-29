# Exercise 2. Different Growth Rates

Compute

$$
\lim_{n\to\infty}\frac{3n+1}{n^2+4},\qquad \lim_{n\to\infty}\frac{2n^3-n}{5n^2+1}.
$$

Compare the two cases and formulate a general observation about the degrees of the polynomials in the numerator and denominator.

> **Why this exercise:** teaches how to compare growth rates and recognize qualitatively different cases.

## Solution

### 1. First Limit: $\lim_{n\to\infty}\frac{3n+1}{n^2+4}$

The numerator has degree $1$ and the denominator has degree $2$. Divide numerator and denominator by the highest power in the denominator, $n^2$:

$$
\frac{3n+1}{n^2+4} = \frac{\frac{3n}{n^2} + \frac{1}{n^2}}{\frac{n^2}{n^2} + \frac{4}{n^2}} = \frac{\frac{3}{n} + \frac{1}{n^2}}{1 + \frac{4}{n^2}}
$$

Taking the limits of the numerator and denominator as $n \to \infty$:

$$
\lim_{n\to\infty}\left(\frac{3}{n} + \frac{1}{n^2}\right) = 0 + 0 = 0
$$

$$
\lim_{n\to\infty}\left(1 + \frac{4}{n^2}\right) = 1 + 0 = 1
$$

Since the denominator approaches $1 \neq 0$:

$$
\lim_{n\to\infty}\frac{3n+1}{n^2+4} = \frac{0}{1} = 0
$$

---

### 2. Second Limit: $\lim_{n\to\infty}\frac{2n^3-n}{5n^2+1}$

The numerator has degree $3$ and the denominator has degree $2$. Factor out $n^2$ from both:

$$
\frac{2n^3-n}{5n^2+1} = \frac{n^2\left(2n - \frac{1}{n}\right)}{n^2\left(5 + \frac{1}{n^2}\right)} = \frac{2n - \frac{1}{n}}{5 + \frac{1}{n^2}} = n \cdot \frac{2 - \frac{1}{n^2}}{5 + \frac{1}{n^2}}
$$

As $n \to \infty$:

$$
\lim_{n\to\infty}\left(2 - \frac{1}{n^2}\right) = 2, \qquad \lim_{n\to\infty}\left(5 + \frac{1}{n^2}\right) = 5
$$

Therefore:

$$
\frac{2 - \frac{1}{n^2}}{5 + \frac{1}{n^2}} \to \frac{2}{5} > 0
$$

Since $n \to \infty$ and $\frac{2}{5} > 0$:

$$
\lim_{n\to\infty}\frac{2n^3-n}{5n^2+1} = \lim_{n\to\infty}\left(n \cdot \frac{2}{5}\right) = +\infty
$$

The sequence diverges to $+\infty$.

---

### 3. Comparison of the Two Cases

- In the first sequence, the denominator grows quadratically ($n^2$), whereas the numerator grows only linearly ($n$). The denominator outpaces the numerator, forcing the quotient to $0$.
- In the second sequence, the numerator grows cubically ($n^3$), whereas the denominator grows only quadratically ($n^2$). The numerator outpaces the denominator, driving the quotient to $+\infty$.

---

### 4. General Observation on Polynomial Degrees

Let $P(n) = a_p n^p + a_{p-1}n^{p-1} + \dots + a_0$ with $a_p \neq 0$, and let $Q(n) = b_q n^q + b_{q-1}n^{q-1} + \dots + b_0$ with $b_q \neq 0$.

The limit of their ratio as $n \to \infty$ depends entirely on the degrees $p = \deg P$ and $q = \deg Q$:

$$
\lim_{n\to\infty}\frac{P(n)}{Q(n)} =
\begin{cases}
0, & p < q, \\
\dfrac{a_p}{b_q}, & p = q, \\
\pm\infty, & p > q,
\end{cases}
$$

where in the case $p > q$, the sign of infinity is determined by the sign of the ratio $a_p / b_q$.
