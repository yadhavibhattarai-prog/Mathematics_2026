# Exercise 12. Exponential Function Limit

Compute

$$
\lim_{x\to0}(1+3x)^{1/x}.
$$

Connect the result with the limit from Exercise 5 and show the appropriate transformation.

> **Why this exercise:** teaches how to recognize the classical pattern after a transformation.

## Solution

### 1. Connection with Exercise 5

In Exercise 5, the fundamental sequence limit defining Euler's number was established:

$$
\lim_{n\to\infty}\left(1+\frac{1}{n}\right)^n = e
$$

Setting $u = \frac{1}{n}$, as $n \to \infty$ we have $u \to 0^+$. More generally, for a continuous real variable $u \to 0$ (both from the left and right), the fundamental exponential limit is

$$
\lim_{u\to0}(1+u)^{1/u} = e
$$

This is the canonical pattern for indeterminate forms of type $1^\infty$.

---

### 2. Algebraic Transformation

In the given expression

$$
(1+3x)^{1/x}
$$

the term added to $1$ is $3x$.
As $x \to 0$, we have $3x \to 0$, while the exponent $\frac{1}{x} \to \pm\infty$, forming an indeterminate expression of type $1^\infty$.

To match the fundamental pattern $(1+u)^{1/u}$, rewrite the exponent $\frac{1}{x}$ by introducing the factor $3$:

$$
\frac{1}{x} = \frac{3}{3x} = \frac{1}{3x} \cdot 3
$$

Using the power of a power property $(a^{bc} = (a^b)^c)$:

$$
(1+3x)^{1/x} = \left((1+3x)^{\frac{1}{3x}}\right)^3
$$

---

### 3. Computation of the Limit

Let $u = 3x$. As $x \to 0$, $u \to 0$.

Substitute $u$ into the inner expression:

$$
\lim_{x\to0}(1+3x)^{\frac{1}{3x}} = \lim_{u\to0}(1+u)^{1/u} = e
$$

Since the function $g(t) = t^3$ is continuous for all $t \in \mathbb{R}$, the limit can be passed inside the exponent:

$$
\lim_{x\to0}(1+3x)^{1/x} = \lim_{x\to0}\left((1+3x)^{\frac{1}{3x}}\right)^3 = \left(\lim_{u\to0}(1+u)^{1/u}\right)^3 = e^3
$$

---

### 4. Alternative Derivation via Natural Logarithm

Express the base and exponent using the exponential identity $y = \exp(\ln y)$:

$$
(1+3x)^{1/x} = \exp\left(\ln\left((1+3x)^{1/x}\right)\right) = \exp\left(\frac{\ln(1+3x)}{x}\right)
$$

Rewrite the fraction in the exponent:

$$
\frac{\ln(1+3x)}{x} = 3 \cdot \frac{\ln(1+3x)}{3x}
$$

Using the fundamental logarithmic limit $\lim_{u\to0}\frac{\ln(1+u)}{u} = 1$ with $u = 3x$:

$$
\lim_{x\to0}\frac{\ln(1+3x)}{x} = 3 \cdot 1 = 3
$$

By continuity of the exponential function:

$$
\lim_{x\to0}(1+3x)^{1/x} = \exp\left(\lim_{x\to0}\frac{\ln(1+3x)}{x}\right) = \exp(3) = e^3
$$

