# Problem 14. Continuity and Differentiability of a Piecewise Function

Investigate the behavior at $x=0$ of

$$
f(x)=
\begin{cases}
x^2,&x\ge0, \\
ax,&x<0.
\end{cases}
$$

For which values of $a$ is the function continuous? For which values do the one-sided derivatives exist and agree? For which value of $a$ is the function differentiable? Explain why continuity alone is not sufficient.

> **Why this problem:** it requires an organized argument and a clear distinction between two concepts.

## Solution

### 1. Continuity at $x = 0$

A function $f$ is continuous at $x = 0$ if and only if

$$
\lim_{x\to0^-} f(x) = \lim_{x\to0^+} f(x) = f(0)
$$

Compute each of the three quantities:
- **Function value at $x = 0$:**
  For $x \ge 0$, $f(x) = x^2$, so

$$
f(0) = 0^2 = 0
$$

- **Right-hand limit ($x \to 0^+$):**
  For $x > 0$, $f(x) = x^2$, so

$$
\lim_{x\to0^+} f(x) = \lim_{x\to0^+} x^2 = 0^2 = 0
$$

- **Left-hand limit ($x \to 0^-$):**
  For $x < 0$, $f(x) = ax$, so

$$
\lim_{x\to0^-} f(x) = \lim_{x\to0^-} (ax) = a(0) = 0
$$

Because $\lim_{x\to0^-} f(x) = \lim_{x\to0^+} f(x) = f(0) = 0$ for every real number $a$:

The function $f$ is continuous at $x = 0$ for **all** $a \in \mathbb{R}$.

---

### 2. Existence and Agreement of One-Sided Derivatives

Use the limit definitions of one-sided derivatives at $x = 0$:

#### Right-Hand Derivative $f'_+(0)$
Approaching from the right ($h > 0$):

$$
f'_+(0) = \lim_{h\to0^+}\frac{f(0 + h) - f(0)}{h} = \lim_{h\to0^+}\frac{h^2 - 0}{h} = \lim_{h\to0^+} h = 0
$$

The right-hand derivative exists and equals $0$ for all $a$.

#### Left-Hand Derivative $f'_-(0)$
Approaching from the left ($h < 0$):

$$
f'_-(0) = \lim_{h\to0^-}\frac{f(0 + h) - f(0)}{h} = \lim_{h\to0^-}\frac{a h - 0}{h} = \lim_{h\to0^-} a = a
$$

The left-hand derivative exists and equals $a$ for all $a$.

#### Agreement of One-Sided Derivatives
Both one-sided derivatives exist for every $a \in \mathbb{R}$. They agree if and only if

$$
f'_-(0) = f'_+(0) \iff a = 0
$$

---

### 3. Differentiability at $x = 0$

By definition, a function is differentiable at an interior point of its domain if and only if both one-sided derivatives exist and are equal.

Therefore:

The function $f$ is differentiable at $x = 0$ if and only if

$$
a = 0
$$

When $a = 0$, the derivative at the origin is $f'(0) = 0$.

---

### 4. Why Continuity Alone is Not Sufficient for Differentiability

1. **Topological vs Geometric Requirements:**
   - **Continuity** is a topological property ensuring that the graph has no breaks, jumps, or missing points (the curve is drawn in one stroke). Here, both branches meet at the origin $(0, 0)$ for any value of $a$.
   - **Differentiability** is a geometric property requiring that the graph be smooth, meaning it possesses a unique non-vertical tangent line at the point.
2. **Presence of a Corner Point (Kink):**
   When $a \neq 0$:
   - The graph approaches the origin from the left along a straight line of non-zero slope $a$.
   - The graph leaves the origin to the right along a parabola with horizontal tangent slope $0$.
   At the junction $(0, 0)$, the graph forms a sharp corner (kink) where the direction of the curve abruptly changes. Because the left-hand slope ($a$) disagrees with the right-hand slope ($0$), no unique tangent line exists at $(0, 0)$, and the function fails to be differentiable.

