# Problem 3. The Product Rule — Why Is It Needed?

For

$$
f(x)=(x^2+1)e^x
$$

compute the derivative. Then compare the correct result with the incorrect idea

$$
f'(x)\stackrel{?}{=}(2x)e^x
$$

and explain which term is missing.

> **Why this problem:** it teaches the product rule by analyzing a common mistake.

## Solution

### 1. Correct Computation of the Derivative

The function is a product of two factors:

$$
f(x) = u(x)v(x)
$$

where

$$
u(x) = x^2 + 1, \qquad v(x) = e^x
$$

Compute the derivative of each factor:

$$
u'(x) = 2x, \qquad v'(x) = e^x
$$

By the product rule:

$$
\frac{d}{dx}[u(x)v(x)] = u'(x)v(x) + u(x)v'(x)
$$

Substitute the functions and their derivatives:

$$
\begin{aligned}
f'(x) &= (2x)e^x + (x^2 + 1)e^x \\
&= (x^2 + 2x + 1)e^x \\
&= (x + 1)^2 e^x
\end{aligned}
$$

---

### 2. Comparison with the Incorrect Proposal

The proposed incorrect calculation is

$$
f'(x) \stackrel{?}{=} (2x)e^x
$$

In this proposal, the first factor $x^2 + 1$ was differentiated to $2x$, while the second factor $e^x$ was left untouched.
This reflects a false analogy with the constant-multiple rule, where a constant $c$ remains untouched: $\frac{d}{dx}[c \cdot u(x)] = c \cdot u'(x)$. Here, however, both factors depend on $x$, so both contribute to the rate of change of the product.

---

### 3. Which Term is Missing and Why

Comparing the correct result with the incorrect idea:

$$
f'_{\mathrm{correct}}(x) - f'_{\mathrm{incorrect}}(x) = \left[(2x)e^x + (x^2+1)e^x\right] - (2x)e^x = (x^2+1)e^x
$$

The missing term is

$$
u(x)v'(x) = (x^2 + 1)e^x
$$

#### Origin of the Product Rule
Consider a small increment $\Delta x$ in $x$. The factors change by $\Delta u$ and $\Delta v$:

$$
\Delta(uv) = (u + \Delta u)(v + \Delta v) - uv = (\Delta u)v + u(\Delta v) + (\Delta u)(\Delta v)
$$

Dividing by $\Delta x$ and taking the limit as $\Delta x \to 0$:

$$
\lim_{\Delta x\to0}\frac{\Delta(uv)}{\Delta x} = \left(\lim_{\Delta x\to0}\frac{\Delta u}{\Delta x}\right)v + u\left(\lim_{\Delta x\to0}\frac{\Delta v}{\Delta x}\right) + 0 = u'v + uv'
$$

The rate of change of the area of a rectangle of sides $u$ and $v$ consists of two distinct contributions:
1. $u'v$: the rate of change caused by stretching side $u$ while side $v$ remains fixed,
2. $uv'$: the rate of change caused by stretching side $v$ while side $u$ remains fixed.

The incorrect proposal $(2x)e^x$ completely neglects the second contribution, ignoring the substantial growth caused by the exponential factor $e^x$.

