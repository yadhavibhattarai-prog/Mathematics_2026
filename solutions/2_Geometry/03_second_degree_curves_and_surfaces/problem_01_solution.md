# Exercise 1. Recognizing Curves from Canonical Form

Recognize the curves

$$
x^2+y^2=9,
$$

$$
\frac{x^2}{16}+\frac{y^2}{9}=1,
$$

$$
y^2=8x,
$$

$$
\frac{x^2}{9}-\frac{y^2}{4}=1.
$$

For each one, identify the most important features and make a sketch. Explain which parts of the equation let you recognize the type of curve.

> **Why this exercise:** builds the basic dictionary: canonical equation → type of curve → shape and scale.

## Solution

### 1. The Curve $x^2+y^2=9$

- **Type of curve:** Circle.
- **Identification:** Both variables are squared with equal positive coefficients ($1$), and the constant on the right-hand side is positive ($R^2 = 9 > 0$).
- **Key geometric features:**
  - Center: $(0, 0)$.
  - Radius: $R = \sqrt{9} = 3$.
  - Intercepts with coordinate axes: $(\pm 3, 0)$ and $(0, \pm 3)$.
  - Symmetry: Symmetric with respect to both axes and the origin.

### 2. The Curve $\frac{x^2}{16}+\frac{y^2}{9}=1$

- **Type of curve:** Ellipse.
- **Identification:** Both variables are squared with different positive coefficients, and their sum equals $1$.
- **Key geometric features:**
  - Center: $(0, 0)$.
  - Semiaxis lengths: Major semiaxis $a = \sqrt{16} = 4$ along the $x$-axis; minor semiaxis $b = \sqrt{9} = 3$ along the $y$-axis.
  - Intercepts with coordinate axes: $(\pm 4, 0)$ on the $x$-axis, and $(0, \pm 3)$ on the $y$-axis.
  - Linear eccentricity: $c = \sqrt{a^2 - b^2} = \sqrt{16 - 9} = \sqrt{7}$.
  - Foci: $(\pm \sqrt{7}, 0)$.

### 3. The Curve $y^2=8x$

- **Type of curve:** Parabola.
- **Identification:** Only one variable ($y$) is squared, while the other ($x$) appears linearly to the first power.
- **Key geometric features:**
  - Canonical parameter: $y^2 = 2px$ with $2p = 8 \implies p = 4$.
  - Vertex: $(0, 0)$.
  - Axis of symmetry: The horizontal line $y = 0$ ($x$-axis).
  - Direction of opening: Opens to the right ($x \ge 0$), because $y^2 \ge 0$ forces $8x \ge 0$.
  - Focus: $(p/2, 0) = (2, 0)$.
  - Directrix: $x = -2$.
  - Sample points: For $x = 2$, $y = \pm 4$; for $x = 8$, $y = \pm 8$.

### 4. The Curve $\frac{x^2}{9}-\frac{y^2}{4}=1$

- **Type of curve:** Hyperbola.
- **Identification:** Both variables are squared with opposite signs (a minus sign precedes $y^2$), equal to $+1$.
- **Key geometric features:**
  - Center: $(0, 0)$.
  - Transverse axis: Along the $x$-axis, since the term with $x^2$ is positive.
  - Semiaxis lengths: Real semiaxis $a = \sqrt{9} = 3$; imaginary semiaxis $b = \sqrt{4} = 2$.
  - Vertices ($x$-intercepts): $(\pm 3, 0)$.
  - $y$-intercepts: None, as $-y^2/4 = 1$ has no real solutions.
  - Asymptotes: The straight lines $y = \pm \frac{b}{a}x = \pm \frac{2}{3}x$.
  - Foci: $c = \sqrt{a^2 + b^2} = \sqrt{9 + 4} = \sqrt{13}$, giving $(\pm \sqrt{13}, 0)$.

