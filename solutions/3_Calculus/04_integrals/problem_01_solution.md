## Question

### Problem 1. Antiderivative and Verification

For

$$
f(x)=3x^2-4x+5
$$

find one antiderivative $F(x)$. Write the entire family of antiderivatives, verify the result by differentiation, and explain the meaning of the constant $C$.

> **Why this problem:** it introduces integration as the inverse operation to differentiation.

## Solution

### 1. Finding One Antiderivative $F(x)$

An antiderivative of a function $f(x)$ is any differentiable function $F(x)$ satisfying

$$
F'(x) = f(x)
$$

on its domain.

Using the power rule for integration $\int x^n\,dx = \frac{x^{n+1}}{n+1} + C$ and the sum and constant multiple rules:
- For $3x^2$:

$$
\int 3x^2\,dx = 3\left(\frac{x^3}{3}\right) = x^3
$$

- For $-4x$:

$$
\int (-4x)\,dx = -4\left(\frac{x^2}{2}\right) = -2x^2
$$

- For the constant $5$:

$$
\int 5\,dx = 5x
$$

Choosing the simplest constant $C = 0$, one particular antiderivative is

$$
F(x) = x^3 - 2x^2 + 5x
$$

---

### 2. The Entire Family of Antiderivatives

Because the derivative of any constant is zero, adding any real constant $C$ to an antiderivative produces another valid antiderivative.

The entire family of antiderivatives (the indefinite integral) is given by

$$
F(x) = x^3 - 2x^2 + 5x + C, \qquad C \in \mathbb{R}
$$

---

### 3. Verification by Differentiation

To verify the result, compute the derivative of $F(x)$ with respect to $x$:

$$
\begin{aligned}
F'(x) &= \frac{d}{dx}\left(x^3 - 2x^2 + 5x + C\right) \\
&= \frac{d}{dx}(x^3) - \frac{d}{dx}(2x^2) + \frac{d}{dx}(5x) + \frac{d}{dx}(C) \\
&= 3x^2 - 2(2x) + 5(1) + 0 \\
&= 3x^2 - 4x + 5 \\
&= f(x)
\end{aligned}
$$

Differentiation recovers the original integrand $f(x)$ identically, confirming that the family of antiderivatives is correct.

---

### 4. Meaning of the Constant of Integration $C$

1. **Algebraic Meaning:**
   Differentiation is an operation that annihilates constants:

$$
\frac{d}{dx}(C) = 0
$$

   Consequently, if $F'(x) = f(x)$, then $(F(x) + C)' = F'(x) + 0 = f(x)$ for every real number $C$. The reverse operation (indefinite integration) cannot recover an individual constant from the derivative alone without additional boundary or initial information.

2. **Uniqueness up to a Constant (Mean Value Theorem):**
   By the corollary to the Mean Value Theorem, if two functions $F_1(x)$ and $F_2(x)$ have the same derivative on a connected interval, their difference has derivative zero everywhere:

$$
(F_1 - F_2)'(x) = f(x) - f(x) = 0 \implies F_1(x) - F_2(x) = C
$$

   This guarantees that any two antiderivatives differ only by an additive constant, meaning $F(x) + C$ exhausts all possible antiderivatives.

3. **Geometric Meaning:**
   The parameter $C$ shifts the graph $y = F(x)$ vertically up or down without changing its shape. Because vertical translation preserves tangent slopes at every $x$-coordinate, every member of the family has the exact same slope $f(x)$ at any given $x$.
