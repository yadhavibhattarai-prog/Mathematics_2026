# Exercise 4. Powers and Oscillation

Analyze

$$
\left(\frac23\right)^n,\qquad \left(\frac32\right)^n,\qquad (-1)^n,\qquad \frac{(-1)^n}{n}.
$$

For each sequence, describe the type of behavior and justify your answer.

> **Why this exercise:** organizes the basic types of sequence behavior and shows that oscillation does not always rule out convergence.

## Solution

### 1. The Sequence $a_n = \left(\frac{2}{3}\right)^n$

- **Type of behavior:** Monotonically decreasing, strictly positive, converging to $0$.
- **Justification:**
  This is a geometric sequence with common ratio $q = \frac{2}{3}$.
  For any real number $q$ satisfying $|q| < 1$:

$$
\lim_{n\to\infty} q^n = 0
$$

  Since $|2/3| = 2/3 < 1$, the terms decrease steadily:

$$
a_1 = \frac{2}{3} \approx 0.667, \quad a_2 = \frac{4}{9} \approx 0.444, \quad a_3 = \frac{8}{27} \approx 0.296, \quad \dots
$$

  Therefore:

$$
\lim_{n\to\infty}\left(\frac{2}{3}\right)^n = 0
$$

---

### 2. The Sequence $b_n = \left(\frac{3}{2}\right)^n$

- **Type of behavior:** Monotonically increasing, strictly positive, diverging to $+\infty$.
- **Justification:**
  This is a geometric sequence with common ratio $q = \frac{3}{2} = 1.5 > 1$.
  By Bernoulli's inequality, for any $h > 0$:

$$
(1 + h)^n \ge 1 + nh
$$

  Setting $h = \frac{1}{2}$:

$$
\left(\frac{3}{2}\right)^n = \left(1 + \frac{1}{2}\right)^n \ge 1 + \frac{n}{2} \to +\infty \quad (n\to\infty)
$$

  Therefore:

$$
\lim_{n\to\infty}\left(\frac{3}{2}\right)^n = +\infty
$$

---

### 3. The Sequence $c_n = (-1)^n$

- **Type of behavior:** Undamped (pure) oscillation between $-1$ and $1$; divergent.
- **Justification:**
  The values of the sequence alternate indefinitely:

$$
c_{2k-1} = -1, \qquad c_{2k} = 1 \quad (k \in \mathbb{N})
$$

  The subsequence of odd terms converges to $-1$:

$$
\lim_{k\to\infty} c_{2k-1} = -1
$$

  The subsequence of even terms converges to $+1$:

$$
\lim_{k\to\infty} c_{2k} = 1
$$

  Because a convergent sequence must have a unique limit and all its subsequences must converge to the same value, the existence of two distinct accumulation points ($-1 \neq 1$) proves that the limit $\lim_{n\to\infty}(-1)^n$ does not exist.

---

### 4. The Sequence $d_n = \frac{(-1)^n}{n}$

- **Type of behavior:** Damped oscillation around $0$, converging to $0$.
- **Justification:**
  The terms alternate in sign with decreasing amplitude:

$$
d_1 = -1, \quad d_2 = \frac{1}{2}, \quad d_3 = -\frac{1}{3}, \quad d_4 = \frac{1}{4}, \quad \dots
$$

  Bound the absolute value:

$$
\left|\frac{(-1)^n}{n}\right| = \frac{1}{n}
$$

  This yields the two-sided inequality:

$$
-\frac{1}{n} \le \frac{(-1)^n}{n} \le \frac{1}{n}
$$

  Taking limits of the bounding sequences:

$$
\lim_{n\to\infty}\left(-\frac{1}{n}\right) = 0, \qquad \lim_{n\to\infty}\frac{1}{n} = 0
$$

  By the Squeeze Theorem (Sandwich Theorem):

$$
\lim_{n\to\infty}\frac{(-1)^n}{n} = 0
$$

---

### 5. Summary and Key Insight

| Sequence | Bounded? | Monotonic? | Oscillating? | Limit |
|:---:|:---:|:---:|:---:|:---:|
| $(2/3)^n$ | Yes | Yes (decreasing) | No | $0$ |
| $(3/2)^n$ | No | Yes (increasing) | No | $+\infty$ |
| $(-1)^n$ | Yes | No | Yes (constant amplitude) | Does not exist |
| $(-1)^n/n$ | Yes | No | Yes (decaying amplitude) | $0$ |

**Key takeaway:** Oscillation alone does not prevent a sequence from converging. A sequence can oscillate and still converge, provided the amplitude of the oscillations shrinks to zero as $n \to \infty$.
