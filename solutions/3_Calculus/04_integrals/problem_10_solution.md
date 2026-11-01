## Question

### Problem 10. Definite Integral and Checking the Result

Before carrying out the exact calculation, estimate the possible range of values of the integral

$$
\int_0^2 (x^2+1)\,dx,
$$

using

$$
1\le x^2+1\le 5
$$

on $[0,2]$. Only then compute the integral exactly, compare the result with the earlier estimate, and explain what type of computational error such a check can detect.

> **Why this problem:** it teaches how to predict the possible range of a result and check the calculation.

## Solution

### 1. Estimating the integral

On the interval $[0,2]$, we have

$$
1 \le x^2+1 \le 5.
$$

Since the length of the interval is

$$
2-0=2,
$$

integrating the inequality gives

$$
\int_0^2 1\,dx \le \int_0^2 (x^2+1)\,dx \le \int_0^2 5\,dx.
$$

That is,

$$
2 \le \int_0^2 (x^2+1)\,dx \le 10.
$$

So the value of the integral must lie between $2$ and $10$.

### 2. Exact computation

Compute the antiderivative:

$$
\int (x^2+1)\,dx = \frac{x^3}{3} + x + C.
$$

Therefore,

$$
\int_0^2 (x^2+1)\,dx
= \left[\frac{x^3}{3} + x\right]_0^2
= \left(\frac{8}{3} + 2\right) - (0+0)
= \frac{8}{3} + \frac{6}{3}
= \frac{14}{3}.
$$

So

$$
\int_0^2 (x^2+1)\,dx = \frac{14}{3} \approx 4.67.
$$

This value lies inside the estimated interval

$$
2 \le \frac{14}{3} \le 10,
$$

as expected.

### 3. Why this estimate is useful

This kind of estimate is a quick validity check. If a later computation produced, for example, a number much larger than $10$ or much smaller than $2$, then there would be a likely mistake in the integration or in the evaluation of the antiderivative.

It can detect many common errors such as:

- forgetting a coefficient,
- using the wrong power rule,
- mis-evaluating the endpoint values,
- sign mistakes in the final result.

The estimate does not replace the exact calculation, but it reveals whether the answer is plausible.
