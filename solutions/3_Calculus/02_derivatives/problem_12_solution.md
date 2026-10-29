# Problem 12. Several Rules at Once

For

$$
f(x)=(x^2+1)^3e^x
$$

compute the derivative. Before calculating, write down a plan: which rule applies to the whole expression and which rule applies to one of its factors. Finally, organize the result by factoring out common factors.

> **Why this problem:** it practices the order of decisions when combining familiar differentiation rules.

## Solution

### 1. Plan of Calculation

The expression $f(x) = (x^2+1)^3 e^x$ combines multiple structural operations:

1. **Global Rule (applies to the whole expression):**
   The primary structure is the product of two functions:

$$
f(x) = u(x) \cdot v(x)
$$

   where $u(x) = (x^2+1)^3$ and $v(x) = e^x$.
   Therefore, the **Product Rule** governs the overall differentiation:

$$
f'(x) = u'(x)v(x) + u(x)v'(x)
$$

2. **Factor Rule (applies to the first factor $u(x)$):**
   The factor $u(x) = (x^2+1)^3$ is not a simple power of $x$; it is a composite function of an outer cube and an inner polynomial $w(x) = x^2 + 1$.
   Therefore, the **Chain Rule** must be used to differentiate $u(x)$:

$$
u'(x) = 3(x^2+1)^2 \cdot \frac{d}{dx}(x^2+1)
$$

3. **Second Factor:**
   The factor $v(x) = e^x$ is the standard natural exponential function, whose derivative is itself: $v'(x) = e^x$.

---

### 2. Executing the Derivatives of the Individual Factors

- **Differentiating $u(x) = (x^2+1)^3$:**

$$
u'(x) = 3(x^2+1)^2 \cdot (2x) = 6x(x^2+1)^2
$$

- **Differentiating $v(x) = e^x$:**

$$
v'(x) = e^x
$$

---

### 3. Assembling the Product Rule

Substitute $u, u', v, v'$ into the product rule formula:

$$
f'(x) = \left[6x(x^2+1)^2\right] e^x + \left[(x^2+1)^3\right] e^x
$$

---

### 4. Organizing and Factoring Out Common Factors

Identify the greatest common factor shared by both terms:
- Both terms contain the power $(x^2+1)^2$.
- Both terms contain the exponential factor $e^x$.

Factor out $(x^2+1)^2 e^x$:

$$
f'(x) = (x^2+1)^2 e^x \left[6x + (x^2+1)\right]
$$

Collect and arrange the terms inside the square bracket in descending powers:

$$
6x + x^2 + 1 = x^2 + 6x + 1
$$

The fully factored, simplified derivative is

$$
f'(x) = (x^2+6x+1)(x^2+1)^2 e^x
$$

