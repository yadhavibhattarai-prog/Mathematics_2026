# Problem 11. Derivative from the Definition

Using only

$$
f'(x)=\lim_{h\to0}\frac{f(x+h)-f(x)}h,
$$

find the derivative of $f(x)=x^2$. Compare the result with the power rule and indicate where the limit is used in the calculation.

> **Why this problem:** it shows the origin of the power rule and the direct connection between the derivative and a limit.

## Solution

### 1. Setting Up the Difference Quotient

For the function $f(x) = x^2$, the value at the shifted argument $x + h$ is

$$
f(x + h) = (x + h)^2
$$

Expand using the binomial expansion:

$$
(x + h)^2 = x^2 + 2xh + h^2
$$

The difference quotient (average rate of change) for an increment $h \neq 0$ is

$$
\frac{f(x + h) - f(x)}{h} = \frac{(x^2 + 2xh + h^2) - x^2}{h}
$$

Cancel the term $x^2$:

$$
\frac{2xh + h^2}{h}
$$

Factor out $h$ from the numerator:

$$
\frac{h(2x + h)}{h}
$$

Because $h \neq 0$ in the difference quotient, cancel $h$ from the numerator and denominator:

$$
\frac{f(x + h) - f(x)}{h} = 2x + h \qquad (h \neq 0)
$$

---

### 2. Evaluating the Limit to Find $f'(x)$

Apply the definition of the derivative:

$$
f'(x) = \lim_{h\to0}\frac{f(x + h) - f(x)}{h} = \lim_{h\to0}(2x + h)
$$

Since $2x + h$ is a continuous polynomial in $h$, the limit as $h \to 0$ is obtained by direct evaluation:

$$
f'(x) = 2x + 0 = 2x
$$

---

### 3. Comparison with the Power Rule

The standard power rule states that for any real exponent $n$:

$$
\frac{d}{dx}[x^n] = n x^{n-1}
$$

For $n = 2$:

$$
\frac{d}{dx}[x^2] = 2 x^{2-1} = 2x^1 = 2x
$$

The result obtained directly from the limit definition agrees with the power rule.

---

### 4. Where the Limit is Used in the Calculation

The limit operation $\lim_{h\to0}$ plays two essential and distinct roles in the calculation:

1. **Resolving the Indeterminate Form $\frac{0}{0}$:**
   Evaluating the difference quotient $\frac{f(x+h)-f(x)}{h}$ at $h = 0$ directly produces $\frac{0}{0}$, which is undefined. The definition of a limit allows us to study the behavior for $h$ arbitrarily close to $0$ without setting $h$ equal to $0$. This justifies canceling the factor $h$ from numerator and denominator before passing to the limit.
2. **Eliminating the Infinitesimal Remainder $h$:**
   After canceling $h$, the difference quotient simplifies to the exact linear expression $2x + h$. This represents the secant line slope over a finite interval $[x, x+h]$.
   The limit step $\lim_{h\to0}(2x + h)$ lets the secant line collapse into the tangent line, discarding the second-order increment $h$ while rigorously preserving the instantaneous rate of change $2x$.

