# Problem 2. Powers, Roots, and the Domain

For

$$
f(x)=2\sqrt{x}-\frac{3}{x^2}+x^{3/2}
$$

1. rewrite the function using powers,
2. determine the domain,
3. compute the derivative,
4. compare the domain of the function with the domain of its derivative.

> **Why this problem:** it teaches how to rewrite different forms so that the power rule can be applied and how to keep track of the domain.

## Solution

### 1. Rewriting the Function Using Powers

Using standard exponent rules:
- $\sqrt{x} = x^{1/2}$
- $\frac{1}{x^2} = x^{-2}$
- $x^{3/2} = x^{3/2}$

The function is expressed as a sum of power terms:

$$
f(x) = 2x^{1/2} - 3x^{-2} + x^{3/2}
$$

---

### 2. Domain of the Function $D_f$

Examine each term individually:
1. $2\sqrt{x} = 2x^{1/2}$ requires the radicand to be non-negative: $x \ge 0$.
2. $-\frac{3}{x^2} = -3x^{-2}$ requires a non-zero denominator: $x \neq 0$.
3. $x^{3/2} = (\sqrt{x})^3$ requires $x \ge 0$.

Taking the intersection of all conditions:

$$
x > 0
$$

The domain of the function is

$$
D_f = (0, \infty)
$$

---

### 3. Computation of the Derivative $f'(x)$

Apply the power rule $\frac{d}{dx}[x^r] = r x^{r-1}$ to each term:

$$
\begin{aligned}
f'(x) &= 2\left(\frac{1}{2}x^{\frac{1}{2}-1}\right) - 3\left(-2x^{-2-1}\right) + \frac{3}{2}x^{\frac{3}{2}-1} \\
&= x^{-1/2} + 6x^{-3} + \frac{3}{2}x^{1/2}
\end{aligned}
$$

Rewriting in radical and fractional notation:

$$
f'(x) = \frac{1}{\sqrt{x}} + \frac{6}{x^3} + \frac{3}{2}\sqrt{x}
$$

---

### 4. Comparison of the Domains $D_f$ and $D_{f'}$

Examine the requirements for the derivative $f'(x)$:
- $\frac{1}{\sqrt{x}}$ requires $x > 0$ (both non-negative for the root and non-zero for the denominator).
- $\frac{6}{x^3}$ requires $x \neq 0$.
- $\frac{3}{2}\sqrt{x}$ requires $x \ge 0$.

Taking the intersection of these conditions:

$$
D_{f'} = (0, \infty)
$$

#### Comparison
The two domains coincide:

$$
D_f = D_{f'} = (0, \infty)
$$

In general, root functions such as $\sqrt{x}$ are defined on $[0, \infty)$ but have derivatives defined only on $(0, \infty)$ because the tangent slope becomes vertical as $x \to 0^+$. In this specific problem, however, the term $-\frac{3}{x^2}$ already excluded $x = 0$ from the domain of $f$, which is why the domain of the function and the domain of its derivative are identical.
