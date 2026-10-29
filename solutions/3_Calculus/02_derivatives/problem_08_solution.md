# Problem 8. Two Exponential Functions

For

$$
f(x)=e^{2x-3}+5^x
$$

compute the derivative. Explain why the factor $2$ appears in the first term and why $\ln5$ appears in the second.

> **Why this problem:** it organizes two different mechanisms that produce additional factors.

## Solution

### 1. Computation of the Derivative

The function is a sum of two exponential expressions:

$$
f(x) = e^{2x-3} + 5^x
$$

Apply the sum rule:

$$
f'(x) = \frac{d}{dx}\left(e^{2x-3}\right) + \frac{d}{dx}\left(5^x\right)
$$

- **Differentiating the first term:**
  The exponent is a linear function $u(x) = 2x - 3$. By the chain rule:

$$
\frac{d}{dx}\left(e^{2x-3}\right) = e^{2x-3} \cdot \frac{d}{dx}(2x - 3) = e^{2x-3} \cdot 2 = 2e^{2x-3}
$$

- **Differentiating the second term:**
  The base is $5 \neq e$. Using the standard derivative of a general exponential function $\frac{d}{dx}(a^x) = a^x \ln a$:

$$
\frac{d}{dx}\left(5^x\right) = 5^x \ln 5
$$

Combine the two derivatives:

$$
f'(x) = 2e^{2x-3} + 5^x \ln 5
$$

---

### 2. Why the Factor $2$ Appears in the First Term

The factor $2$ arises from the **chain rule applied to a composite exponent**.

The function $e^{2x-3}$ is composed of:
- an outer natural exponential $g(u) = e^u$, whose derivative is $g'(u) = e^u$,
- an inner linear function $u(x) = 2x - 3$, whose derivative is $u'(x) = 2$.

By the chain rule:

$$
\frac{d}{dx}\left(e^{u(x)}\right) = e^{u(x)} \cdot u'(x)
$$

Because the rate of growth of the exponent $2x - 3$ with respect to $x$ is $2$, any small step $\Delta x$ doubles the change in the exponent, multiplying the natural exponential rate of change by $2$.

---

### 3. Why the Factor $\ln 5$ Appears in the Second Term

The factor $\ln 5$ arises from **converting an exponential with non-natural base to base $e$**.

By definition of the natural logarithm, any positive base $a > 0$ can be written as an power of $e$:

$$
5 = e^{\ln 5}
$$

Using the power of a power property, rewrite $5^x$ with base $e$:

$$
5^x = \left(e^{\ln 5}\right)^x = e^{(\ln 5)x}
$$

Now differentiate $e^{(\ln 5)x}$ using the chain rule with inner function $v(x) = (\ln 5)x$. Since $\ln 5$ is a constant:

$$
v'(x) = \frac{d}{dx}\left((\ln 5)x\right) = \ln 5
$$

Applying the chain rule gives:

$$
\frac{d}{dx}\left(5^x\right) = \frac{d}{dx}\left(e^{(\ln 5)x}\right) = e^{(\ln 5)x} \cdot \ln 5 = 5^x \ln 5
$$

The factor $\ln 5 \approx 1.6094$ represents the natural scaling constant needed because base $5$ grows faster than base $e \approx 2.7183$.

