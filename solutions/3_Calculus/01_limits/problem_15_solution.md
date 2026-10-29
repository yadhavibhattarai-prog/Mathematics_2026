# Exercise 15. Observation Versus Proof

Choose one sequence and one function from this set. For the sequence, compute several values for increasingly large $n$. For the function, prepare a table of values with arguments approaching the limit point from the left and right. Sketch the behavior of both objects.

Compare the observation with the analytical result and explain why a finite number of calculations or a sketch does not constitute a proof that the limit exists.

> **Why this exercise:** teaches how to distinguish intuition and observation from mathematical argument.

## Solution

### 1. Selected Sequence: $a_n = \sqrt{n^2+5n} - n$ (from Exercise 3)

The analytical result from Exercise 3 established that

$$
\lim_{n\to\infty}\left(\sqrt{n^2+5n}-n\right) = \frac{5}{2} = 2.5
$$

#### Table of Values for Increasingly Large $n$

| $n$ | $\sqrt{n^2+5n}$ | $a_n = \sqrt{n^2+5n} - n$ | Difference $2.5 - a_n$ |
|:---:|:---:|:---:|:---:|
| $1$ | $\sqrt{6} \approx 2.449490$ | $1.449490$ | $1.050510$ |
| $2$ | $\sqrt{14} \approx 3.741657$ | $1.741657$ | $0.758343$ |
| $5$ | $\sqrt{50} \approx 7.071068$ | $2.071068$ | $0.428932$ |
| $10$ | $\sqrt{150} \approx 12.247449$ | $2.247449$ | $0.252551$ |
| $50$ | $\sqrt{2750} \approx 52.440442$ | $2.440442$ | $0.059558$ |
| $100$ | $\sqrt{10\,500} \approx 102.469508$ | $2.469508$ | $0.030492$ |
| $1\,000$ | $\sqrt{1\,005\,000} \approx 1\,002.496883$ | $2.496883$ | $0.003117$ |
| $10\,000$ | $\sqrt{100\,050\,000} \approx 10\,002.499688$ | $2.499688$ | $0.000312$ |

#### Qualitative Behavior of the Sequence
The discrete points $(n, a_n)$ form a strictly increasing sequence starting at $a_1 \approx 1.45$. As $n$ grows, the sequence rises steadily with flattening step sizes, asymptotically leveling off below the horizontal threshold $y = 2.5$.

---

### 2. Selected Function: $f(x) = \frac{\sin 5x}{x}$ as $x \to 0$ (from Exercise 13)

The analytical result from Exercise 13 established that

$$
\lim_{x\to0}\frac{\sin 5x}{x} = 5
$$

#### Table of Values Approaching $x_0 = 0$ from Left and Right

Because the sine function is odd, $f(x)$ is an even function:

$$
f(-x) = \frac{\sin(5(-x))}{-x} = \frac{-\sin(5x)}{-x} = \frac{\sin 5x}{x} = f(x)
$$

The values approaching from the left ($x \to 0^-$) and from the right ($x \to 0^+$) are identical for opposite arguments:

| Step | Negative Argument $x < 0$ | $f(x)$ | Positive Argument $x > 0$ | $f(x)$ |
|:---:|:---:|:---:|:---:|:---:|
| $1$ | $-0.1$ | $4.794255$ | $+0.1$ | $4.794255$ |
| $2$ | $-0.01$ | $4.997917$ | $+0.01$ | $4.997917$ |
| $3$ | $-0.001$ | $4.999979$ | $+0.001$ | $4.999979$ |
| $4$ | $-0.0001$ | $4.9999998$ | $+0.0001$ | $4.9999998$ |

#### Qualitative Behavior of the Function
The graph $y = f(x)$ is an even, bell-like damped wave symmetric with respect to the $y$-axis. Although $f(0)$ is undefined (division by zero), the two symmetric branches smoothly climb toward the peak height $y = 5$, creating a removable discontinuity at $(0, 5)$.

---

### 3. Comparison of Observation with Analytical Results

In both instances, the empirical observations and tables align with the analytical limits:
- The values of $a_n$ steadily approach $2.5$.
- The values of $f(x)$ symmetrically converge to $5$ with high precision.

---

### 4. Why Finite Calculations or Sketches Do Not Constitute a Proof

1. **The Universal Nature of Quantifiers in Analysis:**
   The mathematical definitions of limits require statements about an infinite number of points:
   - For a sequence, $\lim_{n\to\infty} a_n = L$ requires:

$$
\forall \varepsilon > 0 \quad \exists N \in \mathbb{N} \quad \forall n > N: \quad |a_n - L| < \varepsilon
$$

   - For a function, $\lim_{x\to x_0} f(x) = L$ requires:

$$
\forall \varepsilon > 0 \quad \exists \delta > 0 \quad \forall x \in D: \quad 0 < |x - x_0| < \delta \implies |f(x) - L| < \varepsilon
$$

   A table tests only a finite set of points $\{n_1, \dots, n_k\}$ or $\{x_1, \dots, x_m\}$. A finite sample, no matter how large, cannot verify a property that must hold for an infinite tail of indices or an uncountable continuum of real numbers.

2. **Deceptive Hidden Oscillations:**
   A function may appear to settle when sampled at specific points, yet oscillate wildly between them. Consider

$$
g(x) = \sin\left(\frac{\pi}{x}\right)
$$

   Testing the sequence $x_k = \frac{1}{k}$ yields $g(x_k) = \sin(k\pi) = 0$ for every integer $k \ge 1$. A table of these values suggests that $\lim_{x\to0} g(x) = 0$. However, evaluating at $x'_k = \frac{1}{2k + 1/2}$ yields $g(x'_k) = 1$ for all $k$. In reality, the limit does not exist.

3. **Very Slow Divergence:**
   Consider the partial sums of the harmonic series:

$$
h_n = \sum_{k=1}^n \frac{1}{k}
$$

   For $n = 10^6$, $h_n \approx 14.39$; for $n = 10^9$, $h_n \approx 21.30$. The successive differences $\frac{1}{n}$ become microscopic, which can easily mislead an observer into believing the sequence converges to a finite bound. Yet, the sequence rigorously diverges to $+\infty$.

4. **Floating-Point and Numerical Artifacts:**
   Computing expressions such as $\frac{1 - \cos x}{x^2}$ for $x = 10^{-8}$ on a digital computer produces $0$ due to catastrophic cancellation in standard precision arithmetic, completely disguising the true mathematical limit of $0.5$.

5. **The Epistemological Role of Proof:**
   A mathematical proof uses deductive logic based on the field axioms, order properties, and completeness of the real numbers $\mathbb{R}$. It establishes an unbreakable guarantee that applies universally, whereas numerical tables and visual sketches provide only heuristic motivation and hypothesis generation.

