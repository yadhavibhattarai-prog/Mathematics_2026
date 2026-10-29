# Problem 10. The Tangent Line as an Application of the Derivative

For

$$
f(x)=x^2-3x+1
$$

find the equation of the tangent line at the point with $x=2$. Give the point of tangency, the value $f'(2)$, the equation of the line, and verify that the point lies on the obtained tangent line.

> **Why this problem:** it combines the derivative and the equation of a line into a complete geometric problem.

## Solution

### 1. Point of Tangency

The $x$-coordinate is given as $x_0 = 2$.
Compute the corresponding $y$-coordinate by evaluating the function:

$$
y_0 = f(2) = 2^2 - 3(2) + 1 = 4 - 6 + 1 = -1
$$

The point of tangency on the parabola is

$$
P = (x_0, y_0) = (2, -1)
$$

---

### 2. Computing the Derivative and the Value $f'(2)$

Differentiate $f(x)$ using the power and sum rules:

$$
f'(x) = \frac{d}{dx}(x^2 - 3x + 1) = 2x - 3
$$

Evaluate the derivative at the point of tangency $x_0 = 2$:

$$
f'(2) = 2(2) - 3 = 4 - 3 = 1
$$

The slope of the tangent line is $m = f'(2) = 1$.

---

### 3. Equation of the Tangent Line

The point-slope form of the equation of a straight line with slope $m$ passing through $(x_0, y_0)$ is

$$
y - y_0 = f'(x_0)(x - x_0)
$$

Substitute $x_0 = 2$, $y_0 = -1$, and $f'(2) = 1$:

$$
y - (-1) = 1(x - 2)
$$

$$
y + 1 = x - 2
$$

Subtract $1$ from both sides to obtain the slope-intercept form:

$$
y = x - 3
$$

(or in general form: $x - y - 3 = 0$).

---

### 4. Verification that the Point Lies on the Tangent Line

Substitute the coordinates of the tangency point $P(2, -1)$ into the obtained line equation:

- Left-hand side:

$$
y = -1
$$

- Right-hand side:

$$
x - 3 = 2 - 3 = -1
$$

Since $-1 = -1$, the point of tangency $P(2, -1)$ satisfies the equation of the tangent line.

Furthermore, we can verify that the tangent line intersects the parabola with multiplicity $2$:

$$
f(x) - y_{\mathrm{tangent}} = (x^2 - 3x + 1) - (x - 3) = x^2 - 4x + 4 = (x - 2)^2
$$

The difference is a perfect square $(x - 2)^2 \ge 0$, which confirms that the line touches the curve at $x = 2$ and lies entirely below the parabola elsewhere.

