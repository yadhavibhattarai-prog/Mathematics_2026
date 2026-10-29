# Exercise 1. Dominant Terms in a Sequence

Compute

$$
\lim_{n\to\infty}\frac{4n^2-3n+1}{2n^2+5n-7}.
$$

Explain why the highest-degree terms determine the result.

> **Why this exercise:** introduces the idea of a dominant term and teaches how to simplify the behavior of expressions for large arguments.

## Solution

### 1. Calculation of the Limit

Both the numerator and the denominator are quadratic polynomials in $n$. To determine the behavior as $n \to \infty$, factor out the highest power of $n$, which is $n^2$:

$$
\frac{4n^2-3n+1}{2n^2+5n-7} = \frac{n^2\left(4 - \frac{3}{n} + \frac{1}{n^2}\right)}{n^2\left(2 + \frac{5}{n} - \frac{7}{n^2}\right)} = \frac{4 - \frac{3}{n} + \frac{1}{n^2}}{2 + \frac{5}{n} - \frac{7}{n^2}}
$$

For any real constant $c$ and any positive power $k \ge 1$:

$$
\lim_{n\to\infty}\frac{c}{n^k} = 0
$$

Applying this to each term in the fraction:

$$
\lim_{n\to\infty}\left(4 - \frac{3}{n} + \frac{1}{n^2}\right) = 4 - 0 + 0 = 4
$$

$$
\lim_{n\to\infty}\left(2 + \frac{5}{n} - \frac{7}{n^2}\right) = 2 + 0 - 0 = 2
$$

Since the limit of the denominator is non-zero ($2 \neq 0$), apply the quotient rule for limits:

$$
\lim_{n\to\infty}\frac{4n^2-3n+1}{2n^2+5n-7} = \frac{4}{2} = 2
$$

---

### 2. Why the Highest-Degree Terms Determine the Result

As $n$ grows very large, different powers of $n$ scale at vastly different rates:

- $n^2$ grows much faster than $n$, and $n$ grows much faster than a constant.
- The ratio of any lower-degree term to the leading term $n^2$ tends to zero as $n \to \infty$:

$$
\frac{-3n}{4n^2} = -\frac{3}{4n} \to 0, \qquad \frac{1}{4n^2} \to 0
$$

$$
\frac{5n}{2n^2} = \frac{5}{2n} \to 0, \qquad \frac{-7}{2n^2} \to 0
$$

Consequently, the lower-degree terms $-3n+1$ and $5n-7$ contribute a negligibly small fraction to the total values of the numerator and denominator for large $n$. The expressions can be written in terms of asymptotic equivalence:

$$
4n^2 - 3n + 1 = 4n^2\left(1 - \frac{3}{4n} + \frac{1}{4n^2}\right) \sim 4n^2 \quad (n\to\infty)
$$

$$
2n^2 + 5n - 7 = 2n^2\left(1 + \frac{5}{2n} - \frac{7}{2n^2}\right) \sim 2n^2 \quad (n\to\infty)
$$

The ratio of the two polynomials therefore behaves asymptotically like the ratio of their leading terms alone:

$$
\frac{4n^2-3n+1}{2n^2+5n-7} \sim \frac{4n^2}{2n^2} = \frac{4}{2} = 2
$$

---

### 3. Numerical Verification

| $n$ | Numerator $4n^2-3n+1$ | Denominator $2n^2+5n-7$ | Fraction Value |
|:---:|:---:|:---:|:---:|
| $10$ | $371$ | $243$ | $\approx 1.5267$ |
| $100$ | $39\,701$ | $20\,493$ | $\approx 1.9373$ |
| $1\,000$ | $3\,997\,001$ | $2\,004\,993$ | $\approx 1.9935$ |
| $10\,000$ | $399\,970\,001$ | $200\,049\,993$ | $\approx 1.9994$ |

The numerical values approach $2$ as $n$ increases, confirming the analytical limit.
