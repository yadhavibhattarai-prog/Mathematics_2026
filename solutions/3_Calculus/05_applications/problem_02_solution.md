## Question

### Problem 2. Maximum Area of a Rectangle

A rectangle has perimeter $40$.

1. Write its area as a function of the length of one side.
2. Determine the domain of this function resulting from the geometry of the problem.
3. Find the dimensions that give the maximum area.
4. Justify that the point found actually gives a maximum.

## Solution

Let one side have length $x$, and let the adjacent side have length $y$.

The perimeter condition gives:

$$
2x+2y=40.
$$

So,

$$
y=20-x.
$$

### 1. Area as a function of one side

The area is

$$
A(x)=xy=x(20-x)=20x-x^2.
$$

So the area function is

$$
A(x)=20x-x^2.
$$

### 2. Domain

Since both side lengths must be positive,

$$
x>0,\qquad 20-x>0,
$$

so

$$
0<x<20.
$$

Thus the domain is

$$
(0,20).
$$

### 3. Dimensions for maximum area

Differentiate:

$$
A'(x)=20-2x.
$$

Set the derivative equal to zero:

$$
20-2x=0\quad\Rightarrow\quad x=10.
$$

Then

$$
y=20-10=10.
$$

So the rectangle is a square with side length $10$.

The maximum area is

$$
A(10)=10\cdot10=100.
$$

### 4. Why this is a maximum

The second derivative is

$$
A''(x)=-2<0.
$$

Since the second derivative is negative for all $x$, the function is concave down everywhere; therefore the critical point at $x=10$ gives a maximum.

So the rectangle with dimensions $10\times10$ maximizes the area.
