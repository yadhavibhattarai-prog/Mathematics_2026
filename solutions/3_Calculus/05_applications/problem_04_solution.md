## Question

### Problem 4. Area Between Curves

Find the area of the region bounded by the graphs

$$
y=x
$$

and

$$
y=x^2.
$$

First find the intersection points and justify which function is greater on the relevant interval.

## Solution

### 1. Intersection points

Set the two curves equal:

$$
x=x^2.
$$

So

$$
x^2-x=0
\quad\Rightarrow\quad
x(x-1)=0.
$$

Hence the intersection points are at

$$
x=0\quad\text{and}\quad x=1.
$$

### 2. Which function is greater?

On the interval $[0,1]$, take a test point such as $x=\tfrac12$:

$$
x=\frac12,
\qquad
x^2=\frac14.
$$

Since

$$
\frac12 > \frac14,
$$

we have

$$
x > x^2\quad \text{for } 0<x<1.
$$

Thus, on $[0,1]$, the line $y=x$ lies above the parabola $y=x^2$.

### 3. Area between the curves

The required area is

$$
A=\int_0^1 (x-x^2)\,dx.
$$

Compute:

$$
A=\left[\frac{x^2}{2}-\frac{x^3}{3}\right]_0^1
=\frac12-\frac13
=\frac16.
$$

Therefore,

$$
\boxed{A=\frac16}.
$$
