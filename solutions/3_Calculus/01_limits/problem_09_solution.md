# Exercise 9. One-Sided Limits and an Asymptote

Analyze the left-hand and right-hand limits of

$$
f(x)=\frac1{x-2}
$$

as $x\to2$. Does the two-sided limit exist? Interpret the result on a sketch of the graph and identify the vertical asymptote.

> **Why this exercise:** teaches how to distinguish one-sided limits and connect them with the geometry of an asymptote.

## Solution

### 1. Analysis of One-Sided Limits

The function is

$$
f(x) = \frac{1}{x-2}
$$

defined on the domain $D = \mathbb{R} \setminus \{2\}$.

#### Right-Hand Limit ($x \to 2^+$)
When $x$ approaches $2$ from the right, $x > 2$, which implies that the denominator $x - 2$ is strictly positive:

$$
x - 2 > 0, \qquad (x - 2) \to 0^+
$$

The fraction $\frac{1}{x-2}$ is a positive quotient of a fixed positive constant ($1$) by an arbitrarily small positive quantity:

$$
\lim_{x\to2^+} \frac{1}{x-2} = +\infty
$$

#### Left-Hand Limit ($x \to 2^-$)
When $x$ approaches $2$ from the left, $x < 2$, which implies that the denominator $x - 2$ is strictly negative:

$$
x - 2 < 0, \qquad (x - 2) \to 0^-
$$

The fraction $\frac{1}{x-2}$ is a negative quotient of a fixed positive constant ($1$) by an arbitrarily small negative quantity:

$$
\lim_{x\to2^-} \frac{1}{x-2} = -\infty
$$

---

### 2. Existence of the Two-Sided Limit

A two-sided limit $\lim_{x\to 2} f(x)$ exists if and only if both one-sided limits exist and are equal:

$$
\lim_{x\to 2^-} f(x) = \lim_{x\to 2^+} f(x) = L
$$

Because the two one-sided limits are infinite and have opposite signs:

$$
\lim_{x\to 2^-} f(x) = -\infty \neq +\infty = \lim_{x\to 2^+} f(x)
$$

the two-sided limit $\lim_{x\to 2} \frac{1}{x-2}$ **does not exist** (neither as a finite real number nor as a signed infinity).

---

### 3. Geometric Interpretation and Vertical Asymptote

- **Vertical Asymptote:**
  By definition, the line $x = x_0$ is a vertical asymptote of $f(x)$ if at least one of the one-sided limits as $x \to x_0$ is $+\infty$ or $-\infty$.
  Here, both one-sided limits are infinite, so the straight line

$$
x = 2
$$

  is a **vertical two-sided asymptote** of the curve $y = f(x)$.

- **Behavior on the Graph:**
  - As $x$ approaches $2$ from values greater than $2$, the graph shoots upwards toward $+\infty$, staying to the right of the vertical line $x = 2$.
  - As $x$ approaches $2$ from values less than $2$, the graph plunges downwards toward $-\infty$, staying to the left of the vertical line $x = 2$.
  - The graph is a rectangular hyperbola obtained by shifting the standard reciprocal function $y = \frac{1}{x}$ horizontally by $+2$ units to the right.
  - The horizontal line $y = 0$ ($x$-axis) is a horizontal asymptote since $\lim_{x\to\pm\infty}\frac{1}{x-2} = 0$.
