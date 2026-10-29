# Problem 1. Derivative of a Polynomial and the Slope of a Tangent Line

For

$$
f(x)=3x^5-2x^3+7x-4
$$

find $f'(x)$. Then compute $f'(0)$ and $f'(1)$, determine the signs of the obtained values, and explain what they say about the slope of the tangent line to the graph at these two points.

> **Why this problem:** it reinforces the power rule and connects the value of the derivative at a point with the geometric meaning of the tangent slope.

## Solution

### 1. Computation of the Derivative $f'(x)$

Apply the power rule $\frac{d}{dx}[x^n] = n x^{n-1}$, the constant multiple rule, and the sum/difference rule:

$$
\begin{aligned}
f'(x) &= \frac{d}{dx}(3x^5) - \frac{d}{dx}(2x^3) + \frac{d}{dx}(7x) - \frac{d}{dx}(4) \\
&= 3(5x^4) - 2(3x^2) + 7(1) - 0 \\
&= 15x^4 - 6x^2 + 7
\end{aligned}
$$

---

### 2. Computing $f'(0)$ and $f'(1)$

- **At $x = 0$:**

$$
f'(0) = 15(0)^4 - 6(0)^2 + 7 = 7
$$

- **At $x = 1$:**

$$
f'(1) = 15(1)^4 - 6(1)^2 + 7 = 15 - 6 + 7 = 16
$$

---

### 3. Signs of the Obtained Values

- $f'(0) = 7 > 0$ (strictly positive).
- $f'(1) = 16 > 0$ (strictly positive).

In fact, $f'(x) > 0$ for all real $x$ because

$$
15x^4 - 6x^2 + 7 = 15\left(x^2 - \frac{1}{5}\right)^2 + \frac{32}{5} \ge \frac{32}{5} > 0
$$

---

### 4. Geometric Meaning of the Tangent Slope

The derivative of a function at a point $x_0$ gives the slope $m$ of the tangent line to the graph $y = f(x)$ at the point $(x_0, f(x_0))$:

$$
m = \tan\theta = f'(x_0)
$$

where $\theta$ is the inclination angle of the tangent line relative to the positive $x$-axis.

- **At $x = 0$:**
  The slope is $m = 7 > 0$. The tangent line slants upwards from left to right at a steep angle $\theta = \arctan(7) \approx 81.87^\circ$. A positive slope indicates that the function is strictly increasing in an open neighborhood of $x = 0$.
- **At $x = 1$:**
  The slope is $m = 16 > 0$. The tangent line slants upwards even more steeply, with inclination angle $\theta = \arctan(16) \approx 86.42^\circ$.
- **Comparison:**
  Because $f'(1) = 16 > 7 = f'(0)$, the tangent line is steeper at $x = 1$ than at $x = 0$, meaning that the function values grow more rapidly per unit increase in $x$ at $x = 1$ than at $x = 0$.

