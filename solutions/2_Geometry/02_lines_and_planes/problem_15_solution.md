# Exercise 15. Complete Classification of a Line Relative to a Plane

Let

$$
L:p+tv,\qquad \Pi:n\cdot x=d.
$$

State the conditions distinguishing the three cases: one intersection point, parallel with no common points, and the line contained in the plane. Then illustrate each case with your own simple numerical example.

## Solution

Substituting a point $p+tv$ from the line into the plane equation gives

$$
n\cdot(p+tv)=d
\quad\Longleftrightarrow\quad
n\cdot p+t(n\cdot v)=d.
$$

Thus:

1. **One intersection:** if $n\cdot v\ne0$, there is exactly one parameter,
   $$
   t=\frac{d-n\cdot p}{n\cdot v}.
   $$
   Example: in the plane $z=0$, the line $(0,0,1)+t(1,0,-1)$ intersects at $(1,0,0)$.
2. **Parallel, no common points:** if $n\cdot v=0$ but $n\cdot p\ne d$, the line direction is parallel to the plane while its base point is not on the plane. Example: $(0,0,1)+t(1,0,0)$ is parallel to and disjoint from $z=0$.
3. **Contained in the plane:** if $n\cdot v=0$ and $n\cdot p=d$, every point on the line satisfies the plane equation. Example: $(0,0,0)+t(1,0,0)$ lies entirely in $z=0$.