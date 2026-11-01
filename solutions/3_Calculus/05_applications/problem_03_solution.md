## Question

### Problem 3. A Box Made from Cardboard

From a $30\,\mathrm{cm}\times40\,\mathrm{cm}$ sheet, squares of side length $x$ are cut from the corners and the edges are folded up to form an open box.

Write the volume as a function of $x$, determine the physically meaningful domain, and find the value of $x$ for which the volume is greatest.

## Solution

When squares of side $x$ are cut from each corner, the box has dimensions:

- length: $40-2x$,
- width: $30-2x$,
- height: $x$.

### 1. Volume function

So the volume is

$$
V(x)=x(40-2x)(30-2x).
$$

Expand:

$$
V(x)=x(1200-80x-60x+4x^2)
= x(1200-140x+4x^2)
= 4x^3-140x^2+1200x.
$$

Thus,

$$
V(x)=4x^3-140x^2+1200x.
$$

### 2. Domain

The box must have positive dimensions, so:

$$
40-2x>0,\qquad 30-2x>0,\qquad x>0.
$$

This gives

$$
x<20\quad\text{and}\quad x<15,
$$

so the physically meaningful domain is

$$
0<x<15.
$$

### 3. Maximum volume

Differentiate:

$$
V'(x)=12x^2-280x+1200.
$$

Factor out $4$:

$$
V'(x)=4(3x^2-70x+300).
$$

Set to zero:

$$
3x^2-70x+300=0.
$$

Use the quadratic formula:

$$
x=\frac{70\pm\sqrt{(-70)^2-4\cdot3\cdot300}}{2\cdot3}
=\frac{70\pm\sqrt{4900-3600}}{6}
=\frac{70\pm\sqrt{1300}}{6}.
$$

Since $\sqrt{1300}=10\sqrt{13}$,

$$
x=\frac{70\pm10\sqrt{13}}{6}
=\frac{35\pm5\sqrt{13}}{3}.
$$

The two roots are

$$
x\approx 5.66\quad \text{and}\quad x\approx 17.68.
$$

Only $x\approx 5.66$ lies in the allowed domain $(0,15)$.

### 4. Justification that this is a maximum

The second derivative is

$$
V''(x)=24x-280.
$$

At $x\approx 5.66$,

$$
V''(5.66)\approx 24(5.66)-280\approx -136<0,
$$

so this critical point gives a maximum.

Therefore, the greatest volume occurs when

$$
\boxed{x\approx 5.66\text{ cm}}.
$$
