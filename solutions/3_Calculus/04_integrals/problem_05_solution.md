## Question

Compute $\int xe^{x^2}\,dx$ and compare its structure with Problem 4, explaining the common substitution mechanism.

## Solution

The key observation is that the integrand has the form

$$
\text{(outer function of inner expression)} \times \text{(derivative of inner expression)}.
$$

Here the inner expression is

$$u=x^2.
$$

Its derivative is

$$du = 2x\,dx.
$$

This is exactly the pattern we use for substitution.

### 1. Make the substitution

Let

$$u=x^2.
$$

Then

$$du = 2x\,dx,
$$

so

$$x\,dx = \frac{1}{2}du.
$$

Substitute into the integral:

$$
\int xe^{x^2}\,dx = \int e^{x^2}(x\,dx)
= \int e^u \cdot \frac{1}{2}du.
$$

Factor out the constant $\frac12$:

$$
= \frac{1}{2}\int e^u\,du.
$$

### 2. Integrate with respect to $u$

Since $\int e^u du = e^u + C$, we get

$$
\frac{1}{2}\int e^u du = \frac{1}{2}e^u + C.
$$

Now replace $u$ with $x^2$:

$$
\int xe^{x^2}\,dx = \frac{1}{2}e^{x^2} + C.
$$

### 3. Check by differentiation

Differentiate the answer:

$$
\frac{d}{dx}\left(\frac{1}{2}e^{x^2}+C\right).
$$

Using the chain rule,

$$
= \frac{1}{2}e^{x^2}\cdot (2x) = xe^{x^2}.
$$

This matches the original integrand exactly, so the result is correct.

### 4. Why this works

The structure is the same as in Problem 4: an outer function such as $e^u$ is being evaluated at an inner function $u=x^2$, and the remaining factor $x\,dx$ is a constant multiple of $du$. This is the standard substitution pattern: rewrite the integral so that it depends on $u$ and $du$, then integrate in the new variable.
