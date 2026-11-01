## Question

Compute

$$
\int 2x(x^2+1)^4\,dx.
$$

Before calculating, identify a suitable substitution $u$, show that its derivative appears in the integrand, and verify the result by differentiation.

## Solution

The key observation is that the expression inside the power is $x^2+1$, and its derivative is

$$
\frac{d}{dx}(x^2+1)=2x.
$$

This matches the factor $2x$ that is already present in the integrand, so the substitution is a standard chain-rule reversal.

Let

$$
u = x^2+1.
$$

Then

$$
du = 2x\,dx.
$$

Substituting into the integral gives

$$
\int 2x(x^2+1)^4\,dx = \int u^4\,du.
$$

Now apply the power rule for antiderivatives:

$$
\int u^4\,du = \frac{u^5}{5}+C.
$$

Returning to $x$,

$$
\int 2x(x^2+1)^4\,dx = \frac{(x^2+1)^5}{5}+C.
$$

### Verification by differentiation

Differentiate the answer:

$$
\frac{d}{dx}\left(\frac{(x^2+1)^5}{5}+C\right)
= \frac{1}{5}\cdot 5(x^2+1)^4\cdot 2x.
$$

Simplifying,

$$
= 2x(x^2+1)^4.
$$

This is exactly the original integrand, so the antiderivative is correct.

The substitution method works because the derivative of the inner expression appears as a factor in the integral, allowing the integrand to be rewritten in terms of a single variable $u$.
