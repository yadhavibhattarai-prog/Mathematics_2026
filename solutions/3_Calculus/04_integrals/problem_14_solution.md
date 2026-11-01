## Question

### Problem 14. A Piecewise-Defined Function

Let

$$
f(x)=
\begin{cases}
 x+1, & -1\le x<1, \\
 2, & 1\le x\le 3.
\end{cases}
$$

Sketch the graph, decide where to split the integral, compute

$$
\int_{-1}^{3}f(x)\,dx,
$$

and verify the result geometrically.

> **Why this problem:** it requires understanding the definition of the function before carrying out the calculation.

## Solution

### 1. Sketch and splitting point

The function is piecewise-defined, and the formula changes at $x=1$. Therefore, we split the integral at $x=1$.

For $-1\le x<1$:

$$
f(x)=x+1,
$$

which is a line with slope $1$ and $y$-intercept $1$.

For $1\le x\le 3$:

$$
f(x)=2,
$$

which is a horizontal line.

So,

$$
\int_{-1}^{3}f(x)\,dx
= \int_{-1}^{1}(x+1)\,dx + \int_{1}^{3}2\,dx.
$$

### 2. Compute the first integral

$$
\int_{-1}^{1}(x+1)\,dx
= \left[\frac{x^2}{2}+x\right]_{-1}^{1}.
$$

Evaluate:

$$
\left(\frac{1}{2}+1\right)-\left(\frac{1}{2}-1\right)=\frac{3}{2}-\left(-\frac{1}{2}\right)=2.
$$

So,

$$
\int_{-1}^{1}(x+1)\,dx=2.
$$

### 3. Compute the second integral

$$
\int_1^3 2\,dx = 2(3-1)=4.
$$

### 4. Total integral

Therefore,

$$
\int_{-1}^{3}f(x)\,dx = 2 + 4 = 6.
$$

### 5. Geometric verification

- On $[-1,1]$, the graph is the line $y=x+1$, and the area under it from $x=-1$ to $x=1$ is $2$.
- On $[1,3]$, the graph is the horizontal line $y=2$, so the area is a rectangle of width $2$ and height $2$, giving area $4$.

Total area:

$$
2+4=6.
$$

This matches the value of the definite integral, confirming the result.
