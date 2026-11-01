## Question

### Problem 12. Symmetry, Sign, and Absolute Value

Compare

$$
\int_{-2}^{2}x\,dx
\quad \text{and} \quad
\int_{-2}^{2}|x|\,dx.
$$

Before calculating, predict the results from symmetry and a sketch, then carry out the calculation and explain the difference.

> **Why this problem:** it teaches how to use symmetry and geometry before applying a computational procedure.

## Solution

### 1. Predicted behavior from symmetry

The function $f(x)=x$ is odd, because

$$
f(-x)=-f(x).
$$

On a symmetric interval $[-2,2]$, the positive and negative parts cancel exactly. Therefore,

$$
\int_{-2}^{2}x\,dx = 0.
$$

On the other hand, $|x|$ is even, because

$$
|{-x}|=|x|.
$$

So the area on $[-2,0]$ and $[0,2]$ is the same, and the total should be positive.

### 2. Calculation of $\int_{-2}^{2}x\,dx$

$$
\int_{-2}^{2}x\,dx = \left[\frac{x^2}{2}\right]_{-2}^{2}
= \frac{4}{2} - \frac{4}{2}=0.
$$

So,

$$
\int_{-2}^{2}x\,dx = 0.
$$

### 3. Calculation of $\int_{-2}^{2}|x|\,dx$

Because $|x|=-x$ for $x<0$ and $|x|=x$ for $x\ge 0$,

$$
\int_{-2}^{2}|x|\,dx
= \int_{-2}^{0}(-x)\,dx + \int_0^2 x\,dx.
$$

Compute each part:

$$
\int_{-2}^{0}(-x)\,dx = \left[-\frac{x^2}{2}\right]_{-2}^{0} = 0 - \left(-\frac{4}{2}\right) = 2,
$$

$$
\int_0^2 x\,dx = \left[\frac{x^2}{2}\right]_0^2 = 2.
$$

Therefore,

$$
\int_{-2}^{2}|x|\,dx = 2+2 = 4.
$$

### 4. Why the results differ

- $\int_{-2}^{2}x\,dx = 0$ because the signed area above and below the $x$-axis cancels.
- $\int_{-2}^{2}|x|\,dx = 4$ because absolute value turns the negative part positive before integrating, so both halves contribute as area.

Geometrically, the graph of $y=x$ is symmetric about the origin and contributes equal positive and negative area, while the graph of $y=|x|$ is symmetric about the $y$-axis and contributes only positive area.
