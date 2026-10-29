# Exercise 13. Intersection of a Sphere and a Plane

Given the sphere

$$
x^2+y^2+z^2=25
$$

and the plane $z=3$, find the equation of the intersection curve and its radius. Then describe what happens for $z=c$ depending on $c$.

> **Why this exercise:** connects a surface equation with the geometry of its intersection.

## Solution

### 1. Intersection with the Plane $z = 3$

The sphere is centered at the origin $(0, 0, 0)$ with radius $R = \sqrt{25} = 5$.

Substitute $z = 3$ into the equation of the sphere:

$$
x^2 + y^2 + 3^2 = 25 \implies x^2 + y^2 + 9 = 25 \implies x^2 + y^2 = 16
$$

The intersection curve in three-dimensional space is given by the system:

$$
\begin{cases}
x^2 + y^2 = 16, \\
z = 3.
\end{cases}
$$

In the horizontal plane $z = 3$, this equation represents a circle:
- **Center:** $(0, 0, 3)$
- **Radius:** $r = \sqrt{16} = 4$

#### Geometric Verification via the Pythagorean Theorem
The distance from the center of the sphere $(0, 0, 0)$ to the plane $z = 3$ is $d = 3$. By the Pythagorean theorem for the right triangle formed by the sphere radius $R$, plane distance $d$, and circle radius $r$:

$$
r = \sqrt{R^2 - d^2} = \sqrt{5^2 - 3^2} = \sqrt{25 - 9} = \sqrt{16} = 4
$$

The algebraic and geometric results match.

---

### 2. General Intersections with Planes $z = c$

Substitute $z = c$ into the sphere equation:

$$
x^2 + y^2 + c^2 = 25 \implies x^2 + y^2 = 25 - c^2
$$

The distance from the center $(0, 0, 0)$ to the plane $z = c$ is $d = |c|$. Depending on the value of $c$, three geometric cases arise:

#### Case 1: $|c| < 5$ (Secant Plane)
- The plane cuts through the interior of the sphere because the distance to the center is strictly less than the sphere's radius ($|c| < R$).
- The right-hand side is strictly positive: $25 - c^2 > 0$.
- The intersection is a **circle** lying in the plane $z = c$, centered at $(0, 0, c)$, with radius

$$
r(c) = \sqrt{25 - c^2}
$$

- For $c = 0$, the plane passes through the center of the sphere, giving the **great circle** (equator) of maximal radius $r(0) = 5$.
- As $|c|$ increases from $0$ towards $5$, the circle radius decreases monotonically from $5$ to $0$.

#### Case 2: $|c| = 5$ (Tangent Plane)
- The plane touches the sphere at exactly one point ($|c| = R$).
- The equation becomes $x^2 + y^2 = 0 \implies (x, y) = (0, 0)$.
- The intersection is a **single point** (a degenerate circle with radius $r = 0$):
  - For $c = 5$: the north pole $(0, 0, 5)$.
  - For $c = -5$: the south pole $(0, 0, -5)$.

#### Case 3: $|c| > 5$ (Disjoint Plane)
- The distance from the center to the plane exceeds the radius ($|c| > R$).
- The right-hand side is negative: $25 - c^2 < 0$.
- The equation $x^2 + y^2 = 25 - c^2$ has no real solutions.
- The intersection is the **empty set** ($\emptyset$); the plane and the sphere do not meet.

