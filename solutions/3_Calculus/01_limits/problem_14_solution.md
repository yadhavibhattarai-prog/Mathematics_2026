# Exercise 14. A $0/0$ Limit with Trigonometry

Compute

$$
\lim_{x\to0}\frac{1-\cos x}{x^2}.
$$

Justify the result without using l'Hôpital's rule, using a trigonometric identity and the fundamental limit.

> **Why this exercise:** requires combining two known tools in one argument.

## Solution

### 1. Direct Evaluation

Substituting $x = 0$ yields

$$
\frac{1 - \cos 0}{0^2} = \frac{1 - 1}{0} = \frac{0}{0}
$$

which is an indeterminate form.

---

### 2. Method 1: Using the Half-Angle Identity

Recall the standard trigonometric identity for the half-angle sine:

$$
\sin^2\left(\frac{x}{2}\right) = \frac{1 - \cos x}{2}
$$

Multiplying both sides by $2$ gives

$$
1 - \cos x = 2\sin^2\left(\frac{x}{2}\right)
$$

Substitute this identity into the original limit:

$$
\frac{1-\cos x}{x^2} = \frac{2\sin^2\left(\frac{x}{2}\right)}{x^2}
$$

To utilize the fundamental trigonometric limit $\lim_{u\to0}\frac{\sin u}{u} = 1$, the argument inside the sine is $u = \frac{x}{2}$. Group the terms so that $\left(\frac{x}{2}\right)^2$ appears in the denominator:

$$
x^2 = 4 \cdot \left(\frac{x}{2}\right)^2
$$

Substitute this into the fraction:

$$
\frac{2\sin^2\left(\frac{x}{2}\right)}{4\cdot \left(\frac{x}{2}\right)^2} = \frac{2}{4} \cdot \left(\frac{\sin(x/2)}{x/2}\right)^2 = \frac{1}{2} \cdot \left(\frac{\sin(x/2)}{x/2}\right)^2
$$

As $x \to 0$, $u = \frac{x}{2} \to 0$. By the fundamental trigonometric limit:

$$
\lim_{x\to0}\frac{\sin(x/2)}{x/2} = 1
$$

By continuity of the squaring function:

$$
\lim_{x\to0}\left(\frac{\sin(x/2)}{x/2}\right)^2 = 1^2 = 1
$$

Therefore:

$$
\lim_{x\to0}\frac{1-\cos x}{x^2} = \frac{1}{2} \cdot 1 = \frac{1}{2}
$$

---

### 3. Method 2: Using the Trigonometric Conjugate

Multiply both the numerator and the denominator by the conjugate expression $1 + \cos x$:

$$
\begin{aligned}
\frac{1-\cos x}{x^2} &= \frac{(1-\cos x)(1+\cos x)}{x^2(1+\cos x)} \\
&= \frac{1 - \cos^2 x}{x^2(1+\cos x)}
\end{aligned}
$$

Using the Pythagorean trigonometric identity $1 - \cos^2 x = \sin^2 x$:

$$
\frac{1 - \cos^2 x}{x^2(1+\cos x)} = \frac{\sin^2 x}{x^2(1+\cos x)} = \left(\frac{\sin x}{x}\right)^2 \cdot \frac{1}{1+\cos x}
$$

Now compute the limits of the two separate factors as $x \to 0$:
- By the fundamental trigonometric limit:

$$
\lim_{x\to0}\left(\frac{\sin x}{x}\right)^2 = 1^2 = 1
$$

- By continuity of $\cos x$ at $x = 0$:

$$
\lim_{x\to0}\frac{1}{1+\cos x} = \frac{1}{1 + \cos 0} = \frac{1}{1 + 1} = \frac{1}{2}
$$

Applying the product rule for limits:

$$
\lim_{x\to0}\frac{1-\cos x}{x^2} = 1 \cdot \frac{1}{2} = \frac{1}{2}
$$

Both methods rigorously establish the limit without resorting to differential calculus or l'Hôpital's rule.

