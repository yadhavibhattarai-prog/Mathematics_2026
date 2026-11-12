## Question

Compute $\int(2e^x+3\cos x-4\sin x)\,dx$, match each term to a known derivative, and verify the result.

## Solution

We recognize the standard derivative rules:

- $\dfrac{d}{dx}(e^x)=e^x$
- $\dfrac{d}{dx}(\sin x)=\cos x$
- $\dfrac{d}{dx}(\cos x)=-\sin x$

Now integrate each term separately.

### 1. Integrate the exponential term

$$
\int 2e^x\,dx = 2\int e^x\,dx = 2e^x.
$$

### 2. Integrate the cosine term

$$
\int 3\cos x\,dx = 3\sin x,
$$

because $\dfrac{d}{dx}(\sin x)=\cos x$.

### 3. Integrate the sine term

$$
\int (-4\sin x)\,dx = 4\cos x,
$$

because $\dfrac{d}{dx}(\cos x)=-\sin x$.

The negative sign in the original integrand becomes positive in the antiderivative because the derivative of $\cos x$ is $-\sin x$.

Putting everything together,

$$
\int(2e^x+3\cos x-4\sin x)\,dx = 2e^x+3\sin x+4\cos x + C.
$$

### 4. Verify by differentiation

Differentiate the result:

$$
\frac{d}{dx}(2e^x+3\sin x+4\cos x+C).
$$

This gives

$$
2e^x + 3\cos x + 4(-\sin x) = 2e^x+3\cos x-4\sin x.
$$

That is exactly the original integrand, so the antiderivative is correct.
