# Problem 6. A Logarithmic Function

Analyze the domain, zero, and monotonicity of

$$
f(x)=\ln x-x+1.
$$

Explain why the analysis must begin with the domain.

> **Why this problem:** it reinforces the role of the domain and derivative in the analysis of a logarithmic function.

## Solution

### 1. Why the Analysis Must Begin with the Domain

The natural logarithm $\ln x$ is defined strictly for positive real arguments ($x > 0$).
Attempting to analyze the function, find its zeros, or differentiate without first determining its domain leads to significant errors:
- Evaluating $f(x)$ at non-positive numbers (such as $x = 0$ or $x = -2$) produces mathematically undefined quantities.
- The derivative $f'(x) = \frac{1}{x} - 1 = \frac{1-x}{x}$ exists algebraically at negative values (e.g. $f'(-1) = -2$), but these values have no mathematical connection to $f$, because $f$ does not exist for $x \le 0$.
Establishing the domain at the very beginning sets the valid boundary of all subsequent investigations.

The domain is

$$
D_f = (0, \infty)
$$

---

### 2. Derivative and Critical Points

Differentiate $f(x) = \ln x - x + 1$ on its domain $(0, \infty)$:

$$
f'(x) = \frac{1}{x} - 1 = \frac{1 - x}{x}
$$

Find the critical points by setting $f'(x) = 0$:

$$
\frac{1 - x}{x} = 0 \iff 1 - x = 0 \implies x = 1
$$

Since $1 \in D_f$, $x = 1$ is the unique critical point.

---

### 3. Monotonicity and Global Maximum

For all $x \in D_f = (0, \infty)$, the denominator of $f'(x)$ is strictly positive ($x > 0$). The sign of $f'(x)$ is therefore identical to the sign of the numerator $1 - x$:

- **On $(0, 1)$:**
  For $0 < x < 1$, we have $1 - x > 0 \implies f'(x) > 0$.
  The function $f$ is strictly increasing on $(0, 1]$.

- **On $(1, \infty)$:**
  For $x > 1$, we have $1 - x < 0 \implies f'(x) < 0$.
  The function $f$ is strictly decreasing on $[1, \infty)$.

Because $f$ increases on $(0, 1]$ and decreases on $[1, \infty)$, the point $x = 1$ is the **strict global maximum** of $f(x)$ on its entire domain.

Evaluate the maximum value:

$$
f(1) = \ln(1) - 1 + 1 = 0 - 1 + 1 = 0
$$

The global maximum point on the graph is $(1, 0)$.

---

### 4. Determination of the Zeros

A zero of $f(x)$ is an argument $x \in D_f$ such that $f(x) = 0$.

From the evaluation above:

$$
f(1) = 0
$$

so $x = 1$ is a zero.

Furthermore, because $0$ is the unique, strict global maximum value of $f(x)$ on $(0, \infty)$:

$$
f(x) < f(1) = 0 \quad (x \in (0, \infty) \setminus \{1\})
$$

The function is strictly negative for every $x \neq 1$.
Consequently, $x = 1$ is the **only zero** of $f(x)$.

---

### 5. Theoretical Consequence: The Fundamental Logarithmic Inequality

Because $f(x) \le 0$ for all $x > 0$:

$$
\ln x - x + 1 \le 0 \implies \ln x \le x - 1 \quad (x > 0)
$$

with equality if and only if $x = 1$. The tangent line $y = x - 1$ at $(1, 0)$ lies strictly above the logarithmic curve $y = \ln x$ for all $x \neq 1$.

