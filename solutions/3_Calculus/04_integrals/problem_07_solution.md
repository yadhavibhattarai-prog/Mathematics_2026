## Question

### Problem 7. Integration by Parts as Reversing the Product Rule

Compute

$$
\int x e^x\,dx.
$$

First write the product differentiation rule and, on that basis, explain the meaning of the integration-by-parts formula. Verify the result by differentiation.

> **Why this problem:** it connects a new technique with the familiar product rule.

## Solution

### 1. Start from the product rule

If $u(x)$ and $v(x)$ are differentiable functions, then

$$
\frac{d}{dx}(uv) = u'v + uv'.
$$

Rearrange this as

$$
uv' = \frac{d}{dx}(uv) - u'v.
$$

Now integrate both sides:

$$
\int uv'\,dx = uv - \int u'v\,dx.
$$

This is the integration-by-parts formula:

$$
\int u\,dv = uv - \int v\,du.
$$

This is really the product rule in reverse. It is useful when the integrand is a product of two functions, and one part becomes simpler after differentiation while the other is easy to integrate.

### 2. Apply it to $\int x e^x\,dx$

Choose

$$
u = x, \qquad dv = e^x\,dx.
$$

Then

$$
du = dx, \qquad v = e^x.
$$

Substitute into the integration-by-parts formula:

$$
\int x e^x\,dx = x e^x - \int e^x\,dx.
$$

Now integrate $e^x$:

$$
\int e^x\,dx = e^x + C.
$$

So

$$
\int x e^x\,dx = x e^x - e^x + C.
$$

Factor the common $e^x$:

$$
= e^x(x-1)+C.
$$

### 3. Verify by differentiation

Differentiate the answer:

$$
\frac{d}{dx}\left(e^x(x-1)+C\right).
$$

Using the product rule,

$$
= e^x(x-1) + e^x.
$$

Factor out $e^x$:

$$
= e^x\bigl((x-1)+1\bigr)=xe^x.
$$

This matches the original integrand exactly, so the result is correct.

Therefore,

$$
\boxed{\int x e^x\,dx = e^x(x-1)+C.}
$$
