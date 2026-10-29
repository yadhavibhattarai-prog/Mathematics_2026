# Exercise 3. A Square Root and Removing an Indeterminate Form

Compute

$$
\lim_{n\to\infty}\left(\sqrt{n^2+5n}-n\right).
$$

Use the conjugate expression and explain why this transformation removes the difficulty.

> **Why this exercise:** introduces conjugation as a deliberate technique for removing an indeterminate form.

## Solution

### 1. Calculation Using the Conjugate Expression

Direct substitution yields an indeterminate form of the type $\infty - \infty$:

$$
\lim_{n\to\infty}\sqrt{n^2+5n} = \infty, \qquad \lim_{n\to\infty} n = \infty
$$

To resolve this indeterminate form, multiply and divide the expression by its algebraic conjugate, $\sqrt{n^2+5n} + n$:

$$
\begin{aligned}
\sqrt{n^2+5n} - n &= \frac{\left(\sqrt{n^2+5n} - n\right)\left(\sqrt{n^2+5n} + n\right)}{\sqrt{n^2+5n} + n} \\
&= \frac{\left(\sqrt{n^2+5n}\right)^2 - n^2}{\sqrt{n^2+5n} + n} \\
&= \frac{(n^2 + 5n) - n^2}{\sqrt{n^2+5n} + n} \\
&= \frac{5n}{\sqrt{n^2+5n} + n}
\end{aligned}
$$

For $n > 0$, factor out $n$ from the radical in the denominator:

$$
\sqrt{n^2+5n} = \sqrt{n^2\left(1 + \frac{5}{n}\right)} = n\sqrt{1 + \frac{5}{n}}
$$

Substitute this back into the denominator:

$$
\frac{5n}{n\sqrt{1 + \frac{5}{n}} + n} = \frac{5n}{n\left(\sqrt{1 + \frac{5}{n}} + 1\right)} = \frac{5}{\sqrt{1 + \frac{5}{n}} + 1}
$$

Now take the limit as $n \to \infty$. Since $\lim_{n\to\infty} \frac{5}{n} = 0$:

$$
\lim_{n\to\infty}\left(\sqrt{n^2+5n}-n\right) = \lim_{n\to\infty}\frac{5}{\sqrt{1 + \frac{5}{n}} + 1} = \frac{5}{\sqrt{1 + 0} + 1} = \frac{5}{2}
$$

---

### 2. Why Conjugation Removes the Difficulty

1. **Elimination of the Radical via Difference of Squares:**
   The algebraic identity

$$
(A - B)(A + B) = A^2 - B^2
$$

   squares each term individually. Applying this to $A = \sqrt{n^2+5n}$ and $B = n$ cancels the dominant quadratic term $n^2$:

$$
A^2 - B^2 = (n^2 + 5n) - n^2 = 5n
$$

2. **Conversion of Indeterminate Form:**
   In the original expression $\sqrt{n^2+5n} - n$, two large numbers of order $n$ are subtracted from each other (catastrophic cancellation), which is an indeterminate form $\infty - \infty$.
   Conjugation moves the addition operation into the denominator:

$$
\sqrt{n^2+5n} + n \sim n + n = 2n
$$

   This transforms the indeterminate difference $\infty - \infty$ into an indeterminate quotient of the form $\frac{\infty}{\infty}$, where both numerator ($5n$) and denominator ($2n$) have a clearly identifiable, dominant linear growth rate.
3. **Cancellation of the Common Scale Factor:**
   Dividing numerator and denominator by $n$ produces terms of the form $5/n \to 0$ and leaves the finite constant ratio $\frac{5}{1+1} = \frac{5}{2}$.

