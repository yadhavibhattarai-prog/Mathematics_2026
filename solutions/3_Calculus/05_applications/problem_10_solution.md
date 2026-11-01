## Question

### Problem 10. A Cable Through Water and Land

Point $A$ lies on one bank of a river of width $100$ m, and point $B$ lies on the other bank, $500$ m along the bank from the point directly opposite $A$.

The cost per meter of cable underwater is twice the cost per meter of cable on land.

Build a cost function depending on the point where the cable comes out of the water, determine the domain, and find the solution that minimizes the cost.

## Solution

Let the cable leave the water at a point $P$ on the opposite bank, and let the distance from the point directly opposite $A$ to $P$ be $x$ meters.

Then:

- the distance from $P$ to $B$ along land is $500-x$,
- the underwater path is the straight segment from $A$ to $P$, whose length is

$$
\sqrt{x^2+100^2}=
\sqrt{x^2+10000}.
$$

Let the cost per meter on land be $k$. Then the underwater cost is $2k$ per meter.

### 1. Cost function

The total cost is

$$
C(x)=2k\sqrt{x^2+10000}+k(500-x),
\qquad 0\le x\le500.
$$

Since $k$ is a constant factor, we may minimize

$$
C(x)=2\sqrt{x^2+10000}+500-x.
$$

(We divide by $k$ because it does not affect the minimizing point.)

### 2. Domain

The point $P$ must lie between the point directly opposite $A$ and the point $B$ along the bank, so

$$
0\le x\le500.
$$

### 3. Differentiate and optimize

Differentiate:

$$
C'(x)=\frac{2x}{\sqrt{x^2+10000}}-1.
$$

Set equal to zero:

$$
\frac{2x}{\sqrt{x^2+10000}}-1=0.
$$

So,

$$
\frac{2x}{\sqrt{x^2+10000}}=1.
$$

This gives

$$
2x=\sqrt{x^2+10000}.
$$

Square both sides:

$$
4x^2=x^2+10000.
$$

Hence,

$$
3x^2=10000,
$$

so

$$
x=\frac{100}{\sqrt3} \approx 57.7\text{ m}.
$$

### 4. Check that it is a minimum

The second derivative is

$$
C''(x)=\frac{20000}{(x^2+10000)^{3/2}}>0,
$$

so the cost function is convex and the critical point gives the minimum.

Therefore, the minimum cost occurs when the cable enters the water at a point

$$
\boxed{x=\frac{100}{\sqrt3}\text{ m}} 
$$

from the point directly opposite $A$.

So the cable should come out of the water about $57.7$ m downstream from the point directly opposite $A$.
