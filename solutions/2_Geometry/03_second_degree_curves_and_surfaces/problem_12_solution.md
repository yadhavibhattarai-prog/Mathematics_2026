# Exercise 12. Recognizing a Surface from Cross-Sections

A certain surface has the following properties:
- the cross-section $z=0$ is a point,
- for $z>0$, the cross-sections $z=\mathrm{const}$ are circles with increasing radius,
- vertical cross-sections through the $Oz$ axis are parabolas.

Propose a simple equation for such a surface and justify your choice.

> **Why this exercise:** reverses the usual reasoning: from geometry to an equation.

## Solution

### 1. Proposed Equation

A simple canonical equation for this surface is

$$
z = x^2 + y^2
$$

(or more generally $z = k(x^2 + y^2)$ with any positive constant $k > 0$).

This surface is an **elliptic paraboloid of revolution** (or circular paraboloid).

---

### 2. Step-by-Step Justification

#### Requirement 1: Horizontal Cross-Sections are Concentric Circles
Any surface of revolution with the $z$-axis as its axis of symmetry, whose cross-sections parallel to the $xy$-plane are circles centered on the $z$-axis, must have an equation of the form

$$
x^2 + y^2 = f(z)
$$

where $R(z) = \sqrt{f(z)}$ represents the radius of the circle at height $z$.

#### Requirement 2: Cross-Section $z = 0$ is a Single Point
Setting $z = 0$ gives

$$
x^2 + y^2 = f(0)
$$

For this equation to represent a single point (the origin $(0, 0, 0)$), we must have

$$
f(0) = 0
$$

Since $x^2 + y^2 = 0$ has the unique real solution $(x, y) = (0, 0)$.

#### Requirement 3: Increasing Radius for $z > 0$
For $z > 0$, the cross-section must be a non-empty circle with radius $R(z) > 0$ that grows strictly as $z$ increases:

$$
f(z) > 0, \qquad f'(z) > 0
$$

for all $z > 0$.

#### Requirement 4: Vertical Cross-Sections Through $Oz$ are Parabolas
Any vertical plane passing through the $Oz$ axis makes an angle $\theta$ with the positive $x$-axis. Let $r$ be the horizontal radial distance from the $z$-axis:

$$
x = r\cos\theta, \qquad y = r\sin\theta
$$

Substituting these into $x^2 + y^2 = f(z)$:

$$
r^2\cos^2\theta + r^2\sin^2\theta = f(z) \implies r^2 = f(z)
$$

For the curve in this vertical plane to be a parabola with vertex at the origin and axis of symmetry along the $z$-axis, the vertical coordinate $z$ must depend quadratically on the radial coordinate $r$:

$$
z = k r^2 \quad (k > 0) \implies r^2 = \frac{z}{k}
$$

Comparing with $r^2 = f(z)$ shows that the function must be linear in $z$:

$$
f(z) = \frac{z}{k}
$$

Choosing the simplest scaling factor $k = 1$ yields

$$
f(z) = z
$$

which produces the equation:

$$
x^2 + y^2 = z \iff z = x^2 + y^2
$$

---

### 3. Verification of All Given Properties

1. **At $z = 0$:**
   $x^2 + y^2 = 0 \implies (x, y) = (0, 0)$. The section is the single point $(0, 0, 0)$.
2. **For $z = c > 0$:**
   $x^2 + y^2 = c = (\sqrt{c})^2$, which is a circle of radius $R(c) = \sqrt{c}$. Since the derivative $\frac{dR}{dc} = \frac{1}{2\sqrt{c}} > 0$, the radius strictly increases with height.
3. **Vertical section through $Oz$ (for example $y = 0$):**
   $z = x^2$, which is a parabola opening upwards with vertex at the origin.
