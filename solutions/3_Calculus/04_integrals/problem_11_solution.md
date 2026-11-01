## Question

### Problem 11. Choose the Method First

For each integral, first write which method you choose and how you recognize it, and then compute:

1. $\int\sin(3x)\,dx$
2. $\int x\ln x\,dx$
3. $\int\frac{x}{\sqrt{x^2+1}}\,dx$

> **Why this problem:** it tests the choice of method based on the structure of the problem.

## Solution

### 1. $\int \sin(3x)\,dx$

This is a substitution problem because the inner expression is $3x$, and its derivative is a constant $3$.

Let

$$
u = 3x, \qquad du = 3\,dx.
$$

Then

$$
\int \sin(3x)\,dx = \frac13 \int \sin u\,du.
$$

Since

$$
\int \sin u\,du = -\cos u + C,
$$

we get

$$
\int \sin(3x)\,dx = -\frac13\cos(3x) + C.
$$

---

### 2. $\int x\ln x\,dx$

This is an integration-by-parts problem because the integrand is a product of a polynomial and a logarithm.

Choose

$$
u = \ln x, \qquad dv = x\,dx.
$$

Then

$$
du = \frac{1}{x}\,dx, \qquad v = \frac{x^2}{2}.
$$

Apply integration by parts:

$$
\int x\ln x\,dx = \frac{x^2}{2}\ln x - \int \frac{x^2}{2}\cdot \frac{1}{x}\,dx.
$$

Simplify the remaining integral:

$$
= \frac{x^2}{2}\ln x - \frac12 \int x\,dx.
$$

Since

$$
\int x\,dx = \frac{x^2}{2}+C,
$$

we obtain

$$
\int x\ln x\,dx = \frac{x^2}{2}\ln x - \frac{x^2}{4} + C.
$$

---

### 3. $\int \frac{x}{\sqrt{x^2+1}}\,dx$

This is a substitution problem because the derivative of the denominator is

$$
\frac{d}{dx}(x^2+1)=2x,
$$

and the numerator is $x$, which matches after a constant factor.

Let

$$
u = x^2+1, \qquad du = 2x\,dx.
$$

Then

$$
\int \frac{x}{\sqrt{x^2+1}}\,dx = \frac12 \int u^{-1/2}\,du.
$$

Now

$$
\int u^{-1/2}\,du = 2u^{1/2}+C,
$$

so

$$
\frac12 \int u^{-1/2}\,du = \frac12(2u^{1/2})+C = u^{1/2}+C.
$$

Returning to $x$,

$$
\int \frac{x}{\sqrt{x^2+1}}\,dx = \sqrt{x^2+1}+C.
$$

### Final answers

$$
\int\sin(3x)\,dx = -\frac13\cos(3x)+C,
$$

$$
\int x\ln x\,dx = \frac{x^2}{2}\ln x - \frac{x^2}{4}+C,
$$

$$
\int\frac{x}{\sqrt{x^2+1}}\,dx = \sqrt{x^2+1}+C.
$$
