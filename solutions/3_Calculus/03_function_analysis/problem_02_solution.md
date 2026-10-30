# Problem 2. A Parabola from the Perspective of the Derivative

For $f(x)=x^2-4x+1$, find the minimum using the derivative. Compare the result with the vertex form and explain why both approaches lead to the same point.

> **Why this problem:** it connects a new tool with the familiar geometry of a parabola.

## Solution

### 1. Finding the Minimum Using the Derivative

Compute the first derivative of $f(x) = x^2 - 4x + 1$:

$$
f'(x) = \frac{d}{dx}(x^2 - 4x + 1) = 2x - 4
$$

Find the critical point by setting $f'(x) = 0$:

$$
2x - 4 = 0 \implies 2x = 4 \implies x = 2
$$

Determine the nature of this critical point:
- For $x < 2$, $f'(x) = 2x - 4 < 0$, so the function is strictly decreasing.
- For $x > 2$, $f'(x) = 2x - 4 > 0$, so the function is strictly increasing.
- The second derivative is

$$
f''(x) = 2 > 0
$$

Because $f''(x) > 0$ everywhere, the function is strictly convex (concave up), and $x = 2$ is a strict global minimum.

Calculate the minimum value of the function:

$$
f(2) = 2^2 - 4(2) + 1 = 4 - 8 + 1 = -3
$$

The minimum point on the graph is $(2, -3)$.

---

### 2. Finding the Minimum Using the Vertex Form

Complete the square for the quadratic expression $x^2 - 4x + 1$:

$$
\begin{aligned}
f(x) &= (x^2 - 4x + 4) - 4 + 1 \\
&= (x - 2)^2 - 3
\end{aligned}
$$

The canonical vertex form of a parabola is

$$
y = a(x - x_v)^2 + y_v
$$

Comparing coefficients:

$$
a = 1, \qquad x_v = 2, \qquad y_v = -3
$$

Because the square of any real number is non-negative:

$$
(x - 2)^2 \ge 0 \quad (x \in \mathbb{R})
$$

the minimum value of $(x - 2)^2 - 3$ occurs precisely when $(x - 2)^2 = 0$, which yields $x = 2$.
The minimum value is $y_v = -3$, and the vertex coordinates are $(2, -3)$.

---

### 3. Comparison and Explanation of Equivalence

Both approaches produce the identical point $(2, -3)$.

#### Why the Two Approaches Must Agree
1. **Geometric Meaning of the Vertex:**
   A quadratic function $f(x) = ax^2 + bx + c$ with $a > 0$ represents an upward-opening parabola with an axis of symmetry along the vertical line $x = x_v = -b/(2a)$. The vertex is the unique turnaround point where the curve stops decreasing and starts increasing.
2. **Calculus Formulation:**
   At the turnaround point of a smooth curve, the instantaneous rate of change must be zero, meaning the tangent line is horizontal ($f'(x) = 0$). Differentiating the general quadratic gives

$$
f'(x) = 2ax + b = 0 \implies x = -\frac{b}{2a}
$$

3. **Algebraic Formulation:**
   Completing the square organizes the polynomial symmetrically around its axis of symmetry:

$$
ax^2 + bx + c = a\left(x + \frac{b}{2a}\right)^2 + \left(c - \frac{b^2}{4a}\right)
$$

Both methods identify the same geometric feature: the vertex is simultaneously the algebraic minimizer of the squared term and the calculus critical point where the tangent slope is zero.

