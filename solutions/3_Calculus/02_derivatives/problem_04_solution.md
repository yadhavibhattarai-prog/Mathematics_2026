# Problem 4. A Quotient and Domain Control

For

$$
f(x)=\frac{x^2+1}{x-1}
$$

determine the domain, compute the derivative, simplify the result, and explain why the restriction $x\neq1$ remains important.

> **Why this problem:** it practices the quotient rule together with domain control.

## Solution

### 1. Determining the Domain of $f$

The function is a rational expression. Division by zero is undefined, so the denominator must not vanish:

$$
x - 1 \neq 0 \implies x \neq 1
$$

The domain is

$$
D_f = \mathbb{R} \setminus \{1\} = (-\infty, 1) \cup (1, \infty)
$$

---

### 2. Computing the Derivative Using the Quotient Rule

The quotient rule states that for $f(x) = \frac{u(x)}{v(x)}$:

$$
f'(x) = \frac{u'(x)v(x) - u(x)v'(x)}{[v(x)]^2}
$$

Set

$$
u(x) = x^2 + 1 \implies u'(x) = 2x
$$

$$
v(x) = x - 1 \implies v'(x) = 1
$$

Substitute into the quotient rule:

$$
\begin{aligned}
f'(x) &= \frac{(2x)(x - 1) - (x^2 + 1)(1)}{(x - 1)^2} \\
&= \frac{2x^2 - 2x - x^2 - 1}{(x - 1)^2} \\
&= \frac{x^2 - 2x - 1}{(x - 1)^2}
\end{aligned}
$$

---

### 3. Simplifying the Result

The numerator can be rewritten by completing the square:

$$
x^2 - 2x - 1 = (x - 1)^2 - 2
$$

Dividing term by term yields an alternative simplified representation:

$$
f'(x) = \frac{(x - 1)^2 - 2}{(x - 1)^2} = 1 - \frac{2}{(x - 1)^2}
$$

Both representations are valid canonical forms of the derivative.

---

### 4. Why the Restriction $x \neq 1$ Remains Important

1. **Existence of the Function and Derivative:**
   At $x = 1$, the function $f(1)$ is not defined because the denominator is zero while the numerator is $1^2 + 1 = 2 \neq 0$. The line $x = 1$ is a vertical asymptote of the graph. Because a function cannot be differentiable at a point where it is not even defined, the derivative $f'(1)$ does not exist.
2. **Domain of the Derivative:**
   The derivative formula contains $(x - 1)^2$ in its denominator, which vanishes at $x = 1$. The domain of the derivative is strictly

$$
D_{f'} = \mathbb{R} \setminus \{1\}
$$

3. **Separation of the Domain into Disconnected Components:**
   The restriction $x \neq 1$ splits the domain into two disjoint open intervals, $(-\infty, 1)$ and $(1, \infty)$. Theorems of calculus (such as the Mean Value Theorem or testing for monotonicity via the sign of $f'$) apply only to connected intervals. For instance, while $f'(x)$ determines where the function increases or decreases on $(-\infty, 1)$ and on $(1, \infty)$ individually, one cannot compare values across the asymptote at $x = 1$ without accounting for the discontinuity.

