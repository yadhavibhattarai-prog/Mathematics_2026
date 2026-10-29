# Exercise 8. A Square Root in a Function Limit

Compute

$$
\lim_{x\to4}\frac{\sqrt{x}-2}{x-4}
$$

by rationalizing the numerator. Compare the idea with Exercise 3 involving a sequence.

> **Why this exercise:** reinforces transferring the same algebraic technique between two types of limits.

## Solution

### 1. Calculation by Rationalizing the Numerator

Direct substitution of $x = 4$ yields

$$
\frac{\sqrt{4}-2}{4-4} = \frac{2-2}{0} = \frac{0}{0}
$$

which is an indeterminate form.

To rationalize the numerator, multiply both the numerator and the denominator by the conjugate expression $\sqrt{x} + 2$:

$$
\begin{aligned}
\frac{\sqrt{x}-2}{x-4} &= \frac{(\sqrt{x}-2)(\sqrt{x}+2)}{(x-4)(\sqrt{x}+2)} \\
&= \frac{(\sqrt{x})^2 - 2^2}{(x-4)(\sqrt{x}+2)} \\
&= \frac{x-4}{(x-4)(\sqrt{x}+2)}
\end{aligned}
$$

For $x \neq 4$, the non-zero factor $(x - 4)$ cancels from the numerator and denominator:

$$
\frac{x-4}{(x-4)(\sqrt{x}+2)} = \frac{1}{\sqrt{x}+2} \qquad (x \neq 4)
$$

Now compute the limit as $x \to 4$:

$$
\lim_{x\to4}\frac{\sqrt{x}-2}{x-4} = \lim_{x\to4}\frac{1}{\sqrt{x}+2} = \frac{1}{\sqrt{4}+2} = \frac{1}{2+2} = \frac{1}{4}
$$

---

### 2. Alternative Factoring Approach

The denominator can also be factored as a difference of squares:

$$
x - 4 = (\sqrt{x})^2 - 2^2 = (\sqrt{x}-2)(\sqrt{x}+2)
$$

Substituting this into the fraction yields the same cancellation:

$$
\frac{\sqrt{x}-2}{x-4} = \frac{\sqrt{x}-2}{(\sqrt{x}-2)(\sqrt{x}+2)} = \frac{1}{\sqrt{x}+2} \to \frac{1}{4}
$$

---

### 3. Comparison with Exercise 3

- **Identical Core Mechanism:**
  In both problems, the algebraic identity $(A - B)(A + B) = A^2 - B^2$ is applied to eliminate square roots by turning a difference into a difference of squares.
- **Different Indeterminate Forms and Contexts:**
  - In Exercise 3, we considered a **sequence** as $n \to \infty$, where the indeterminate form was $\infty - \infty$. Multiplying by the conjugate moved the radical to the denominator and converted the difference of two large numbers into a quotient with a clear dominant linear term:

$$
\sqrt{n^2+5n}-n = \frac{5n}{\sqrt{n^2+5n}+n} \sim \frac{5n}{2n} = \frac{5}{2}
$$

  - In Exercise 8, we considered a **function** at a finite point $x \to 4$, where the indeterminate form was $\frac{0}{0}$. Multiplying by the conjugate created the factor $(x - 4)$ in the numerator, directly canceling the zero in the denominator:

$$
\frac{\sqrt{x}-2}{x-4} = \frac{x-4}{(x-4)(\sqrt{x}+2)} = \frac{1}{\sqrt{x}+2} \to \frac{1}{4}
$$

- In both situations, conjugation eliminates the algebraic root cause of the indeterminacy.

