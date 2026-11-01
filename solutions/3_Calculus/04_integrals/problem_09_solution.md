## Question

### Problem 9. Definite Integral and Geometric Area

Compute

$$
\int_{-1}^{2}x\,dx.
$$

Then separately compute the areas of the parts of the graph below and above the $x$-axis and explain the difference between the definite integral and geometric area.

> **Why this problem:** it clarifies the difference between signed accumulation and area.

## Solution

First compute the definite integral:

$$
\int_{-1}^{2} x\,dx = \left[\frac{x^2}{2}\right]_{-1}^{2}.
$$

Evaluate at the endpoints:

$$
\frac{2^2}{2} - \frac{(-1)^2}{2} = \frac{4}{2} - \frac{1}{2} = 2 - \frac{1}{2} = \frac{3}{2}.
$$

So

$$
\int_{-1}^{2} x\,dx = \frac{3}{2}.
$$

### Geometric interpretation

The graph of $y=x$ is a line through the origin.

- On the interval $[-1,0]$, the graph lies below the $x$-axis, so the signed contribution is negative.
- On the interval $[0,2]$, the graph lies above the $x$-axis, so the contribution is positive.

Compute the signed area pieces:

$$
\int_{-1}^{0} x\,dx = \left[\frac{x^2}{2}\right]_{-1}^{0} = 0 - \frac{1}{2} = -\frac{1}{2}.
$$

$$
\int_{0}^{2} x\,dx = \left[\frac{x^2}{2}\right]_{0}^{2} = 2.
$$

Thus the definite integral is

$$
-\frac{1}{2}+2 = \frac{3}{2}.
$$

### Geometric area (not signed)

The area below the $x$-axis from $-1$ to $0$ is

$$
\text{Area}_1 = \frac{1}{2}.
$$

The area above the $x$-axis from $0$ to $2$ is

$$
\text{Area}_2 = \frac{1}{2}(2)(2)=2.
$$

So the total geometric area is

$$
\text{Area} = \frac{1}{2} + 2 = \frac{5}{2}.
$$

### Difference between definite integral and area

- The definite integral measures the signed accumulation: regions below the axis contribute negatively and regions above the axis contribute positively.
- Geometric area always counts length as positive, regardless of whether the curve is below or above the axis.

Hence:

$$
\int_{-1}^{2}x\,dx = \frac{3}{2}, \qquad \text{but} \qquad \text{geometric area} = \frac{5}{2}.
$$
