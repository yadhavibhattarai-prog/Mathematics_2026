# Problem 5. The Chain Rule as Working Through Layers

For

$$
f(x)=(3x^2-2x+1)^5
$$

identify the inner and outer functions, compute their derivatives, and combine the result according to the chain rule. Explain the origin of the additional factor.

> **Why this problem:** it teaches how to recognize the structure of a composition instead of memorizing the rule as a meaningless pattern.

## Solution

### 1. Identifying the Inner and Outer Functions

The expression is a composition of two functions:

$$
f(x) = g(u(x))
$$

- **Inner function:**

$$
u(x) = 3x^2 - 2x + 1
$$

- **Outer function:**

$$
g(u) = u^5
$$

---

### 2. Computing the Individual Derivatives

- **Derivative of the outer function with respect to $u$:**
  By the power rule:

$$
g'(u) = \frac{dg}{du} = 5u^4
$$

- **Derivative of the inner function with respect to $x$:**
  By the sum and power rules:

$$
u'(x) = \frac{du}{dx} = \frac{d}{dx}(3x^2 - 2x + 1) = 6x - 2 = 2(3x - 1)
$$

---

### 3. Combining the Result via the Chain Rule

According to the chain rule:

$$
f'(x) = g'(u(x)) \cdot u'(x)
$$

Substitute $u(x) = 3x^2 - 2x + 1$, $g'(u) = 5u^4$, and $u'(x) = 6x - 2$:

$$
\begin{aligned}
f'(x) &= 5(3x^2 - 2x + 1)^4 \cdot (6x - 2) \\
&= 10(3x - 1)(3x^2 - 2x + 1)^4
\end{aligned}
$$

---

### 4. Origin of the Additional Factor

The additional factor $(6x - 2)$ is the derivative of the inner function, $u'(x) = \frac{du}{dx}$.

#### Why It Must Appear
When the input $x$ is nudged by a tiny amount $\Delta x$:
1. The inner quantity $u = 3x^2 - 2x + 1$ does not stay constant; it changes by approximately

$$
\Delta u \approx u'(x)\,\Delta x = (6x - 2)\,\Delta x
$$

2. The outer quantity $g(u) = u^5$ responds to this shift $\Delta u$ with an amplification factor given by its own sensitivity:

$$
\Delta g \approx g'(u)\,\Delta u = 5u^4\,\Delta u
$$

3. Combining these two successive rate transfers by substitution:

$$
\Delta f \approx 5u^4 \cdot \left((6x - 2)\,\Delta x\right) = 5(3x^2 - 2x + 1)^4 (6x - 2)\,\Delta x
$$

Dividing by $\Delta x$ and taking the limit as $\Delta x \to 0$ yields the product of rates in Leibniz notation:

$$
\frac{df}{dx} = \frac{dg}{du} \cdot \frac{du}{dx}
$$

Without the additional factor $(6x - 2)$, one would incorrectly treat the base of the power as an independent variable, ignoring how fast the base itself varies as $x$ moves.

