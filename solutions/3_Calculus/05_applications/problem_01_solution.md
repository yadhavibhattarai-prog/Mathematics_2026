## Question

### Problem 1. Motion — from Position to Velocity

The position of a point is described by

$$
s(t)=t^3-6t^2+9t+2,\qquad t\ge0.
$$

1. Determine the velocity and acceleration.
2. Find the times at which the point stops.
3. Determine on which intervals the point moves in the positive direction of the axis and on which intervals it moves in the negative direction.

## Solution

The velocity is the derivative of the position function, and acceleration is the derivative of velocity.

### 1. Velocity and acceleration

$$
v(t)=s'(t)=3t^2-12t+9.
$$

Factor the quadratic:

$$
v(t)=3(t^2-4t+3)=3(t-1)(t-3).
$$

Then

$$
a(t)=v'(t)=6t-12=6(t-2).
$$

So,

$$
v(t)=3t^2-12t+9,\qquad a(t)=6t-12.
$$

### 2. Times when the point stops

The point stops when the velocity is zero:

$$
3(t-1)(t-3)=0.
$$

Thus,

$$
t=1\quad \text{or}\quad t=3.
$$

So the point is at rest at $t=1$ and $t=3$.

### 3. Direction of motion

The sign of $v(t)$ tells us the direction of motion.

Because

$$
v(t)=3(t-1)(t-3),
$$

we test the sign on the intervals determined by $t=1$ and $t=3$:

- For $0\le t<1$: choose $t=0$,
  $$v(0)=9>0,$$
  so the point moves in the positive direction.

- For $1<t<3$: choose $t=2$,
  $$v(2)=3(1)(-1)=-3<0,$$
  so the point moves in the negative direction.

- For $t>3$: choose $t=4$,
  $$v(4)=3(3)(1)=9>0,$$
  so the point moves in the positive direction.

Therefore:

- positive direction: $[0,1)$ and $(3,\infty)$,
- negative direction: $(1,3)$.

The point changes direction at $t=1$ and $t=3$.
