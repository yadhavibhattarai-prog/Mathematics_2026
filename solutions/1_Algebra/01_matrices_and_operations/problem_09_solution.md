# Chapter 9: Composing Linear Transformations

## 1. Learning goals

By the end of this chapter, you should be able to:

- interpret a matrix product as a sequence of transformations;
- determine the order in which transformations are applied;
- calculate two different compositions of scaling and rotation; and
- explain why changing the order can change the result.

## 2. The order in a matrix product

A matrix represents a linear transformation of vectors. If $A$ and $B$ are
matrices and $x$ is a vector, then

$$
ABx=A(Bx).
$$

This means that $B$ acts on $x$ first, followed by $A$. Read a product of
matrices from right to left when determining the order of transformations.

In general, matrix multiplication is not commutative: $AB$ and $BA$ need not be
equal. The following example shows how the order of a rotation and a
nonuniform scaling changes a vector.

## 3. Transformations in this example

Consider the scaling matrix

$$
S=
\begin{pmatrix}
2 & 0\\
0 & 1
\end{pmatrix}
$$

and the $90^\circ$ counterclockwise rotation matrix

$$
R=
\begin{pmatrix}
0 & -1\\
1 & 0
\end{pmatrix}.
$$

The scaling matrix doubles the horizontal coordinate and leaves the vertical
coordinate unchanged. Let the original vector be

$$
x=
\begin{pmatrix}
1\\
2
\end{pmatrix}.
$$

We will compare $RSx$ (scale, then rotate) with $SRx$ (rotate, then scale).

## 4. Scale first, then rotate: $RSx$

The rightmost matrix, $S$, acts first:

$$
Sx=
\begin{pmatrix}
2 & 0\\
0 & 1
\end{pmatrix}
\begin{pmatrix}
1\\
2
\end{pmatrix}
=
\begin{pmatrix}
2\\
2
\end{pmatrix}.
$$

Now apply the rotation $R$:

$$
RSx=
\begin{pmatrix}
0 & -1\\
1 & 0
\end{pmatrix}
\begin{pmatrix}
2\\
2
\end{pmatrix}
=
\begin{pmatrix}
-2\\
2
\end{pmatrix}.
$$

Thus, scaling first and rotating second gives

$$
\boxed{RSx=
\begin{pmatrix}
-2\\
2
\end{pmatrix}}.
$$

## 5. Rotate first, then scale: $SRx$

This time, the rightmost matrix, $R$, acts first:

$$
Rx=
\begin{pmatrix}
0 & -1\\
1 & 0
\end{pmatrix}
\begin{pmatrix}
1\\
2
\end{pmatrix}
=
\begin{pmatrix}
-2\\
1
\end{pmatrix}.
$$

Now apply the scaling $S$:

$$
SRx=
\begin{pmatrix}
2 & 0\\
0 & 1
\end{pmatrix}
\begin{pmatrix}
-2\\
1
\end{pmatrix}
=
\begin{pmatrix}
-4\\
1
\end{pmatrix}.
$$

Therefore, rotating first and scaling second gives

$$
\boxed{SRx=
\begin{pmatrix}
-4\\
1
\end{pmatrix}}.
$$

## 6. Compare the compositions

The two results are different:

$$
RSx=
\begin{pmatrix}
-2\\
2
\end{pmatrix},
\qquad
SRx=
\begin{pmatrix}
-4\\
1
\end{pmatrix}.
$$

Hence, for this vector,

$$
\boxed{RSx\ne SRx}.
$$

The matrices themselves also differ:

$$
RS=
\begin{pmatrix}
0 & -1\\
2 & 0
\end{pmatrix},
\qquad
SR=
\begin{pmatrix}
0 & -2\\
1 & 0
\end{pmatrix}.
$$

Thus $RS\ne SR$: these transformations do not commute. Checking the matrices
shows that the transformations differ in general, not just for the particular
vector $x$ used in the example.

## 7. Geometric interpretation

- **Scale, then rotate:** $x=(1,2)$ becomes $(2,2)$ after scaling, then
  $(-2,2)$ after the counterclockwise rotation.
- **Rotate, then scale:** $x=(1,2)$ becomes $(-2,1)$ after rotation, then
  $(-4,1)$ after scaling.

The scaling treats horizontal and vertical coordinates differently. Rotating
the vector first changes which coordinates are horizontal and vertical before
the scaling is applied. That is why the order matters.

## 8. Visualize the transformations with Python

This program calculates the intermediate vectors and plots each one from the
origin. It also prints the two final results.

```python
import matplotlib.pyplot as plt
import numpy as np

S = np.array([[2, 0], [0, 1]])
R = np.array([[0, -1], [1, 0]])
x = np.array([1, 2])

scaled = S @ x
scale_then_rotate = R @ scaled
rotated = R @ x
rotate_then_scale = S @ rotated

vectors = [
    (x, "Original vector x", "tab:blue"),
    (scaled, "Scaled vector Sx", "tab:orange"),
    (scale_then_rotate, "RSx: scale then rotate", "tab:green"),
    (rotated, "Rotated vector Rx", "tab:red"),
    (rotate_then_scale, "SRx: rotate then scale", "tab:purple"),
]

fig, ax = plt.subplots(figsize=(8, 8))

for vector, label, color in vectors:
    ax.quiver(
        0,
        0,
        vector[0],
        vector[1],
        angles="xy",
        scale_units="xy",
        scale=1,
        label=label,
        color=color,
    )

ax.axhline(0, color="black", linewidth=0.8)
ax.axvline(0, color="black", linewidth=0.8)
ax.set_xlim(-5, 3)
ax.set_ylim(-1, 4)
ax.set_aspect("equal", adjustable="box")
ax.set_xlabel("x-coordinate")
ax.set_ylabel("y-coordinate")
ax.set_title("Order of Scaling and Rotation")
ax.grid(True)
ax.legend(loc="best")

print("RSx (scale, then rotate):", scale_then_rotate)
print("SRx (rotate, then scale):", rotate_then_scale)

output_path = (
    "solutions/1_Algebra/01_matrices_and_operations/"
    "problem_09_transformations.png"
)
plt.savefig(output_path, dpi=180, bbox_inches="tight")
print(f"Plot saved to {output_path}")

plt.show()
```

## 9. Key takeaway

For a product $ABx$, apply $B$ first and then $A$. Since changing the order of
transformations can change the result, always read matrix compositions from
right to left and check whether the matrices commute before swapping their
order.

## 10. Plot from section 8

![Plot of the original vector and the results of applying scaling and rotation in different orders](problem_09_transformations.png)
