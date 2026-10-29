# Exercise 11. Two Similar Surfaces

Compare

$$
x^2+y^2-z^2=1
$$

and

$$
x^2+y^2-z^2=-1.
$$

For several values $z=c$, check whether the cross-section exists and what its radius is. Based on this, describe qualitatively the difference between the surfaces and make sketches.

> **Why this exercise:** teaches how to recognize the shape of a surface from cross-sections instead of from a memorized catalog of names.

## Solution

### 1. Analysis of the First Surface: $x^2 + y^2 - z^2 = 1$

Rewrite the equation by setting $z = c$:

$$
x^2 + y^2 = 1 + c^2
$$

Since $c^2 \ge 0$ for all real numbers $c$, the right-hand side satisfies $1 + c^2 \ge 1 > 0$ for every $c \in \mathbb{R}$.

Therefore, every horizontal cross-section $z = c$ is a circle centered on the $z$-axis with radius

$$
R_1(c) = \sqrt{1 + c^2}
$$

#### Radii for Specific Values of $c$

| $c$ | Cross-Section Equation | Exists? | Radius $R_1(c)$ |
|:---:|:---:|:---:|:---:|
| $0$ | $x^2 + y^2 = 1$ | Yes | $1$ |
| $\pm 1$ | $x^2 + y^2 = 2$ | Yes | $\sqrt{2} \approx 1.414$ |
| $\pm 2$ | $x^2 + y^2 = 5$ | Yes | $\sqrt{5} \approx 2.236$ |
| $\pm 3$ | $x^2 + y^2 = 10$ | Yes | $\sqrt{10} \approx 3.162$ |

- The minimum radius occurs at the equatorial plane $z = 0$, where $R_1(0) = 1$ (the throat or waist circle).
- As $|c| \to \infty$, the radius grows without bound.
- The surface is a single continuous, connected piece: a **hyperboloid of one sheet** (hyperboloid of revolution of one sheet).

---

### 2. Analysis of the Second Surface: $x^2 + y^2 - z^2 = -1$

Rewrite the equation by setting $z = c$:

$$
x^2 + y^2 = c^2 - 1
$$

For real coordinates $(x, y)$, the sum $x^2 + y^2$ must be non-negative ($x^2 + y^2 \ge 0$). Thus, real cross-sections exist if and only if

$$
c^2 - 1 \ge 0 \iff c^2 \ge 1 \iff |c| \ge 1
$$

When this condition is satisfied, the cross-section is a circle with radius

$$
R_2(c) = \sqrt{c^2 - 1}
$$

#### Radii for Specific Values of $c$

| $c$ | Cross-Section Equation | Exists? | Radius $R_2(c)$ |
|:---:|:---:|:---:|:---:|
| $0$ | $x^2 + y^2 = -1$ | No (empty set) | Does not exist |
| $\pm 0.5$ | $x^2 + y^2 = -0.75$ | No (empty set) | Does not exist |
| $\pm 1$ | $x^2 + y^2 = 0$ | Yes (single point) | $0$ (vertices $(0, 0, \pm 1)$) |
| $\pm 2$ | $x^2 + y^2 = 3$ | Yes | $\sqrt{3} \approx 1.732$ |
| $\pm 3$ | $x^2 + y^2 = 8$ | Yes | $\sqrt{8} = 2\sqrt{2} \approx 2.828$ |

- In the entire open band $-1 < z < 1$, no points of the surface exist.
- At $z = 1$ and $z = -1$, the cross-sections degenerate to single points: the two vertices $(0, 0, 1)$ and $(0, 0, -1)$.
- For $|c| > 1$, circular cross-sections appear and widen as $|c|$ increases.
- The surface consists of two separate, disconnected cup-like sheets: a **hyperboloid of two sheets** (hyperboloid of revolution of two sheets).

---

### 3. Qualitative Comparison

- **Connectivity and Topology:**
  - $x^2 + y^2 - z^2 = 1$ is topologically connected, forming an hourglass-like tube with a central waist of radius $1$.
  - $x^2 + y^2 - z^2 = -1$ is disconnected, separated by a gap of vertical height $2$ (between $z = -1$ and $z = 1$).
- **Common Asymptotic Cone:**
  Both surfaces approach the common asymptotic circular cone
  
$$
x^2 + y^2 - z^2 = 0 \iff x^2 + y^2 = z^2
$$

  as $|z| \to \infty$. The one-sheeted hyperboloid surrounds the exterior of this cone, while the two-sheeted hyperboloid lies in the interior cavity of the upper and lower nappes of the cone.

