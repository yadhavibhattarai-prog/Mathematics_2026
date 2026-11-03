## Question

### Problem 7. Integration by Parts as Reversing the Product Rule

Compute

$$
\int x e^x\,dx.
$$

First write the product differentiation rule and, on that basis, explain the meaning of the integration-by-parts formula. Verify the result by differentiation.

> **Why this problem:** it connects a new technique with the familiar product rule.

## Solution

Let \(u\) and \(v\) be differentiable functions of \(x\). By the definition
of the derivative,

$$
(uv)'(x)
= \lim_{h\to 0}\frac{u(x+h)v(x+h)-u(x)v(x)}{h}.
$$

Add and subtract \(u(x+h)v(x)\) in the numerator and factor:

$$
\begin{aligned}
(uv)'(x)
&= \lim_{h\to 0}\left(
u(x+h)\frac{v(x+h)-v(x)}{h}
+ v(x)\frac{u(x+h)-u(x)}{h}
\right) \\
&= u(x)v'(x)+u'(x)v(x).
\end{aligned}
$$

Thus, \((uv)'=u'v+uv'\).

Rearranging,

$$
uv' = (uv)' - u'v.
$$

Integrating both sides gives the integration-by-parts formula:

$$
\int u\,dv = uv - \int v\,du.
$$

This is the reverse of the product rule, used when the integrand is a product of two functions where one part becomes simpler after differentiation and the other is easy to integrate.

For

$$
\int x e^x\,dx,
$$

choose

$$
u = x, \quad dv = e^x\,dx.
$$

Then

$$
du = dx, \quad v = e^x.
$$

Apply integration by parts:

$$
\int x e^x\,dx = x e^x - \int e^x\,dx.
$$

Since

$$
\int e^x\,dx = e^x + C,
$$

we obtain

$$
\int x e^x\,dx = x e^x - e^x + C = e^x(x-1) + C.
$$

### Verification by differentiation

Differentiate the answer:

$$
\frac{d}{dx}\left(e^x(x-1)+C\right)
= e^x(x-1) + e^x
= x e^x.
$$

This matches the original integrand, so the result is correct.
