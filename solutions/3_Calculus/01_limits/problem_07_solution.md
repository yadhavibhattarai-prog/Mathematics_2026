# Exercise 7. Limit at a Point and Canceling a Factor

Compute

$$
\lim_{x\to3}\frac{x^2-4x+3}{x-3}.
$$

Explain why the value of the function at $x=3$ is not needed to compute the limit.

> **Why this exercise:** separates the concept of a limit from the value of a function at a point.

## Solution

### 1. Calculation of the Limit

Direct substitution of $x = 3$ yields

$$
\frac{3^2 - 4(3) + 3}{3 - 3} = \frac{9 - 12 + 3}{0} = \frac{0}{0}
$$

which is an indeterminate form.

Factor the quadratic numerator. The roots of $x^2 - 4x + 3 = 0$ are:

$$
\Delta = (-4)^2 - 4(1)(3) = 16 - 12 = 4
$$

$$
x_1 = \frac{4 - 2}{2} = 1, \qquad x_2 = \frac{4 + 2}{2} = 3
$$

Thus, the numerator factors as

$$
x^2 - 4x + 3 = (x - 1)(x - 3)
$$

Substitute the factorization into the fraction:

$$
\frac{x^2 - 4x + 3}{x-3} = \frac{(x-1)(x-3)}{x-3}
$$

In the definition of the limit as $x \to 3$, $x$ approaches $3$ but is strictly not equal to $3$ ($x \neq 3$). Therefore, the denominator $x - 3 \neq 0$, which allows us to cancel the common factor $(x - 3)$:

$$
\frac{(x-1)(x-3)}{x-3} = x - 1 \qquad (x \neq 3)
$$

Taking the limit:

$$
\lim_{x\to3}\frac{x^2-4x+3}{x-3} = \lim_{x\to3}(x - 1) = 3 - 1 = 2
$$

---

### 2. Why the Function Value at $x = 3$ is Not Needed

1. **Definition of a Limit at a Point:**
   The formal definition states that $\lim_{x\to x_0} f(x) = L$ if for every $\varepsilon > 0$, there exists a $\delta > 0$ such that:

$$
0 < |x - x_0| < \delta \implies |f(x) - L| < \varepsilon
$$

   The condition $0 < |x - x_0|$ explicitly excludes the point $x = x_0$ itself. The limit depends strictly on the values assumed by $f(x)$ on a punctured neighborhood of $x_0$, never on $f(x_0)$.
2. **The Function is Not Even Defined at $x = 3$:**
   For $f(x) = \frac{x^2-4x+3}{x-3}$, the domain is $D = \mathbb{R} \setminus \{3\}$. The value $f(3)$ does not exist because division by zero is undefined in arithmetic. The non-existence of $f(3)$ does not hinder the existence of the limit in any way.
3. **Geometric Meaning:**
   The graph of $y = \frac{x^2-4x+3}{x-3}$ is the straight line $y = x - 1$ with a single missing point (a removable discontinuity or "hole") at $(3, 2)$. As $x$ approaches $3$ from either side, the points $(x, f(x))$ on the line approach the coordinates $(3, 2)$, meaning the limit is $2$ regardless of what happens at $x = 3$.
