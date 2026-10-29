# Exercise 10. Continuity of a Piecewise Function

Find $a$ so that

$$
f(x)=
\begin{cases}
ax+1,&x<2, \\
x^2-1,&x\ge2
\end{cases}
$$

is continuous at $x=2$. Explicitly compare the left-hand limit, right-hand limit, and function value.

> **Why this exercise:** organizes the definition of continuity as agreement among three quantities.

## Solution

### 1. Definition of Continuity at $x = 2$

A function $f$ is continuous at the point $x_0 = 2$ if and only if three conditions are simultaneously satisfied:

1. The function is defined at $x_0$, so $f(2)$ exists.
2. The limit of $f(x)$ as $x \to 2$ exists, which means the left-hand and right-hand limits exist and are equal:

$$
\lim_{x\to2^-} f(x) = \lim_{x\to2^+} f(x)
$$

3. The two-sided limit equals the function value:

$$
\lim_{x\to2} f(x) = f(2)
$$

Combining these, continuity at $x = 2$ requires the mutual equality of three quantities:

$$
\lim_{x\to2^-} f(x) = \lim_{x\to2^+} f(x) = f(2)
$$

---

### 2. Computation of the Three Quantities

#### 1. Function Value at $x = 2$
For $x \ge 2$, the function rule is $f(x) = x^2 - 1$. Substituting $x = 2$:

$$
f(2) = 2^2 - 1 = 4 - 1 = 3
$$

#### 2. Right-Hand Limit ($x \to 2^+$)
When $x$ approaches $2$ from the right ($x > 2$), the function rule is $f(x) = x^2 - 1$:

$$
\lim_{x\to2^+} f(x) = \lim_{x\to2^+} (x^2 - 1) = 2^2 - 1 = 3
$$

Notice that the right-hand limit automatically matches the function value ($f(2) = 3$), confirming that $f$ is right-continuous at $x = 2$ for every choice of $a$.

#### 3. Left-Hand Limit ($x \to 2^-$)
When $x$ approaches $2$ from the left ($x < 2$), the function rule is $f(x) = ax + 1$:

$$
\lim_{x\to2^-} f(x) = \lim_{x\to2^-} (ax + 1) = a(2) + 1 = 2a + 1
$$

---

### 3. Determining the Parameter $a$

For $f(x)$ to be continuous at $x = 2$, the left-hand limit must equal the common value of the right-hand limit and function value:

$$
\lim_{x\to2^-} f(x) = f(2)
$$

$$
2a + 1 = 3
$$

Solving this linear equation for $a$:

$$
2a = 3 - 1 = 2 \implies a = 1
$$

---

### 4. Conclusion and Verification

When $a = 1$:
- Left-hand limit: $\lim_{x\to2^-} (x + 1) = 3$
- Right-hand limit: $\lim_{x\to2^+} (x^2 - 1) = 3$
- Function value: $f(2) = 3$

All three quantities coincide at the value $3$. Thus, the piecewise function

$$
f(x)=
\begin{cases}
x+1, & x<2, \\
x^2-1, & x\ge2
\end{cases}
$$

is continuous at $x = 2$ if and only if $a = 1$.

