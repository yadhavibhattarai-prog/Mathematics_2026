# Exercise 9. Ellipsoid and Its Cross-Sections

Consider

$$
\frac{x^2}{9}+\frac{y^2}{4}+\frac{z^2}{16}=1.
$$

Give the semiaxis lengths, describe the cross-section $z=0$, and explain how the cross-sections $z=c$ change for $|c|<4$.

> **Why this exercise:** teaches how to understand a 3D surface through a family of simpler 2D cross-sections.

## Solution

### 1. Semiaxis Lengths

The standard equation of an ellipsoid centered at the origin $(0, 0, 0)$ is

$$
\frac{x^2}{a^2} + \frac{y^2}{b^2} + \frac{z^2}{c_z^2} = 1
$$

Comparing with the given equation:

- Along the $x$-axis: $a^2 = 9 \implies a = 3$
- Along the $y$-axis: $b^2 = 4 \implies b = 2$
- Along the $z$-axis: $c_z^2 = 16 \implies c_z = 4$

The semiaxis lengths are $a = 3$, $b = 2$, and $c_z = 4$. The ellipsoid is most elongated vertically along the $z$-axis and narrowest along the $y$-axis.

### 2. Cross-Section with the Plane $z = 0$

Substitute $z = 0$ into the equation of the ellipsoid:

$$
\frac{x^2}{9} + \frac{y^2}{4} + 0 = 1 \implies \frac{x^2}{9} + \frac{y^2}{4} = 1
$$

In the coordinate plane $z = 0$ (the $xy$-plane), this equation represents an ellipse centered at $(0, 0, 0)$ with:

- Semiaxis along $x$: $a = 3$
- Semiaxis along $y$: $b = 2$
- Vertices: $(\pm 3, 0, 0)$ and $(0, \pm 2, 0)$

This is the largest horizontal cross-section of the ellipsoid (the equatorial ellipse).

### 3. Family of Horizontal Cross-Sections $z = c$ for $|c| < 4$

Substitute $z = c$ into the equation:

$$
\frac{x^2}{9} + \frac{y^2}{4} + \frac{c^2}{16} = 1 \implies \frac{x^2}{9} + \frac{y^2}{4} = 1 - \frac{c^2}{16}
$$

For $|c| < 4$, the right-hand side is strictly positive:

$$
1 - \frac{c^2}{16} > 0
$$

Dividing both sides by $1 - \frac{c^2}{16}$ gives the canonical form of the curve in the plane $z = c$:

$$
\frac{x^2}{9\left(1 - \frac{c^2}{16}\right)} + \frac{y^2}{4\left(1 - \frac{c^2}{16}\right)} = 1
$$

This represents a family of concentric ellipses in planes parallel to the $xy$-plane:

- **Semiaxes at height $z = c$:**

$$
a(c) = 3\sqrt{1 - \frac{c^2}{16}}, \quad b(c) = 2\sqrt{1 - \frac{c^2}{16}}
$$

- **Constant aspect ratio:**
  The ratio of the semiaxes is independent of $c$:

$$
\frac{a(c)}{b(c)} = \frac{3\sqrt{1 - c^2/16}}{2\sqrt{1 - c^2/16}} = \frac{3}{2}
$$

  All horizontal slices are geometrically similar ellipses.

- **Variation with $|c|$:**
  - At $c = 0$, the semiaxes reach their maximum values $a(0) = 3$ and $b(0) = 2$.
  - As $|c|$ increases from $0$ towards $4$, the scaling factor $\sqrt{1 - c^2/16}$ decreases monotonically to $0$, so the ellipses shrink continuously.
  - At the boundary $|c| = 4$ ($z = \pm 4$), the semiaxes shrink to $0$, degenerating into the points $(0, 0, \pm 4)$, which are the upper and lower poles of the ellipsoid.
  - For $|c| > 4$, $1 - c^2/16 < 0$, which yields no real solutions, confirming that the entire surface is bounded within the slab $-4 \le z \le 4$.

