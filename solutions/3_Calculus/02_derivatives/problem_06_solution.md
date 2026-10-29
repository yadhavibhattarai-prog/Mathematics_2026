# Problem 6. Product Rule and Trigonometry

For

$$
f(x)=x\sin x+\cos x
$$

compute the derivative and simplify the result. Then compute $f'(0)$ and interpret the direction of the tangent line at that point.

> **Why this problem:** it combines the product rule with trigonometric derivatives and geometric interpretation.

## Solution

### 1. Computing the Derivative and Simplifying

The function is a sum of two terms:

$$
f(x) = x\sin x + \cos x
$$

Apply the sum rule:

$$
f'(x) = \frac{d}{dx}(x\sin x) + \frac{d}{dx}(\cos x)
$$

For the first term, apply the product rule with $u(x) = x$ and $v(x) = \sin x$:

$$
\frac{d}{dx}(x\sin x) = (1)\sin x + x(\cos x) = \sin x + x\cos x
$$

For the second term, use the standard derivative of the cosine function:

$$
\frac{d}{dx}(\cos x) = -\sin x
$$

Add the two results:

$$
f'(x) = (\sin x + x\cos x) + (-\sin x)
$$

Notice that $\sin x$ and $-\sin x$ cancel out completely:

$$
f'(x) = x\cos x
$$

---

### 2. Computing $f'(0)$

Substitute $x = 0$ into the simplified derivative:

$$
f'(0) = 0 \cdot \cos(0) = 0 \cdot 1 = 0
$$

---

### 3. Geometric Interpretation of the Tangent Line at $x = 0$

- **Slope:**
  The derivative at $x = 0$ is $m = f'(0) = 0$. A slope of zero means that the tangent line is **horizontal** (strictly parallel to the $x$-axis).
- **Point of Tangency:**
  The $y$-coordinate at $x = 0$ is

$$
f(0) = 0 \cdot \sin(0) + \cos(0) = 0 + 1 = 1
$$

  The point of tangency on the graph is $(0, 1)$.
- **Equation of the Tangent Line:**
  In point-slope form:

$$
y - 1 = 0 \cdot (x - 0) \implies y = 1
$$

- **Behavior Near $x = 0$:**
  Because $f'(0) = 0$, $x = 0$ is a stationary (critical) point of the function.
  For small $x \neq 0$, $\cos x \approx 1 > 0$, so $f'(x) = x\cos x$ has the same sign as $x$:
  - For $x < 0$, $f'(x) < 0$ (the function is decreasing).
  - For $x > 0$, $f'(x) > 0$ (the function is increasing).
  Because the derivative changes sign from negative to positive at $x = 0$, the function achieves a local minimum at $(0, 1)$, and the horizontal tangent line $y = 1$ touches the bottom of this local valley.

