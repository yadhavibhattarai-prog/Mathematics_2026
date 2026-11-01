## Question

### Problem 8. Choosing the Factors in Integration by Parts

Compute

$$
\int x\cos x\,dx.
$$

Before calculating, justify why it is convenient to differentiate $x$ and integrate $\cos x$, rather than the other way around.

> **Why this problem:** it teaches that integration by parts requires a deliberate choice of factors.

## Solution

We want to use integration by parts:

$$
\int u\,dv = uv - \int v\,du.
$$

For the integrand $x\cos x$, we choose

$$
u = x, \qquad dv = \cos x\,dx.
$$

Then

$$
du = dx, \qquad v = \sin x.
$$

This choice is convenient because differentiating $x$ gives $1$, which simplifies the expression, while integrating $\cos x$ gives $\sin x$, which is easy to manage. If we reversed the choice, we would get a more complicated integral.

Now apply the formula:

$$
\int x\cos x\,dx = x\sin x - \int \sin x\,dx.
$$

Since

$$
\int \sin x\,dx = -\cos x + C,
$$

we get

$$
\int x\cos x\,dx = x\sin x - (-\cos x) + C = x\sin x + \cos x + C.
$$

### Verification by differentiation

Differentiate the answer:

$$
\frac{d}{dx}(x\sin x + \cos x + C)
= \sin x + x\cos x - \sin x
= x\cos x.
$$

This matches the original integrand exactly, so the antiderivative is correct.
