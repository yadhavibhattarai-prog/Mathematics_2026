# Exercise 13. Fundamental Trigonometric Limit

Using

$$
\lim_{x\to0}\frac{\sin x}{x}=1,
$$

compute

$$
\lim_{x\to0}\frac{\sin5x}{x},\qquad \lim_{x\to0}\frac{\sin2x}{\sin3x}.
$$

In each case, show how you reduce the expression to the fundamental limit.

> **Why this exercise:** teaches how to reduce new limits to one known pattern.

## Solution

### 1. Fundamental Pattern

The fundamental trigonometric limit states that for any variable $u \to 0$:

$$
\lim_{u\to0}\frac{\sin u}{u} = 1
$$

To apply this pattern, the argument inside the sine function must exactly match the expression in the denominator, and both must approach $0$.

---

### 2. First Limit: $\lim_{x\to0}\frac{\sin5x}{x}$

The argument of the sine is $5x$, while the denominator is $x$.
To match the argument, multiply and divide the fraction by $5$:

$$
\frac{\sin5x}{x} = 5 \cdot \frac{\sin5x}{5x}
$$

Let $u = 5x$. As $x \to 0$, we have $u \to 0$.

Applying the fundamental limit:

$$
\lim_{x\to0}\frac{\sin5x}{5x} = \lim_{u\to0}\frac{\sin u}{u} = 1
$$

Using the constant multiple rule for limits:

$$
\lim_{x\to0}\frac{\sin5x}{x} = 5 \cdot \lim_{x\to0}\frac{\sin5x}{5x} = 5 \cdot 1 = 5
$$

---

### 3. Second Limit: $\lim_{x\to0}\frac{\sin2x}{\sin3x}$

The numerator contains $\sin 2x$ and the denominator contains $\sin 3x$.
Divide both numerator and denominator by $x$ (valid for $x \neq 0$):

$$
\frac{\sin2x}{\sin3x} = \frac{\frac{\sin2x}{x}}{\frac{\sin3x}{x}}
$$

Normalize each sub-expression to the fundamental form by multiplying and dividing by the appropriate constant:
- For the numerator: $\frac{\sin2x}{x} = 2 \cdot \frac{\sin2x}{2x}$
- For the denominator: $\frac{\sin3x}{x} = 3 \cdot \frac{\sin3x}{3x}$

Combine these into a single expression:

$$
\frac{\sin2x}{\sin3x} = \frac{2 \cdot \frac{\sin2x}{2x}}{3 \cdot \frac{\sin3x}{3x}} = \frac{2}{3} \cdot \frac{\frac{\sin2x}{2x}}{\frac{\sin3x}{3x}}
$$

As $x \to 0$, both $2x \to 0$ and $3x \to 0$:

$$
\lim_{x\to0}\frac{\sin2x}{2x} = 1, \qquad \lim_{x\to0}\frac{\sin3x}{3x} = 1
$$

Since the denominator approaches $1 \neq 0$, apply the quotient limit law:

$$
\lim_{x\to0}\frac{\sin2x}{\sin3x} = \frac{2}{3} \cdot \frac{1}{1} = \frac{2}{3}
$$

---

### 4. General Formula

For any real constants $a \neq 0$ and $b \neq 0$:

$$
\lim_{x\to0}\frac{\sin(ax)}{bx} = \frac{a}{b} \cdot \lim_{x\to0}\frac{\sin(ax)}{ax} = \frac{a}{b}
$$

$$
\lim_{x\to0}\frac{\sin(ax)}{\sin(bx)} = \frac{a}{b} \cdot \lim_{x\to0}\frac{\frac{\sin(ax)}{ax}}{\frac{\sin(bx)}{bx}} = \frac{a}{b}
$$

