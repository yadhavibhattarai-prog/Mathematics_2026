# Exercise 5. The Classical Limit Leading to the Number $e$

Compute

$$
\lim_{n\to\infty}\left(1+\frac1n\right)^n.
$$

Calculate several values for increasing $n$ and compare the observed behavior with the value of the limit. Explain why a few values do not constitute a proof.

> **Why this exercise:** connects a central limit with intuition based on concrete terms of a sequence.

## Solution

### 1. Value of the Limit

The expression is an indeterminate form of type $1^\infty$. By definition of Euler's mathematical constant $e$:

$$
\lim_{n\to\infty}\left(1+\frac{1}{n}\right)^n = e
$$

The number $e$ is an irrational, transcendental constant with numerical value

$$
e \approx 2.718281828459...
$$

---

### 2. Table of Values for Increasing $n$

Let $a_n = \left(1 + \frac{1}{n}\right)^n$.

| $n$ | $1 + \frac{1}{n}$ | $a_n = \left(1 + \frac{1}{n}\right)^n$ | Difference $e - a_n$ |
|:---:|:---:|:---:|:---:|
| $1$ | $2.0$ | $2.000000$ | $\approx 0.718282$ |
| $2$ | $1.5$ | $2.250000$ | $\approx 0.468282$ |
| $5$ | $1.2$ | $2.488320$ | $\approx 0.229962$ |
| $10$ | $1.1$ | $2.593742$ | $\approx 0.124540$ |
| $50$ | $1.02$ | $2.691588$ | $\approx 0.026694$ |
| $100$ | $1.01$ | $2.704814$ | $\approx 0.013468$ |
| $1\,000$ | $1.001$ | $2.716924$ | $\approx 0.001358$ |
| $10\,000$ | $1.0001$ | $2.718146$ | $\approx 0.000136$ |
| $100\,000$ | $1.00001$ | $2.718268$ | $\approx 0.000014$ |

#### Comparison of Observed Behavior with the Analytical Limit
- **Monotonicity:** As $n$ increases from $1$ to $100\,000$, the terms $a_n$ strictly increase ($a_1 < a_2 < a_3 < \dots$).
- **Boundedness:** Even as $n$ grows by several orders of magnitude, the values never exceed $3$.
- **Rate of Convergence:** The difference $e - a_n$ decreases roughly as $\frac{e}{2n} \approx \frac{1.36}{n}$, confirming slow but steady convergence toward $e$.

---

### 3. Why Calculating a Few Values Does Not Constitute a Proof

1. **The Inductive Gap of Finite Testing:**
   Computing any finite list of values $a_1, a_2, \dots, a_k$ reveals information only about the specific indices tested. It cannot tell us what happens as $n \to \infty$. A sequence might exhibit regular behavior initially but diverge, oscillate, or stabilize at a completely different number for larger values of $n$.
2. **Deceptive Examples in Analysis:**
   - The sequence $s_n = \sum_{k=1}^n \frac{1}{k} - 100$ appears almost constant over hundreds of steps because $\frac{1}{n}$ becomes tiny, yet the harmonic series diverges to $+\infty$.
   - A sequence such as $x_n = \left(1 + \frac{1}{n}\right)^n + \sin\left(\frac{n\pi}{10^6}\right)$ is numerically indistinguishable from $e$ for $n \le 10^3$, yet oscillates indefinitely as $n \to \infty$.
3. **The Indeterminate Nature of $1^\infty$:**
   In the expression $\left(1 + \frac{1}{n}\right)^n$, two competing operations occur simultaneously:
   - The base $1 + \frac{1}{n}$ decreases toward $1$, which tends to pull the power toward $1$.
   - The exponent $n$ increases toward $\infty$, which tends to drive any base greater than $1$ toward $\infty$.
   Numerical values alone cannot prove that these two opposing effects achieve an exact finite balance.
4. **What Constitutes a Rigorous Proof:**
   A valid mathematical proof must establish:
   - **Strict monotonicity:** $a_n < a_{n+1}$ for all $n \in \mathbb{N}$ (proven using Bernoulli's inequality or the AM-GM inequality).
   - **Boundedness from above:** $a_n < 3$ for all $n \in \mathbb{N}$ (proven using the binomial theorem and comparison with a geometric series).
   - **Monotone Convergence Theorem:** Every sequence of real numbers that is bounded above and monotonically increasing possesses a finite real limit $L$. The number $e$ is formally defined as this unique limit.

