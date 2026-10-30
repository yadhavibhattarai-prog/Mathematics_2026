# Problem 7. A Trigonometric Function

On $[0,2\pi]$, find the intervals of monotonicity and the extrema of

$$
f(x)=\sin x+\cos x.
$$

Include the endpoints of the interval and compare the function values at the critical points and at the endpoints.

> **Why this problem:** it practices the analysis of a periodic function on a bounded interval.

## Solution

### 1. Derivative and Critical Points on $[0, 2\pi]$

The function is defined and differentiable everywhere on the closed interval $[0, 2\pi]$.
Differentiate $f(x) = \sin x + \cos x$:

$$
f'(x) = \cos x - \sin x
$$

Set $f'(x) = 0$ to find the critical points in $(0, 2\pi)$:

$$
\cos x - \sin x = 0 \iff \sin x = \cos x
$$

Since $\cos x = 0$ implies $\sin x = \pm 1 \neq 0$, we can divide by $\cos x$:

$$
\tan x = 1
$$

In the interval $[0, 2\pi]$, the equation $\tan x = 1$ has two solutions:

$$
x_1 = \frac{\pi}{4}, \qquad x_2 = \frac{5\pi}{4}
$$

---

### 2. Sign of the Derivative and Intervals of Monotonicity

Using the harmonic addition identity:

$$
f'(x) = \cos x - \sin x = \sqrt{2}\cos\left(x + \frac{\pi}{4}\right)
$$

Determine the sign of $f'(x)$ on each subinterval of $[0, 2\pi]$:

- **On $[0, \pi/4)$:**
  Here $x + \frac{\pi}{4} \in \left[\frac{\pi}{4}, \frac{\pi}{2}\right)$, so the cosine is strictly positive:

$$
f'(x) > 0
$$

  The function $f$ is strictly increasing on $\left[0, \frac{\pi}{4}\right]$.

- **On $(\pi/4, 5\pi/4)$:**
  Here $x + \frac{\pi}{4} \in \left(\frac{\pi}{2}, \frac{3\pi}{2}\right)$, where the cosine is strictly negative:

$$
f'(x) < 0
$$

  The function $f$ is strictly decreasing on $\left[\frac{\pi}{4}, \frac{5\pi}{4}\right]$.

- **On $(5\pi/4, 2\pi]$:**
  Here $x + \frac{\pi}{4} \in \left(\frac{3\pi}{2}, \frac{9\pi}{4}\right]$, where the cosine is strictly positive:

$$
f'(x) > 0
$$

  The function $f$ is strictly increasing on $\left[\frac{5\pi}{4}, 2\pi\right]$.

---

### 3. Function Values at Critical Points and Endpoints

Evaluate $f(x)$ at all four candidate points for extrema:

1. **Left Endpoint ($x = 0$):**

$$
f(0) = \sin(0) + \cos(0) = 0 + 1 = 1
$$

2. **First Critical Point ($x = \pi/4$):**

$$
f\left(\frac{\pi}{4}\right) = \sin\left(\frac{\pi}{4}\right) + \cos\left(\frac{\pi}{4}\right) = \frac{\sqrt{2}}{2} + \frac{\sqrt{2}}{2} = \sqrt{2} \approx 1.4142
$$

3. **Second Critical Point ($x = 5\pi/4$):**

$$
f\left(\frac{5\pi}{4}\right) = \sin\left(\frac{5\pi}{4}\right) + \cos\left(\frac{5\pi}{4}\right) = -\frac{\sqrt{2}}{2} - \frac{\sqrt{2}}{2} = -\sqrt{2} \approx -1.4142
$$

4. **Right Endpoint ($x = 2\pi$):**

$$
f(2\pi) = \sin(2\pi) + \cos(2\pi) = 0 + 1 = 1
$$

---

### 4. Comparison and Classification of Extrema

Ordering the values obtained:

$$
-\sqrt{2} < 1 < \sqrt{2}
$$

- **Global Maximum:**
  The largest value is $\sqrt{2}$, attained at the interior critical point $x = \frac{\pi}{4}$.
  Because $f'$ changes from positive to negative, it is both a local maximum and the **global maximum** on $[0, 2\pi]$.
- **Global Minimum:**
  The smallest value is $-\sqrt{2}$, attained at the interior critical point $x = \frac{5\pi}{4}$.
  Because $f'$ changes from negative to positive, it is both a local minimum and the **global minimum** on $[0, 2\pi]$.
- **Endpoints:**
  - At the left boundary $x = 0$, $f$ starts at $1$ and immediately increases, so $x = 0$ is a **boundary local minimum**.
  - At the right boundary $x = 2\pi$, $f$ reaches $1$ from below by increasing, so $x = 2\pi$ is a **boundary local maximum**.
  Neither endpoint attains an absolute extremum, as $-\sqrt{2} < 1 < \sqrt{2}$.

