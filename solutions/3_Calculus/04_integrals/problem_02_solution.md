## Question

Compute $\int(2\sqrt{x}+3/x^2-x^{1/3})\,dx$, first rewriting powers and determining the original domain, then verify by differentiation.

## Solution

First rewrite each term using exponents so the power rule can be applied directly:

$$
2\sqrt{x} = 2x^{1/2}, \qquad \frac{3}{x^2}=3x^{-2}, \qquad x^{1/3}=x^{1/3}.
$$

So the integral becomes

$$
\int \left(2x^{1/2}+3x^{-2}-x^{1/3}\right)dx.
$$

### 1. Determine the domain

The original expression contains:
- $\sqrt{x}$, which requires $x \ge 0$
- $\frac{3}{x^2}$, which requires $x \ne 0$

The intersection of these conditions is

$$x>0.
$$

So the original integrand is defined on $x>0$.

### 2. Integrate term by term

Apply the power rule $\int x^n dx = \frac{x^{n+1}}{n+1}+C$ for each term:

$$
\int 2x^{1/2}dx = 2\cdot \frac{x^{3/2}}{3/2} = \frac{4}{3}x^{3/2},
$$

$$
\int 3x^{-2}dx = 3\cdot \frac{x^{-1}}{-1} = -\frac{3}{x},
$$

$$
\int -x^{1/3}dx = -\frac{x^{4/3}}{4/3} = -\frac{3}{4}x^{4/3}.
$$

Therefore,

$$
\int \left(2\sqrt{x}+\frac{3}{x^2}-x^{1/3}\right)dx
= \frac{4}{3}x^{3/2}-\frac{3}{x}-\frac{3}{4}x^{4/3}+C.
$$

### 3. Verify by differentiation

Differentiate the result:

$$
\frac{d}{dx}\left(\frac{4}{3}x^{3/2}-\frac{3}{x}-\frac{3}{4}x^{4/3}+C\right).
$$

Using the derivative rules,

$$
\frac{d}{dx}\left(\frac{4}{3}x^{3/2}\right)=2x^{1/2},
$$

$$
\frac{d}{dx}\left(-\frac{3}{x}\right)=\frac{3}{x^2}=3x^{-2},
$$

$$
\frac{d}{dx}\left(-\frac{3}{4}x^{4/3}\right)=-x^{1/3}.
$$

Adding them gives

$$
2x^{1/2}+3x^{-2}-x^{1/3}
=2\sqrt{x}+\frac{3}{x^2}-x^{1/3},
$$

which matches the original integrand for $x>0$.

So the antiderivative is correct.
