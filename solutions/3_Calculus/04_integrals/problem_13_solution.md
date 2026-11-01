## Question

### Problem 13. An Integral Depending on the Upper Limit

Let

$$
F(x)=\int_0^x (t^2+1)\,dt.
$$

Determine $F(x)$, compute $F'(x)$, and compare the result with the integrand. Explain in your own words why the height of the function describes the local rate of increase of the accumulated area.

> **Why this problem:** it connects differentiation and integration through the idea of accumulation.

## Solution

### 1. Compute $F(x)$

We integrate the function $t^2+1$ with respect to $t$:

$$
\int (t^2+1)\,dt = \frac{t^3}{3}+t.
$$

So,

$$
F(x)=\left[\frac{t^3}{3}+t\right]_{0}^{x}
= \frac{x^3}{3}+x.
$$

### 2. Differentiate $F(x)$

$$
F'(x)=\frac{d}{dx}\left(\frac{x^3}{3}+x\right)
= x^2+1.
$$

This is exactly the integrand we started with.

### 3. Interpretation

The Fundamental Theorem of Calculus says:

$$
F'(x)=f(x),
$$

when

$$
F(x)=\int_a^x f(t)\,dt.
$$

So the derivative of the accumulated area equals the height of the original function at the upper limit.

### 4. Why the height describes the local rate of increase

Think of $F(x)$ as the accumulated area under the curve $y=f(t)$ from $0$ to $x$. As $x$ increases slightly by $\Delta x$, the additional area is approximately a thin rectangle of width $\Delta x$ and height $f(x)$. Therefore,

$$
\Delta F \approx f(x)\Delta x,
$$

so

$$
\frac{\Delta F}{\Delta x} \approx f(x).
$$

In the limit, this becomes

$$
F'(x)=f(x).
$$

This is why the value of the function at a point tells us how quickly the accumulated area is changing there: the higher the graph, the faster the area under it increases locally.
