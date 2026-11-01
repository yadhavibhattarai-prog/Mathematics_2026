## Question

### Problem 11. Volume of a Solid of Revolution

The region under the graph

$$
y=\sqrt{x},\qquad x\in[0,4],
$$

is rotated about the $x$-axis.

1. Construct the integral describing the volume using the disk method.
2. Compute the volume.
3. Explain where the factor $\pi y^2$ in the integral comes from.

## Solution

### 1. Set up the integral

When the region under $y=\sqrt{x}$ is rotated about the $x$-axis, each cross-section perpendicular to the axis is a disk of radius

$$
r=y=\sqrt{x}.
$$

The area of a disk is

$$
A(x)=\pi r^2 = \pi y^2 = \pi x.
$$

Hence the volume is

$$
V=\int_0^4 \pi (\sqrt{x})^2\,dx
=\pi\int_0^4 x\,dx.
$$

### 2. Compute the volume

$$
V=\pi\left[\frac{x^2}{2}\right]_0^4
=\pi\left(\frac{16}{2}\right)
=8\pi.
$$

So,

$$
\boxed{V=8\pi}.
$$

### 3. Why the factor $\pi y^2$ appears

Each cross-section is a disk whose radius is the distance from the axis of rotation to the curve. For a point on the graph, that radius is $y$. The area of a circle is

$$
A=\pi r^2=
\pi y^2.
$$

Therefore, the volume is found by integrating the cross-sectional area over the interval of $x$ values:

$$
V=\int \pi y^2\,dx.
$$

This is the disk method.
