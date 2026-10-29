# Exercise 11. Plane Containing a Line and a Point

Find the equation of the plane containing

$$
(x,y,z)=(1,0,2)+t(1,1,-1)
$$

and the point $P=(0,2,1)$. Check that both the entire line and the point lie in the plane you obtain.

## Solution

The line has base point $A=(1,0,2)$ and direction $v=(1,1,-1)$. A second direction in the plane is

$$
w=P-A=(-1,2,-1).
$$

A normal vector is

$$
n=v\times w=(1,2,3).
$$

The plane through $A$ is therefore

$$
x+2y+3z=7.
$$

For every point on the line, the left-hand side is
$$(1+t)+2t+3(2-t)=7,$$
so the entire line lies in the plane. The given point also satisfies it: $0+2(2)+3(1)=7$.