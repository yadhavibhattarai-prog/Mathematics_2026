# Problem 5. An Exponential Function with a Maximum

Analyze the monotonicity and extrema of

$$
f(x)=xe^{-x}.
$$

Also examine the behavior as $x\to\infty$ and explain how the limit affects the shape of the graph on the right-hand side.

> **Why this problem:** it combines the derivative with a limit in the description of the global behavior of a function.

## Solution

### 1. Domain and Derivative

The function is defined for all real numbers:

$$
D_f = \mathbb{R}
$$

Apply the product rule and chain rule to differentiate $f(x) = x e^{-x}$:

$$
\begin{aligned}
f'(x) &= \frac{d}{dx}(x) \cdot e^{-x} + x \cdot \frac{d}{dx}\left(e^{-x}\right) \\
&= 1 \cdot e^{-x} + x \cdot \left(-e^{-x}\right) \\
&= (1 - x)e^{-x}
\end{aligned}
$$

---

### 2. Critical Points

Because the exponential factor is strictly positive for all real $x$:

$$
e^{-x} > 0 \quad (x \in \mathbb{R})
$$

the critical points occur where $1 - x = 0$:

$$
f'(x) = 0 \iff 1 - x = 0 \implies x = 1
$$

The unique critical point is $x = 1$.

---

### 3. Monotonicity and Local Extrema

The sign of $f'(x) = (1 - x)e^{-x}$ is governed entirely by the linear factor $1 - x$:

- **On $(-\infty, 1)$:**
  For $x < 1$, we have $1 - x > 0$, so $f'(x) > 0$.
  The function $f$ is strictly increasing on $(-\infty, 1]$.

- **On $(1, \infty)$:**
  For $x > 1$, we have $1 - x < 0$, so $f'(x) < 0$.
  The function $f$ is strictly decreasing on $[1, \infty)$.

- **At $x = 1$:**
  Because the derivative changes sign from positive to negative, the function attains a **local maximum** at $x = 1$.
  Since $f$ increases on $(-\infty, 1]$ and decreases on $[1, \infty)$, this point is also the **strict global maximum** of $f$ on $\mathbb{R}$.

Calculate the maximum value:

$$
f(1) = 1 \cdot e^{-1} = \frac{1}{e} \approx 0.3679
$$

The maximum point on the graph is $\left(1, \frac{1}{e}\right)$.

---

### 4. Behavior as $x \to \infty$

Write the function as a quotient:

$$
f(x) = \frac{x}{e^x}
$$

As $x \to \infty$, both $x \to \infty$ and $e^x \to \infty$. By the standard hierarchy of growth rates (or by applying l'Hôpital's rule once):

$$
\lim_{x\to\infty} x e^{-x} = \lim_{x\to\infty}\frac{x}{e^x} = \lim_{x\to\infty}\frac{1}{e^x} = 0
$$

The horizontal line

$$
y = 0
$$

is a horizontal asymptote of the graph as $x \to +\infty$.

---

### 5. Effect of the Limit on the Shape of the Graph on the Right-Hand Side

1. **Positivity for Positive $x$:**
   For all $x > 0$, $x > 0$ and $e^{-x} > 0$, so $f(x) > 0$. The graph remains strictly above the $x$-axis.
2. **Asymptotic Flattening:**
   After peaking at the maximum point $\left(1, \frac{1}{e}\right)$, the graph slopes downward ($f'(x) < 0$), but it cannot cross below $y = 0$. Instead, the rate of descent diminishes as the graph flattens, approaching the $x$-axis from above.
3. **Inflection Point:**
   The second derivative is

$$
f''(x) = \frac{d}{dx}\left((1-x)e^{-x}\right) = -e^{-x} - (1-x)e^{-x} = (x - 2)e^{-x}
$$

   At $x = 2$, $f''(2) = 0$, and $f''$ changes from negative to positive.
   Thus, for $1 < x < 2$, the graph is concave down (curving away from the peak), and at the inflection point $\left(2, \frac{2}{e^2}\right) \approx (2, 0.2707)$, the curve switches to being concave up, creating the smooth, asymptotic tail that glides along the horizontal asymptote $y = 0$.

