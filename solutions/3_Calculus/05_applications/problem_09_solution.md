## Question

### Problem 9. Minimizing the Material Used for a Can

A closed cylinder has fixed volume $V$.

1. Write the volume constraint.
2. Eliminate one of the variables.
3. Express the surface area as a function of the radius $r$.
4. Find the relation between the height $h$ and the radius $r$ for which the material usage is minimal.

Interpret the obtained relation geometrically.

## Solution

Let the radius be $r$ and the height be $h$.

### 1. Volume constraint

For a cylinder,

$$
V=\pi r^2 h.
$$

This is the fixed volume condition.

### 2. Eliminate one variable

Solve for $h$:

$$
h=\frac{V}{\pi r^2}.
$$

### 3. Surface area as a function of $r$

A closed cylinder has total surface area

$$
S=2\pi r^2+2\pi rh.
$$

Substitute $h=\frac{V}{\pi r^2}$:

$$
S(r)=2\pi r^2+2\pi r\left(\frac{V}{\pi r^2}\right)
=2\pi r^2+\frac{2V}{r}.
$$

So,

$$
\boxed{S(r)=2\pi r^2+\frac{2V}{r}}.
$$

### 4. Minimize the surface area

Differentiate:

$$
S'(r)=4\pi r-\frac{2V}{r^2}.
$$

Set the derivative equal to zero:

$$
4\pi r-\frac{2V}{r^2}=0.
$$

So,

$$
4\pi r = \frac{2V}{r^2}
\quad\Rightarrow\quad
4\pi r^3=2V
\quad\Rightarrow\quad
r^3=\frac{V}{2\pi}.
$$

Thus,

$$
\boxed{r=\left(\frac{V}{2\pi}\right)^{1/3}}.
$$

Now use the volume constraint:

$$
V=\pi r^2 h.
$$

Substitute $V=2\pi r^3$ from the condition above:

$$
2\pi r^3 = \pi r^2 h.
$$

Cancel $\pi r^2$:

$$
h=2r.
$$

Therefore, the material is minimized when

$$
\boxed{h=2r}.
$$

### Geometric interpretation

This means the optimal cylinder has height equal to the diameter of the base. In other words, the can is as tall as it is wide.

The second derivative is

$$
S''(r)=4\pi+\frac{4V}{r^3}>0,
$$

so this critical point gives a minimum.
