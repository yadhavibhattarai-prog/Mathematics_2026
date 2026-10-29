# Exercise 10. Projection of a Point onto a Plane

Find the orthogonal projection of $P=(2,1,3)$ onto the plane $x+y+z=3$, and then find the reflection of $P$ across this plane. Check that the midpoint of the segment joining the point and its reflection lies on the plane.

## Solution

The plane's normal vector is $n=(1,1,1)$, and $n\cdot P=6$. The projection onto $n\cdot x=3$ is

$$
P_{\mathrm{proj}}=P-\frac{n\cdot P-3}{\|n\|^2}n
=(2,1,3)-\frac{3}{3}(1,1,1)=(1,0,2).
$$

Reflecting across the plane moves the point twice this normal displacement:

$$
P_{\mathrm{refl}}=P-2\frac{n\cdot P-3}{\|n\|^2}n
=(2,1,3)-2(1,1,1)=(0,-1,1).
$$

Their midpoint is

$$
\frac{P+P_{\mathrm{refl}}}{2}=(1,0,2),
$$

and $1+0+2=3$, so it lies on the plane (it is the orthogonal projection).