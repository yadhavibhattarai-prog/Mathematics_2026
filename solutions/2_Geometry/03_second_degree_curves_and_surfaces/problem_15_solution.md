# Exercise 15. Recognition and Sketch Without a Given Name

Consider the two equations:

$$
4x^2+9y^2-8x+36y+4=0,
$$

$$
4x^2+y^2=z^2.
$$

For the first equation, reduce it to canonical form, recognize the curve, give its most important features, and make a sketch.

For the second equation, do not begin by using a ready-made name for the surface. First describe the cross-sections $z=c$ and the cross-sections by the planes $x=0$ and $y=0$, paying attention to the different scales along the axes. Only then identify the surface and make a sketch.

> **Why this exercise:** tests transfer of the two main mechanisms of the set—moving to canonical form and recognizing an object through cross-sections—without allowing the easiest example to be chosen.

## Solution

### 1. First Equation: $4x^2+9y^2-8x+36y+4=0$

#### Reduction to Canonical Form
Group terms by variables:

$$
(4x^2 - 8x) + (9y^2 + 36y) + 4 = 0
$$

Factor out the leading coefficients:

$$
4(x^2 - 2x) + 9(y^2 + 4y) + 4 = 0
$$

Complete the square inside each parenthesis:

$$
\begin{aligned}
x^2 - 2x &= (x - 1)^2 - 1 \\
y^2 + 4y &= (y + 2)^2 - 4
\end{aligned}
$$

Substitute these into the equation:

$$
4\left((x - 1)^2 - 1\right) + 9\left((y + 2)^2 - 4\right) + 4 = 0
$$

Expand and simplify constants:

$$
4(x - 1)^2 - 4 + 9(y + 2)^2 - 36 + 4 = 0
$$

$$
4(x - 1)^2 + 9(y + 2)^2 = 36
$$

Divide both sides by $36$:

$$
\frac{4(x - 1)^2}{36} + \frac{9(y + 2)^2}{36} = 1
$$

$$
\frac{(x - 1)^2}{9} + \frac{(y + 2)^2}{4} = 1
$$

Writing the denominators as squares:

$$
\frac{(x - 1)^2}{3^2} + \frac{(y + 2)^2}{2^2} = 1
$$

#### Identification and Geometric Features
- **Curve Type:** Shifted ellipse.
- **Center:** $S = (x_0, y_0) = (1, -2)$.
- **Semiaxis Lengths:**
  - Major semiaxis along $x$: $a = 3$.
  - Minor semiaxis along $y$: $b = 2$.
- **Axes of Symmetry:**
  - Major axis: The horizontal line $y = -2$.
  - Minor axis: The vertical line $x = 1$.
- **Vertices:**
  - On the major axis: $(1 \pm 3, -2)$, giving $A_1 = (-2, -2)$ and $A_2 = (4, -2)$.
  - On the minor axis (co-vertices): $(1, -2 \pm 2)$, giving $B_1 = (1, -4)$ and $B_2 = (1, 0)$.
- **Foci:**
  - Linear eccentricity: $c_f = \sqrt{a^2 - b^2} = \sqrt{9 - 4} = \sqrt{5}$.
  - Foci coordinates: $F_{1,2} = (1 \pm \sqrt{5}, -2)$.

---

### 2. Second Equation: $4x^2+y^2=z^2$

#### Horizontal Cross-Sections $z = c$
Substitute $z = c$ into the equation:

$$
4x^2 + y^2 = c^2
$$

- **For $c = 0$:**
  The equation becomes $4x^2 + y^2 = 0$. Since squares of real numbers are non-negative, the only solution is $(x, y) = (0, 0)$.
  The cross-section is the single point $(0, 0, 0)$.

- **For $c \neq 0$:**
  Divide both sides by $c^2 > 0$:

$$
\frac{4x^2}{c^2} + \frac{y^2}{c^2} = 1 \implies \frac{x^2}{\left(\frac{|c|}{2}\right)^2} + \frac{y^2}{|c|^2} = 1
$$

  In the plane $z = c$, this is an ellipse centered at $(0, 0, c)$ with:
  - Semiaxis along the $x$-direction: $a(c) = \frac{|c|}{2}$
  - Semiaxis along the $y$-direction: $b(c) = |c|$
  
  **Scale comparison along the axes:**
  For every non-zero height $c$, the ratio of the semiaxes is

$$
\frac{b(c)}{a(c)} = \frac{|c|}{|c|/2} = 2
$$

  The cross-section is always twice as wide in the $y$-direction as it is in the $x$-direction. The slices are geometrically similar ellipses whose sizes scale linearly with $|c|$.

#### Vertical Cross-Section $x = 0$ ($yz$-plane)
Substitute $x = 0$:

$$
y^2 = z^2 \implies y^2 - z^2 = 0 \implies (y - z)(y + z) = 0 \implies y = \pm z
$$

In the $yz$-plane, this is a pair of straight lines intersecting at the origin with slope $\pm 1$ ($45^\circ$ angles with the coordinate axes).

#### Vertical Cross-Section $y = 0$ ($xz$-plane)
Substitute $y = 0$:

$$
4x^2 = z^2 \implies z^2 - 4x^2 = 0 \implies (z - 2x)(z + 2x) = 0 \implies z = \pm 2x
$$

In the $xz$-plane, this is a pair of straight lines intersecting at the origin with slope $\pm 2$ relative to the $x$-axis. The surface rises twice as steeply along the $x$-axis as it does along the $y$-axis.

#### Identification of the Surface
The deductions reveal that:
1. Slicing with horizontal planes $z = c$ gives ellipses whose dimensions are strictly proportional to $|c|$.
2. At $z = 0$, the slice shrinks to a single point (apex).
3. Slicing with vertical planes through the origin gives pairs of intersecting straight lines.
4. The equation is quadratic and homogeneous: if $(x, y, z)$ lies on the surface, then $(\lambda x, \lambda y, \lambda z)$ also lies on the surface for every real $\lambda$.

Therefore, the surface is an **elliptic cone** with vertex at the origin $(0, 0, 0)$ and principal axis along the $z$-axis, with an elliptical cross-section having an aspect ratio of $2:1$ (elongated along the $y$-axis).

