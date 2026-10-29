# Exercise 1. Line Through Two Points

Find the equation of the line through $A=(1,2)$ and $B=(4,-1)$ in parametric and general form. Identify a direction vector and an example of a normal vector. Check that both points satisfy the equation you obtain.

## Solution

A direction vector from $A$ to $B$ is

$$
v=B-A=(4-1,-1-2)=(3,-3).
$$

The parametric equation through $A$ with this direction is

$$
(x,y)=(1,2)+t(3,-3),\qquad t\in\mathbb R,
$$

or $x=1+3t,\ y=2-3t$. A normal vector is $n=(1,1)$, since $n\cdot v=3-3=0$. The line's general equation through $A$ is therefore

$$
x+y=3 \qquad\text{or}\qquad x+y-3=0.
$$

Both points satisfy it: $1+2=3$ and $4+(-1)=3$.