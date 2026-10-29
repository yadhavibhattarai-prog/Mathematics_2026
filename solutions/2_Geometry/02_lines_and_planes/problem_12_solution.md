# Exercise 12. Intersection Line of Two Planes

Find a parametric equation of the line that is the intersection of

$$
x+y+z=3,\qquad x-y+z=1.
$$

Find its direction vector in two ways: from the system of equations and from the cross product of the normal vectors. Compare the results.

## Solution

Subtract the second plane equation from the first to get $2y=2$, so $y=1$. Substitution gives $x+z=2$. Let $z=t$; then $x=2-t$, and the intersection line is

$$
(x,y,z)=(2,1,0)+t(-1,0,1),\qquad t\in\mathbb R.
$$

The direction vector from this parametrization is $(-1,0,1)$. The plane normals are $n_1=(1,1,1)$ and $n_2=(1,-1,1)$, whose cross product is

$$
n_1\times n_2=(2,0,-2)=-2(-1,0,1).
$$

This is a nonzero scalar multiple of the same direction, as expected.