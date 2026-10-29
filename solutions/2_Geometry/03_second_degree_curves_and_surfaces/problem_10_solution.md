# Exercise 10. Paraboloids

Compare

$$
z=x^2+y^2
$$

and

$$
z=x^2-y^2.
$$

For each surface, describe the cross-sections $x=0$, $y=0$, and $z=c$, then make a qualitative sketch.

> **Why this exercise:** teaches how to distinguish two basic types of paraboloids from their cross-sections.

## Solution

### 1. Analysis of $z = x^2 + y^2$ (Elliptic / Circular Paraboloid)

#### Cross-Sections by Coordinate Planes
- **Cross-section with $x = 0$ ($yz$-plane):**
  Substituting $x = 0$ yields

$$
z = y^2
$$

  This is a parabola opening upwards ($z \ge 0$) with vertex at $(0, 0, 0)$ and the $z$-axis as its axis of symmetry.

- **Cross-section with $y = 0$ ($xz$-plane):**
  Substituting $y = 0$ yields

$$
z = x^2
$$

  This is an identical parabola opening upwards ($z \ge 0$) with vertex at $(0, 0, 0)$ and the $z$-axis as its axis of symmetry.

#### Horizontal Cross-Sections $z = c$
- **For $c > 0$:**
  Substituting $z = c$ yields

$$
x^2 + y^2 = c = (\sqrt{c})^2
$$

  Each horizontal slice is a circle centered on the $z$-axis with radius $R(c) = \sqrt{c}$. As $c$ increases, the radius grows proportionally to $\sqrt{c}$.
- **For $c = 0$:**

$$
x^2 + y^2 = 0 \implies (x, y) = (0, 0)
$$

  The cross-section reduces to a single point, the vertex $(0, 0, 0)$, which is the global minimum of the surface.
- **For $c < 0$:**

$$
x^2 + y^2 = c < 0
$$

  There are no real solutions. The surface lies entirely in the upper half-space $z \ge 0$.

#### Qualitative Geometry
The surface is a rotationally symmetric, bowl-shaped cup opening upwards. Every vertical section through the $z$-axis is an upward-opening parabola, and every horizontal section above the vertex is a circle.

---

### 2. Analysis of $z = x^2 - y^2$ (Hyperbolic Paraboloid)

#### Cross-Sections by Coordinate Planes
- **Cross-section with $x = 0$ ($yz$-plane):**
  Substituting $x = 0$ yields

$$
z = -y^2
$$

  This is a downward-opening parabola ($z \le 0$) with vertex at $(0, 0, 0)$.

- **Cross-section with $y = 0$ ($xz$-plane):**
  Substituting $y = 0$ yields

$$
z = x^2
$$

  This is an upward-opening parabola ($z \ge 0$) with vertex at $(0, 0, 0)$.

#### Horizontal Cross-Sections $z = c$
- **For $c > 0$:**
  Substituting $z = c$ yields

$$
x^2 - y^2 = c \implies \frac{x^2}{c} - \frac{y^2}{c} = 1
$$

  These are hyperbolas opening along the $x$-axis with vertices at $(\pm\sqrt{c}, 0, c)$ and asymptotes $y = \pm x$.
- **For $c = 0$:**

$$
x^2 - y^2 = 0 \implies (x - y)(x + y) = 0 \implies y = \pm x
$$

  The cross-section consists of two straight lines intersecting at the origin at angles of $45^\circ$ to the axes.
- **For $c < 0$:**
  Substituting $z = c = -|c|$ yields

$$
x^2 - y^2 = -|c| \implies y^2 - x^2 = |c| \implies \frac{y^2}{|c|} - \frac{x^2}{|c|} = 1
$$

  These are hyperbolas opening along the $y$-axis with vertices at $(0, \pm\sqrt{|c|}, c)$ and the same asymptotes $y = \pm x$.

#### Qualitative Geometry
The surface has the shape of a saddle (or a mountain pass). As one moves along the $x$-direction across the origin, the surface curves upwards ($z = x^2$), while along the $y$-direction it curves downwards ($z = -y^2$). The origin $(0, 0, 0)$ is a saddle point (minimax point).

---

### 3. Comparison Summary

- **Sign of Curvatures:**
  - In $z = x^2 + y^2$, both principal vertical parabolas ($z = x^2$ and $z = y^2$) have positive curvature (both open upwards). The Gaussian curvature is positive everywhere.
  - In $z = x^2 - y^2$, the two principal vertical parabolas have opposite signs ($z = x^2$ opens up, $z = -y^2$ opens down). The Gaussian curvature is negative everywhere.
- **Nature of Horizontal Slices:**
  - For $z = x^2 + y^2$, slices are concentric circles expanding upwards, with no points below $z = 0$.
  - For $z = x^2 - y^2$, slices are hyperbolas for all $c \neq 0$, switching their transverse axis from $x$ (for $c > 0$) to $y$ (for $c < 0$), passing through a degenerate pair of intersecting lines at $c = 0$.

