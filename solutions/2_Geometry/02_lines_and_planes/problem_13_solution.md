# Exercise 13. Closest Point on a Plane

Find the point on the plane $x+2y+2z=4$ closest to $P=(3,0,0)$. Give the distance and check that the segment joining the two points is perpendicular to the plane.

## Solution

The plane has normal vector $n=(1,2,2)$, with $\|n\|^2=9$. Since $n\cdot P=3$, project onto the plane by moving along the normal:

$$
Q=P-\frac{n\cdot P-4}{\|n\|^2}n
=(3,0,0)-\frac{-1}{9}(1,2,2)
=\left(\frac{28}{9},\frac29,\frac29\right).
$$

Check that $Q$ lies on the plane:

$$
\frac{28}{9}+2\left(\frac29\right)+2\left(\frac29\right)=4.
$$

The distance is

$$
d(P,Q)=\frac{|n\cdot P-4|}{\|n\|}=\frac13.
$$

The displacement $Q-P=(1,2,2)/9$ is a scalar multiple of the plane normal, so the segment is perpendicular to the plane.