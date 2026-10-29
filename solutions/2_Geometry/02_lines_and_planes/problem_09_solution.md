# Exercise 9. Distances

Compute:

1. the distance from $P=(2,3)$ to the line $3x+4y-10=0$,
2. the distance from $Q=(2,-1,3)$ to the plane $2x-2y+z-4=0$.

Compare the two formulas and explain their common connection with the normal direction.

## Solution

For a line $ax+by+c=0$, the point-to-line distance is $|ax_0+by_0+c|/\sqrt{a^2+b^2}$. Thus

$$
d(P,L)=\frac{|3(2)+4(3)-10|}{\sqrt{3^2+4^2}}=\frac85.
$$

For a plane $ax+by+cz+d=0$, use the corresponding formula in three dimensions:

$$
d(Q,\Pi)=\frac{|2(2)-2(-1)+3-4|}{\sqrt{2^2+(-2)^2+1^2}}=\frac53.
$$

In both cases the denominator is the length of the normal vector, and the numerator measures the point's signed displacement in the normal equation. Dividing by the normal length gives the perpendicular distance.