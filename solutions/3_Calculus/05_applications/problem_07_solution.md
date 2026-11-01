## Question

### Problem 7. Exponential Growth

Assume the model

$$
N(t)=N_0e^{kt},\qquad k>0.
$$

1. Verify by differentiation that the model satisfies the relation $N'(t)=kN(t)$.
2. Find the population doubling time.
3. Explain why the doubling time does not depend on $N_0$.

## Solution

### 1. Differentiate the model

$$
N(t)=N_0e^{kt}.
$$

Differentiate with respect to $t$:

$$
N'(t)=N_0\cdot k e^{kt}=kN_0e^{kt}=kN(t).
$$

So the model satisfies

$$
\boxed{N'(t)=kN(t)}.
$$

This means the growth rate is proportional to the current population.

### 2. Doubling time

A population doubles when

$$
N(t)=2N_0.
$$

So

$$
N_0e^{kt}=2N_0.
$$

Cancel $N_0$:

$$
e^{kt}=2.
$$

Take natural logarithms:

$$
kt=\ln 2,
$$

hence

$$
\boxed{t=\frac{\ln 2}{k}}.
$$

This is the doubling time.

### 3. Why the doubling time does not depend on $N_0$

The equation for doubling is

$$
\frac{N(t)}{N_0}=e^{kt}=2,
$$

so the initial value $N_0$ cancels out. The doubling time depends only on the growth rate $k$.

Therefore, for exponential growth with fixed $k$, the time to double is the same regardless of the starting amount.
