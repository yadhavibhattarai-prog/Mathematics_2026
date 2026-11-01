## Question

### Problem 5. Distance from Velocity

The velocity of a car during the first five seconds is described by the function

$$
v(t)=4t+2\quad [\mathrm{m/s}].
$$

Compute the distance traveled and explain why the integral of velocity gives the change in position.

Then answer what would have to be changed in the reasoning if the velocity also took negative values.

## Solution

### 1. Distance traveled in the first five seconds

Since velocity is the rate of change of position, the total change in position over the time interval $[0,5]$ is

$$
\int_0^5 v(t)\,dt.
$$

So

$$
\int_0^5 (4t+2)\,dt = \left[2t^2+2t\right]_0^5.
$$

Evaluate:

$$
2(25)+2(5)=50+10=60.
$$

Thus the car travels

$$
\boxed{60\text{ m}}.
$$

### 2. Why the integral of velocity gives change in position

Velocity is the derivative of position:

$$
\frac{ds}{dt}=v(t).
$$

Therefore,

$$
 s(5)-s(0)=\int_0^5 v(t)\,dt.
$$

This means the integral of velocity accumulates the total change in position over time.

### 3. If velocity could be negative

If the velocity took negative values, then the integral would still give the displacement (signed change in position), not the total distance. Negative values contribute negatively to the integral.

To get actual distance traveled, we must integrate the absolute value of the velocity:

$$
\text{distance} = \int_a^b |v(t)|\,dt.
$$

This requires splitting the interval at the times when $v(t)=0$, so that each part of the motion is handled with its correct sign.
