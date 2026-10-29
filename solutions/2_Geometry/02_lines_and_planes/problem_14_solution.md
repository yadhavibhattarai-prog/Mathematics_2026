# Exercise 14. Contrast: Intersection and Parallelism

From the point $P=(0,0,1)$, two lines are drawn with direction vectors

$$
v_1=(2,1,-1),\qquad v_2=(2,1,0).
$$

For each line, analyze its position relative to the plane $z=0$.

For the line that intersects the plane, find the intersection point. For the other line, explain how you can recognize parallelism without solving an equation.

## Solution

The plane $z=0$ has normal vector $n=(0,0,1)$.

- For direction $v_1$, $n\cdot v_1=-1\ne0$, so the line intersects the plane once. Its points are $(2t,t,1-t)$; setting $z=0$ gives $t=1$, hence the intersection is $(2,1,0)$.
- For direction $v_2$, $n\cdot v_2=0$, so the line is parallel to the plane or contained in it. Its base point has $z=1$, not $z=0$, so it is parallel and disjoint from the plane.

The zero dot product detects parallel direction; checking the base point shows the line is not contained in the plane.