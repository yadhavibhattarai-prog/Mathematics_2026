### Exercise 14. Rotation Matrices

The matrix for a rotation through an angle $\theta$ is

$$
R(\theta)=
\begin{pmatrix}
\cos\theta & -\sin\theta\\
\sin\theta & \cos\theta
\end{pmatrix}
$$

We need to compute $R(\alpha)R(\beta)$ and show that

$$
R(\alpha)R(\beta)=R(\alpha+\beta)
$$

using the angle-sum formulas for sine and cosine.

### Step 1: Write the Two Rotation Matrices

For angles $\alpha$ and $\beta$, we have

$$
R(\alpha)=
\begin{pmatrix}
\cos\alpha & -\sin\alpha\\
\sin\alpha & \cos\alpha
\end{pmatrix}
$$

and

$$
R(\beta)=
\begin{pmatrix}
\cos\beta & -\sin\beta\\
\sin\beta & \cos\beta
\end{pmatrix}
$$

### Step 2: Compute $R(\alpha)R(\beta)$

Multiply the two matrices:

$$
R(\alpha)R(\beta)=
\begin{pmatrix}
\cos\alpha & -\sin\alpha\\
\sin\alpha & \cos\alpha
\end{pmatrix}
\begin{pmatrix}
\cos\beta & -\sin\beta\\
\sin\beta & \cos\beta
\end{pmatrix}
$$

Using row-by-column multiplication, calculate each entry.

**Top-left entry:**

$$
\cos\alpha\cos\beta-\sin\alpha\sin\beta
$$

**Top-right entry:**

$$
-\cos\alpha\sin\beta-\sin\alpha\cos\beta
$$

**Bottom-left entry:**

$$
\sin\alpha\cos\beta+\cos\alpha\sin\beta
$$

**Bottom-right entry:**

$$
-\sin\alpha\sin\beta+\cos\alpha\cos\beta
$$

Therefore,

$$
R(\alpha)R(\beta)=
\begin{pmatrix}
\cos\alpha\cos\beta-\sin\alpha\sin\beta
&
-\cos\alpha\sin\beta-\sin\alpha\cos\beta
\\
\sin\alpha\cos\beta+\cos\alpha\sin\beta
&
\cos\alpha\cos\beta-\sin\alpha\sin\beta
\end{pmatrix}
$$

### Step 3: Apply the Angle-Sum Formulas

Recall the angle-sum formulas:

$$
\cos(\alpha+\beta)
=
\cos\alpha\cos\beta-\sin\alpha\sin\beta
$$

and

$$
\sin(\alpha+\beta)
=
\sin\alpha\cos\beta+\cos\alpha\sin\beta
$$

Using these identities, we can rewrite the top-left entry as

$$
\cos\alpha\cos\beta-\sin\alpha\sin\beta
=
\cos(\alpha+\beta)
$$

The top-right entry becomes

$$
\begin{aligned}
&-\cos\alpha\sin\beta-\sin\alpha\cos\beta\\
&=-\left(\cos\alpha\sin\beta+\sin\alpha\cos\beta\right)\\
&=-\sin(\alpha+\beta)
\end{aligned}
$$

The bottom-left entry becomes

$$
\sin\alpha\cos\beta+\cos\alpha\sin\beta
=
\sin(\alpha+\beta)
$$

The bottom-right entry becomes

$$
\cos\alpha\cos\beta-\sin\alpha\sin\beta
=
\cos(\alpha+\beta)
$$

Substituting these expressions into the product gives

$$
R(\alpha)R(\beta)=
\begin{pmatrix}
\cos(\alpha+\beta) & -\sin(\alpha+\beta)\\
\sin(\alpha+\beta) & \cos(\alpha+\beta)
\end{pmatrix}
$$

By the definition of a rotation matrix, this is exactly $R(\alpha+\beta)$.

Therefore,

$$
\boxed{R(\alpha)R(\beta)=R(\alpha+\beta)}
$$

### Step 4: Geometric Explanation

A rotation matrix turns a vector around the origin by a specified angle.

When we multiply $R(\alpha)R(\beta)$, the transformation on the right is applied
