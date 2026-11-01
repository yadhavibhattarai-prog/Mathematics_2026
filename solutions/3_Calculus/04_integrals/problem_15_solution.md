## Question

### Problem 15. Recovering a Function from Its Derivative and a Condition

The function $F$ satisfies

$$
F'(x)=2xe^{x^2}
$$

and

$$
F(0)=3.
$$

1. Recognize the method needed to find the function $F$.
2. Determine the entire family of functions with the given derivative.
3. Use the condition $F(0)=3$ to determine the correct constant.
4. Verify the final result by differentiation and substitution of $x=0$.

> **Why this problem:** it combines recognition of substitution, the meaning of the constant of integration, and an initial condition in one problem, using only mechanisms introduced earlier.

## Solution

### 1. Recognize the method

The derivative is

$$
F'(x)=2xe^{x^2}.
$$

Notice that the derivative of the exponent $x^2$ is $2x$, so a substitution is natural.

Let

$$
u = x^2, \qquad du = 2x\,dx.
$$

This is the standard pattern of reversing the chain rule.

### 2. Find the family of antiderivatives

Then

$$
F(x)=\int 2xe^{x^2}\,dx = \int e^u\,du.
$$

Since

$$
\int e^u\,du = e^u + C,
$$

we get

$$
F(x)=e^{x^2}+C.
$$

So the entire family of functions with derivative $2xe^{x^2}$ is

$$
F(x)=e^{x^2}+C.
$$

### 3. Use the initial condition

We are told that

$$
F(0)=3.
$$

Substitute $x=0$:

$$
F(0)=e^{0^2}+C=1+C=3.
$$

Hence,

$$
C=2.
$$

Therefore,

$$
F(x)=e^{x^2}+2.
$$

### 4. Verification

Differentiate:

$$
F'(x)=\frac{d}{dx}(e^{x^2}+2)=e^{x^2}(2x)=2xe^{x^2}.
$$

This matches the required derivative.

Now check the condition at $x=0$:

$$
F(0)=e^0+2=1+2=3.
$$

Everything agrees, so the function is correct.

Final answer:

$$
\boxed{F(x)=e^{x^2}+2.}
$$
