# Problem 7. A Trigonometric Composition

For

$$
f(x)=\sin(x^2+1)
$$

compute the derivative. Explicitly identify the outer function, the inner function, and the derivative of the inner function. Finally, determine the sign of $f'(0)$.

> **Why this problem:** it reinforces the chain rule in a different type of composition.

## Solution

### 1. Identifying the Components of the Composition

The function is a composite function of the form $f(x) = g(u(x))$:

- **Inner function:**

$$
u(x) = x^2 + 1
$$

- **Outer function:**

$$
g(u) = \sin u
$$

- **Derivative of the outer function with respect to $u$:**

$$
g'(u) = \cos u
$$

- **Derivative of the inner function with respect to $x$:**

$$
u'(x) = \frac{d}{dx}(x^2 + 1) = 2x
$$

---

### 2. Computing the Derivative via the Chain Rule

By the chain rule:

$$
f'(x) = g'(u(x)) \cdot u'(x)
$$

Substitute the expressions:

$$
f'(x) = \cos(x^2 + 1) \cdot (2x) = 2x\cos(x^2 + 1)
$$

---

### 3. Evaluating and Determining the Sign of $f'(0)$

Substitute $x = 0$ into the derivative:

$$
f'(0) = 2(0)\cos(0^2 + 1) = 0 \cdot \cos(1) = 0
$$

#### Analysis of the Sign
The value $f'(0) = 0$ is exactly zero. It is neither strictly positive ($f'(0) > 0$) nor strictly negative ($f'(0) < 0$).

#### Geometric Significance
At $x = 0$, the tangent line to the graph of $f(x)$ is horizontal (slope $m = 0$). Because $\cos(1) \approx 0.5403 > 0$, the sign of $f'(x) = 2x\cos(x^2+1)$ in a small neighborhood around $x = 0$ is governed entirely by $2x$:
- For $x \in (-\varepsilon, 0)$, $f'(x) < 0$ (the function is decreasing).
- For $x \in (0, \varepsilon)$, $f'(x) > 0$ (the function is increasing).
Therefore, $x = 0$ is a stationary point corresponding to a local minimum of $f(x)$.

