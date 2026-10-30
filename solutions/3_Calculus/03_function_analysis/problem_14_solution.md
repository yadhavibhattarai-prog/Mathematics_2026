# Problem 14. Reconstructing Information from the Derivative

It is known that

$$
f'(x)=(x-1)(x+2).
$$

Determine the monotonicity and the locations of the extrema, and sketch a possible qualitative shape of the function. Then, for

$$
g(x)=\frac{x^3}{3}+\frac{x^2}{2}-2x
$$

verify that $g'(x)=(x-1)(x+2)$, and compare the specific graph with the earlier qualitative sketch.

> **Why this problem:** it teaches how to read the behavior of a function directly from its derivative.

## Solution

### 1. Monotonicity and Extrema from $f'(x)$

The given derivative is

$$
f'(x) = (x - 1)(x + 2) = x^2 + x - 2
$$

The critical points where $f'(x) = 0$ are

$$
x_1 = -2, \qquad x_2 = 1
$$

Because $f'(x)$ is a quadratic polynomial with a positive leading coefficient ($a = 1 > 0$), it is an upward-opening parabola:

- **On $(-\infty, -2)$:**
  Both $x - 1 < 0$ and $x + 2 < 0$, so their product is positive:

$$
f'(x) > 0
$$

  The function $f$ is strictly increasing on $(-\infty, -2]$.

- **On $(-2, 1)$:**
  Here $x + 2 > 0$ and $x - 1 < 0$, so their product is negative:

$$
f'(x) < 0
$$

  The function $f$ is strictly decreasing on $[-2, 1]$.

- **On $(1, \infty)$:**
  Both $x + 2 > 0$ and $x - 1 > 0$, so their product is positive:

$$
f'(x) > 0
$$

  The function $f$ is strictly increasing on $[1, \infty)$.

#### Locations and Types of Local Extrema
- **At $x = -2$:**
  The derivative changes sign from positive to negative.
  Therefore, $f$ has a **local maximum** at $x = -2$.
- **At $x = 1$:**
  The derivative changes sign from negative to positive.
  Therefore, $f$ has a **local minimum** at $x = 1$.

---

### 2. Qualitative Shape of the Function $f(x)$

Even without knowing the vertical placement (constant of integration $C$), the derivative completely determines the geometry:
- It is a cubic polynomial of the form $f(x) = \frac{x^3}{3} + \frac{x^2}{2} - 2x + C$.
- The graph enters from $-\infty$ at the bottom-left, climbs strictly to a local crest at $x = -2$, descends through an inflection point at $x = -0.5$ into a local trough at $x = 1$, and climbs towards $+\infty$ at the top-right.

---

### 3. Verification for $g(x) = \frac{x^3}{3}+\frac{x^2}{2}-2x$

Differentiate $g(x)$ term by term using the power rule:

$$
\begin{aligned}
g'(x) &= \frac{d}{dx}\left(\frac{x^3}{3}\right) + \frac{d}{dx}\left(\frac{x^2}{2}\right) - \frac{d}{dx}(2x) \\
&= \frac{3x^2}{3} + \frac{2x}{2} - 2 \\
&= x^2 + x - 2
\end{aligned}
$$

Factor the resulting quadratic expression:

$$
x^2 + x - 2 = (x - 1)(x + 2)
$$

This verifies that

$$
g'(x) = (x - 1)(x + 2) = f'(x)
$$

identically for all $x \in \mathbb{R}$.

---

### 4. Comparison of the Specific Graph of $g(x)$ with the Qualitative Sketch

The specific function $g(x)$ corresponds to the particular choice of integration constant $C = 0$. We can now compute the exact coordinates of all key geometric landmarks:

1. **Local Maximum Point:**
   Evaluate at $x = -2$:

$$
g(-2) = \frac{(-2)^3}{3} + \frac{(-2)^2}{2} - 2(-2) = -\frac{8}{3} + 2 + 4 = -\frac{8}{3} + 6 = \frac{10}{3} \approx 3.333
$$

   Local maximum coordinates: $\left(-2, \frac{10}{3}\right)$.

2. **Local Minimum Point:**
   Evaluate at $x = 1$:

$$
g(1) = \frac{1^3}{3} + \frac{1^2}{2} - 2(1) = \frac{1}{3} + \frac{1}{2} - 2 = \frac{5}{6} - 2 = -\frac{7}{6} \approx -1.167
$$

   Local minimum coordinates: $\left(1, -\frac{7}{6}\right)$.

3. **Inflection Point:**
   The second derivative is $g''(x) = 2x + 1 = 0 \implies x = -\frac{1}{2}$.

$$
g\left(-\frac{1}{2}\right) = \frac{-1/8}{3} + \frac{1/4}{2} - 2\left(-\frac{1}{2}\right) = -\frac{1}{24} + \frac{1}{8} + 1 = \frac{-1 + 3 + 24}{24} = \frac{26}{24} = \frac{13}{12} \approx 1.083
$$

   Inflection point coordinates: $\left(-\frac{1}{2}, \frac{13}{12}\right)$.

4. **Zero Crossings (Intercepts):**
   Factor $g(x) = x\left(\frac{x^2}{3} + \frac{x}{2} - 2\right) = \frac{x}{6}(2x^2 + 3x - 12) = 0$:
   - $x = 0$ (passes through the origin $(0, 0)$),
   - Roots of $2x^2 + 3x - 12 = 0$: $x = \frac{-3 \pm \sqrt{9 + 96}}{4} = \frac{-3 \pm \sqrt{105}}{4} \approx -3.31$ and $1.81$.

#### Conclusion
The specific graph of $g(x)$ matches the qualitative sketch in every structural detail:
- It crests at $x = -2$ with a horizontal tangent at height $y = 3.33 > 0$,
- crosses the origin $(0, 0)$ with downward slope $g'(0) = -2$,
- bottoms out at $x = 1$ with a horizontal tangent at height $y = -1.17 < 0$,
confirming that the derivative captures the full geometric structure of the curve up to a vertical shift.

