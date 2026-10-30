# Problem 11. A Parameter and the Number of Extrema

For

$$
f_a(x)=x^3-3ax
$$

depending on $a$, determine the number of critical points and their character. Separate the parameter cases and justify why the structure of the graph changes.

> **Why this problem:** it teaches how to analyze an entire family of functions instead of a single example.

## Solution

### 1. Computation of the Derivative

The family of functions is $f_a(x) = x^3 - 3ax$ defined for all $x \in \mathbb{R}$ with parameter $a \in \mathbb{R}$.

Compute the first derivative with respect to $x$:

$$
f_a'(x) = \frac{d}{dx}(x^3 - 3ax) = 3x^2 - 3a = 3(x^2 - a)
$$

The critical points are the real solutions to $f_a'(x) = 0$:

$$
x^2 = a
$$

The nature and number of critical points depend directly on the sign of the parameter $a$.

---

### 2. Analysis of the Parameter Cases

#### Case 1: $a > 0$
When $a > 0$, the equation $x^2 = a$ has two distinct real roots:

$$
x_1 = -\sqrt{a}, \qquad x_2 = \sqrt{a}
$$

The derivative factors as:

$$
f_a'(x) = 3(x + \sqrt{a})(x - \sqrt{a})
$$

- **Sign of $f_a'(x)$:**
  - For $x \in (-\infty, -\sqrt{a})$: $f_a'(x) > 0 \implies f_a$ is strictly increasing.
  - For $x \in (-\sqrt{a}, \sqrt{a})$: $f_a'(x) < 0 \implies f_a$ is strictly decreasing.
  - For $x \in (\sqrt{a}, \infty)$: $f_a'(x) > 0 \implies f_a$ is strictly increasing.

- **Local Extrema:**
  - At $x_1 = -\sqrt{a}$, $f_a'$ changes from positive to negative: **local maximum**.
    The maximum value is

$$
f_a(-\sqrt{a}) = (-\sqrt{a})^3 - 3a(-\sqrt{a}) = -a\sqrt{a} + 3a\sqrt{a} = 2a\sqrt{a} > 0
$$

  - At $x_2 = \sqrt{a}$, $f_a'$ changes from negative to positive: **local minimum**.
    The minimum value is

$$
f_a(\sqrt{a}) = (\sqrt{a})^3 - 3a(\sqrt{a}) = a\sqrt{a} - 3a\sqrt{a} = -2a\sqrt{a} < 0
$$

Conclusion for $a > 0$: **2 critical points**, which correspond to **2 local extrema** (one local maximum and one local minimum).

---

#### Case 2: $a = 0$
When $a = 0$, the function reduces to the basic cubic monomial:

$$
f_0(x) = x^3
$$

The derivative is

$$
f_0'(x) = 3x^2
$$

The equation $f_0'(x) = 0$ yields a single double root:

$$
x = 0
$$

- **Sign of $f_0'(x)$:**
  $3x^2 > 0$ for all $x \neq 0$. The derivative does not change sign across $x = 0$.
- **Character of the Point:**
  The function is strictly increasing on the entire real line $\mathbb{R}$.
  At $x = 0$, the tangent line is horizontal ($f_0'(0) = 0$), but this point is an **inflection point**, not a local extremum.

Conclusion for $a = 0$: **1 critical point**, which corresponds to **0 local extrema**.

---

#### Case 3: $a < 0$
When $a < 0$, let $a = -|a|$. The derivative becomes

$$
f_a'(x) = 3(x^2 - a) = 3(x^2 + |a|)
$$

Since $x^2 \ge 0$ and $|a| > 0$, the sum $x^2 + |a| > 0$ for every real number $x$.
Thus:

$$
f_a'(x) \ge 3|a| > 0 \quad (x \in \mathbb{R})
$$

- The equation $f_a'(x) = 0$ has **no real solutions**.
- The function $f_a(x)$ is strictly increasing on all of $\mathbb{R}$ with a strictly positive derivative everywhere (no horizontal tangents).

Conclusion for $a < 0$: **0 critical points** and **0 local extrema**.

---

### 3. Summary of Results

| Parameter | Number of Critical Points | Critical Points | Number of Local Extrema | Character |
|:---:|:---:|:---:|:---:|:---:|
| $a > 0$ | $2$ | $x = \pm\sqrt{a}$ | $2$ | Max at $-\sqrt{a}$, Min at $\sqrt{a}$ |
| $a = 0$ | $1$ | $x = 0$ | $0$ | Horizontal inflection point |
| $a < 0$ | $0$ | None | $0$ | Strictly increasing everywhere |

---

### 4. Why the Structure of the Graph Changes

The structural qualitative change at $a = 0$ is a classic **bifurcation** in dynamical systems and calculus:

1. **Shift of the Derivative's Parabola:**
   The derivative $f_a'(x) = 3x^2 - 3a$ is an upward parabola with vertex at $(0, -3a)$.
   - When $a < 0$, the vertex $(0, 3|a|)$ lies strictly above the $x$-axis, so $f_a'(x)$ never touches zero.
   - As $a$ increases to $0$, the parabola sinks until its vertex touches the $x$-axis at $(0, 0)$.
   - When $a > 0$, the vertex sinks below the $x$-axis to $(0, -3a)$, causing the parabola to cross the $x$-axis at two symmetric points $\pm\sqrt{a}$.
2. **Topological Transformation of the Curve:**
   For $a \le 0$, the function is strictly monotonic with a one-to-one mapping $\mathbb{R} \to \mathbb{R}$. As $a$ crosses zero into positive values, the graph develops an "S-bend" or wave, folding the curve to create a local peak and a local valley.

