# Problem 15. The Difference Quotient as a Check of the Derivative

Choose one function from the problem set and a point $x_0$ at which the derivative exists. Compute $f'(x_0)$ exactly, and then calculate

$$
\frac{f(x_0+h)-f(x_0)}h
$$

for $h=1$, $0.1$, and $0.01$. Compare the values with $f'(x_0)$ and explain why the difference quotient approaching a single number is consistent with the definition of the derivative, while a few computations do not replace a limit argument.

> **Why this problem:** it connects the definition of the derivative with concrete calculations and teaches the distinction between observation and proof.

## Solution

### 1. Choice of Function and Point $x_0$

Choose the quadratic function from Problem 10:

$$
f(x) = x^2 - 3x + 1
$$

at the point of tangency

$$
x_0 = 2
$$

---

### 2. Exact Computation of $f'(x_0)$

Using standard differentiation rules:

$$
f'(x) = 2x - 3
$$

Evaluating at $x_0 = 2$:

$$
f'(2) = 2(2) - 3 = 4 - 3 = 1
$$

The exact analytical derivative is $f'(2) = 1$.

---

### 3. Algebraic Expression of the Difference Quotient

Compute the function values:
- At $x_0 = 2$:

$$
f(2) = 2^2 - 3(2) + 1 = 4 - 6 + 1 = -1
$$

- At $x_0 + h = 2 + h$:

$$
\begin{aligned}
f(2 + h) &= (2 + h)^2 - 3(2 + h) + 1 \\
&= (4 + 4h + h^2) - (6 + 3h) + 1 \\
&= h^2 + h - 1
\end{aligned}
$$

Form the difference quotient for any increment $h \neq 0$:

$$
\frac{f(2 + h) - f(2)}{h} = \frac{(h^2 + h - 1) - (-1)}{h} = \frac{h^2 + h}{h} = 1 + h
$$

---

### 4. Numerical Calculations for $h = 1$, $0.1$, and $0.01$

Substitute the three given step sizes into the simplified difference quotient $1 + h$:

1. **For $h = 1$:**

$$
\frac{f(2 + 1) - f(2)}{1} = \frac{f(3) - f(2)}{1} = 1 + 1 = 2
$$

2. **For $h = 0.1$:**

$$
\frac{f(2 + 0.1) - f(2)}{0.1} = \frac{f(2.1) - f(2)}{0.1} = 1 + 0.1 = 1.1
$$

3. **For $h = 0.01$:**

$$
\frac{f(2 + 0.01) - f(2)}{0.01} = \frac{f(2.01) - f(2)}{0.01} = 1 + 0.01 = 1.01
$$

#### Comparison with the Exact Derivative $f'(2) = 1$

| Step Size $h$ | Secant Line Slope $\frac{f(2+h)-f(2)}{h}$ | Exact Tangent Slope $f'(2)$ | Absolute Error $|(1+h) - 1|$ |
|:---:|:---:|:---:|:---:|
| $1.0$ | $2.00$ | $1$ | $1.00$ |
| $0.1$ | $1.10$ | $1$ | $0.10$ |
| $0.01$ | $1.01$ | $1$ | $0.01$ |

As $h$ decreases by powers of $10$, the secant slope rapidly approaches the exact tangent slope $1$, with the error $|(1+h)-1| = h$ scaling in direct proportion to $h$.

---

### 5. Why Observation is Consistent with the Definition, but Does Not Replace a Proof

1. **Consistency with the Formal Definition:**
   The derivative is defined as the limit of the difference quotient as $h \to 0$:

$$
f'(x_0) = \lim_{h\to0}\frac{f(x_0+h)-f(x_0)}{h}
$$

   Our numerical calculations observe secant slopes approaching $1$ as $h$ decreases. This confirms the geometric intuition: the secant line passing through $(x_0, f(x_0))$ and $(x_0+h, f(x_0+h))$ pivots around $(x_0, f(x_0))$ and rotates continuously toward the tangent line.

2. **Why a Finite Number of Computations is Not a Proof:**
   - **Quantifier Scope:** The limit definition requires that for **every** $\varepsilon > 0$, there exists a $\delta > 0$ such that the difference quotient is within $\varepsilon$ of $L$ for **all** $0 < |h| < \delta$. Computing values for three specific choices ($h = 1, 0.1, 0.01$) tests only three points out of an uncountable continuum of possible increments.
   - **Deceptive Functions with High-Frequency Oscillations:** Consider the function

$$
g(x) = x^2\sin\left(\frac{2\pi}{x}\right) \quad (x \neq 0), \qquad g(0) = 0
$$

     If one tests $h_k = \frac{1}{k}$, then $g(h_k) = 0$, giving difference quotients $\frac{g(h_k)-0}{h_k} = 0$ for all $k \in \mathbb{N}$, suggesting an apparent slope of $0$. However, testing intermediate points reveals that the quotient oscillates between $-h$ and $+h$.
   - **Numerical Round-off and Loss of Significance:** In computational mathematics, evaluating $\frac{f(x_0+h)-f(x_0)}{h}$ for extremely small $h$ (e.g. $h = 10^{-16}$) on digital hardware leads to catastrophic cancellation error, causing the computed quotient to diverge or become zero, failing to represent the true mathematical limit.
   - **The Role of the Limit Argument:** The algebraic reduction $\frac{h^2+h}{h} = 1 + h$ followed by the limit $\lim_{h\to0}(1+h) = 1$ is an exact deductive argument valid for every real $h \neq 0$. Only this analytical transition provides an absolute mathematical guarantee.

