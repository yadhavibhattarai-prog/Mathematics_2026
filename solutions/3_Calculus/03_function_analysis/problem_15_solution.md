# Problem 15. Find the Error in the Monotonicity Analysis

For the function

$$
f(x)=x^3-3x
$$

the derivative was correctly computed as

$$
f'(x)=3(x-1)(x+1).
$$

However, a student wrote the following conclusion:

> The derivative is positive between its zeros and negative outside them. Therefore, the function is decreasing on $(-\infty,-1)\cup(1,\infty)$, increasing on $(-1,1)$, has a local minimum at $x=-1$, and a local maximum at $x=1$.

1. Without differentiating again, explain why merely identifying the zeros of the derivative does not justify the stated sign chart, and find the error in the student's reasoning.
2. Construct the correct sign chart for $f'(x)$.
3. Give the correct intervals of monotonicity and the character of the extrema.
4. In each of the three intervals, choose one simple test point and show that the sign of the derivative confirms your classification.

> **Why this problem:** it teaches how to diagnose an error in a completed argument and shows that a correct derivative formula is not enough if its sign is interpreted incorrectly.

## Solution

### 1. Diagnosis of the Student's Errors

The student's argument contains two fundamental errors:

1. **Inverted Sign Rule for a Quadratic Polynomial:**
   The zeros of $f'(x) = 3(x^2 - 1)$ are correctly $x = -1$ and $x = 1$. However, knowing the zeros of a function only identifies the boundary points where the sign could potentially change; it does not indicate which regions are positive and which are negative.
   The derivative is a quadratic function with a **positive leading coefficient** ($a = 3 > 0$):

$$
f'(x) = 3x^2 - 3
$$

   The graph of $y = 3x^2 - 3$ is an upward-opening parabola with vertex at $(0, -3)$.
   - Between its roots (for $-1 < x < 1$), the parabola dips **below** the $x$-axis, so $f'(x) < 0$.
   - Outside its roots (for $x < -1$ and $x > 1$), the parabola rises **above** the $x$-axis, so $f'(x) > 0$.
   The student asserted the exact opposite ("positive between its zeros and negative outside them"), completely inverting the sign chart. Consequently, all deduced monotonicity intervals and extrema classifications were inverted.

2. **Improper Notation for Monotonicity:**
   The student wrote that the function is decreasing on $(-\infty, -1) \cup (1, \infty)$.
   Monotonicity is a property defined on connected intervals, not on disjoint unions. Even when a derivative is negative on two disjoint intervals, writing a union symbol is mathematically incorrect because the function value may jump upwards across the gap.

---

### 2. Correct Sign Chart for $f'(x)$

Factor the derivative:

$$
f'(x) = 3(x - 1)(x + 1)
$$

The zeros partition the real line into three open intervals:

| Interval | $(-\infty, -1)$ | $x = -1$ | $(-1, 1)$ | $x = 1$ | $(1, \infty)$ |
|:---:|:---:|:---:|:---:|:---:|:---:|
| Factor $3$ | $+$ | $+$ | $+$ | $+$ | $+$ |
| Factor $x + 1$ | $-$ | $0$ | $+$ | $+$ | $+$ |
| Factor $x - 1$ | $-$ | $-$ | $-$ | $0$ | $+$ |
| Product $f'(x)$ | $\mathbf{+}$ | $\mathbf{0}$ | $\mathbf{-}$ | $\mathbf{0}$ | $\mathbf{+}$ |

- On $(-\infty, -1)$: $f'(x) > 0$.
- On $(-1, 1)$: $f'(x) < 0$.
- On $(1, \infty)$: $f'(x) > 0$.

---

### 3. Correct Monotonicity and Character of Extrema

#### Intervals of Monotonicity
- The function $f$ is strictly **increasing** on $(-\infty, -1]$.
- The function $f$ is strictly **decreasing** on $[-1, 1]$.
- The function $f$ is strictly **increasing** on $[1, \infty)$.

#### Character and Values of Extrema
- **At $x = -1$:**
  The derivative changes sign from positive ($+$) to negative ($-$) as $x$ increases through $-1$.
  Therefore, $x = -1$ is a **local maximum** (contrary to the student's claim of a minimum).
  The maximum value is

$$
f(-1) = (-1)^3 - 3(-1) = -1 + 3 = 2
$$

  Local maximum point: $(-1, 2)$.

- **At $x = 1$:**
  The derivative changes sign from negative ($-$) to positive ($+$) as $x$ increases through $1$.
  Therefore, $x = 1$ is a **local minimum** (contrary to the student's claim of a maximum).
  The minimum value is

$$
f(1) = 1^3 - 3(1) = 1 - 3 = -2
$$

  Local minimum point: $(1, -2)$.

---

### 4. Verification Using Test Points

In each of the three intervals, choose one simple test value for $x$ and evaluate $f'(x) = 3(x^2 - 1)$:

1. **Interval $(-\infty, -1)$ — Choose test point $x = -2$:**

$$
f'(-2) = 3\left((-2)^2 - 1\right) = 3(4 - 1) = 3(3) = 9 > 0
$$

   Since $f'(-2) = 9 > 0$, the derivative is positive, confirming that $f$ is increasing on $(-\infty, -1]$.

2. **Interval $(-1, 1)$ — Choose test point $x = 0$:**

$$
f'(0) = 3\left(0^2 - 1\right) = 3(-1) = -3 < 0
$$

   Since $f'(0) = -3 < 0$, the derivative is negative, confirming that $f$ is decreasing on $[-1, 1]$.

3. **Interval $(1, \infty)$ — Choose test point $x = 2$:**

$$
f'(2) = 3\left(2^2 - 1\right) = 3(4 - 1) = 3(3) = 9 > 0
$$

   Since $f'(2) = 9 > 0$, the derivative is positive, confirming that $f$ is increasing on $[1, \infty)$.

The test points confirm that the student's sign claims were completely inverted.

