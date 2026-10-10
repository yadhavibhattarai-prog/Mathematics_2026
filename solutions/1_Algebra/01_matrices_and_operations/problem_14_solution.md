# Exercise 14. Rotation Matrices and Angle Addition

## Given

The rotation matrix for an angle $\theta$ is

$$
R(\theta)=
\begin{pmatrix}
\cos\theta & -\sin\theta\\
\sin\theta & \cos\theta
\end{pmatrix}
$$

We want to prove that

$$
R(\alpha)R(\beta)=R(\alpha+\beta)
$$

## Step 1: Write the two rotation matrices

$$
R(\alpha)=
\begin{pmatrix}
\cos\alpha & -\sin\alpha\\
\sin\alpha & \cos\alpha
\end{pmatrix}
$$

$$
R(\beta)=
\begin{pmatrix}
\cos\beta & -\sin\beta\\
\sin\beta & \cos\beta
\end{pmatrix}
$$

## Step 2: Multiply the matrices

Using the matrix multiplication formula

$$
\begin{pmatrix}
a & b\\
c & d
\end{pmatrix}
\begin{pmatrix}
e & f\\
g & h
\end{pmatrix}
=
\begin{pmatrix}
ae+bg & af+bh\\
ce+dg & cf+dh
\end{pmatrix}
$$

we obtain

$$
R(\alpha)R(\beta)=
\begin{pmatrix}
\cos\alpha\cos\beta-\sin\alpha\sin\beta
&
-\cos\alpha\sin\beta-\sin\alpha\cos\beta
\\
\sin\alpha\cos\beta+\cos\alpha\sin\beta
&
-\sin\alpha(-\sin\beta)+\cos\alpha\cos\beta
\end{pmatrix}
$$

Simplifying the bottom-right entry gives

$$
R(\alpha)R(\beta)=
\begin{pmatrix}
\cos\alpha\cos\beta-\sin\alpha\sin\beta
&
-(\cos\alpha\sin\beta+\sin\alpha\cos\beta)
\\
\sin\alpha\cos\beta+\cos\alpha\sin\beta
&
\cos\alpha\cos\beta-\sin\alpha\sin\beta
\end{pmatrix}
$$

## Step 3: Apply the trigonometric addition formulae

The necessary trigonometric identities are

**Cosine addition formula:**

$$
\cos(\alpha+\beta)
=
\cos\alpha\cos\beta-\sin\alpha\sin\beta
$$

**Sine addition formula:**

$$
\sin(\alpha+\beta)
=
\sin\alpha\cos\beta+\cos\alpha\sin\beta
$$

Substituting these identities into the matrix gives

$$
R(\alpha)R(\beta)=
\begin{pmatrix}
\cos(\alpha+\beta) & -\sin(\alpha+\beta)\\
\sin(\alpha+\beta) & \cos(\alpha+\beta)
\end{pmatrix}
$$

This is exactly the rotation matrix for the angle $\alpha+\beta$.

Therefore,

$$
\boxed{R(\alpha)R(\beta)=R(\alpha+\beta)}
$$

## Step 4: Geometric interpretation

A rotation matrix rotates a vector around the origin.

- First, $R(\beta)$ rotates the vector by angle $\beta$.
- Then, $R(\alpha)$ rotates the resulting vector by angle $\alpha$.
- Since both rotations are around the same origin, the total rotation is $\alpha+\beta$.

Thus, applying two rotations is equivalent to applying one rotation by the sum of their angles.

## Step 5: Plot the rotations using Python

The following code illustrates two successive rotations of a vector.

````python
import numpy as np
import matplotlib.pyplot as plt

def rotation_matrix(theta):
    return np.array([
        [np.cos(theta), -np.sin(theta)],
        [np.sin(theta),  np.cos(theta)]
    ])

# Initial vector
v = np.array([1, 0])

# Rotation angles in degrees
alpha = 30
beta = 45

# Convert degrees to radians
alpha_rad = np.radians(alpha)
beta_rad = np.radians(beta)

# Apply the rotations
v_beta = rotation_matrix(beta_rad) @ v
v_alpha_beta = rotation_matrix(alpha_rad) @ v_beta

# Direct rotation by alpha + beta
v_direct = rotation_matrix(alpha_rad + beta_rad) @ v

# Plot the vectors
plt.figure(figsize=(7, 7))
plt.axhline(0, color="gray", linewidth=0.8)
plt.axvline(0, color="gray", linewidth=0.8)

plt.quiver(0, 0, v[0], v[1],
           angles="xy", scale_units="xy", scale=1,
           label="Initial vector")

plt.quiver(0, 0, v_beta[0], v_beta[1],
           angles="xy", scale_units="xy", scale=1,
           label="After beta = 45°")

plt.quiver(0, 0, v_alpha_beta[0], v_alpha_beta[1],
           angles="xy", scale_units="xy", scale=1,
           label="After beta then alpha")

plt.quiver(0, 0, v_direct[0], v_direct[1],
           angles="xy", scale_units="xy", scale=1,
           label="Direct rotation by 75°")

plt.xlim(-1.2, 1.2)
plt.ylim(-1.2, 1.2)
plt.gca().set_aspect("equal")
plt.grid(True)
plt.xlabel("x")
plt.ylabel("y")
plt.title("Composition of Rotation Matrices")
plt.legend()
plt.show()

# Verify that both methods give the same result
print("Successive rotations:", v_alpha_beta)
print("Direct rotation:", v_direct)
print("Equal:", np.allclose(v_alpha_beta, v_direct))
