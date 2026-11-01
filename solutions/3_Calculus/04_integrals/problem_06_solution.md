## Question

### Problem 6. When Does a Logarithm Appear from an Integral?

Compute

$$
\int \frac{2x}{x^2+5}\,dx.
$$

Identify the denominator as a candidate for substitution, compare the numerator with its derivative, and explain the source of the logarithm in the result.

> **Why this problem:** it teaches how to recognize the structure “derivative of the denominator over the denominator.”

## Solution

The denominator is

$$
 x^2+5,
$$

and its derivative is

$$
\frac{d}{dx}(x^2+5)=2x.
$$

The numerator is exactly $2x$, so the integrand has the form

$$
\frac{g'(x)}{g(x)},
$$

where $g(x)=x^2+5$.

This is the standard pattern for a logarithm. Let

$$
u = x^2+5.
$$

Then

$$
du=2x\,dx,
$$

and the integral becomes

$$
\int \frac{2x}{x^2+5}\,dx = \int \frac{1}{u}\,du.
$$

Now recall that

$$
\int \frac{1}{u}\,du = \ln|u| + C.
$$

Therefore,

$$
\int \frac{2x}{x^2+5}\,dx = \ln|x^2+5| + C.
$$

### Why the logarithm appears

The logarithm arises because the antiderivative of $1/u$ is $\\ln|u|$. In this problem, the quotient is not arbitrary; it is the derivative of the denominator divided by the denominator itself. That is exactly the pattern that produces a logarithm.

### Verification

Differentiate the answer:

$$
\frac{d}{dx}\left(\ln|x^2+5| + C\right)
= \frac{1}{x^2+5}\cdot 2x
= \frac{2x}{x^2+5}.
$$

This matches the original integrand, so the result is correct.
