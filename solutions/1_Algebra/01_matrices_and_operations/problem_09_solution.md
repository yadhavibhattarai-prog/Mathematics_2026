### Exercise 9. Composing Transformations

Given:

$$
S=
\begin{pmatrix}
2 & 0\\
0 & 1
\end{pmatrix},
\qquad
R=
\begin{pmatrix}
0 & -1\\
1 & 0
\end{pmatrix}
$$

and

$$
x=
\begin{pmatrix}
1\\
2
\end{pmatrix}
$$

The matrix $S$ describes nonuniform scaling, which doubles the $x$-coordinate while keeping the $y$-coordinate unchanged. The matrix $R$ describes a $90^\circ$ counterclockwise rotation.

### Step 1: Compute $RSx$

First, calculate $Sx$:

$$
\begin{aligned}
Sx
&=
\begin{pmatrix}
2 & 0\\
0 & 1
\end{pmatrix}
\begin{pmatrix}
1\\
2
\end{pmatrix}\\
&=
\begin{pmatrix}
2\\
2
\end{pmatrix}
\end{aligned}
$$

Now multiply the result by $R$:

$$
\begin{aligned}
RSx
&=
\begin{pmatrix}
0 & -1\\
1 & 0
\end{pmatrix}
\begin{pmatrix}
2\\
2
\end{pmatrix}\\
&=
\begin{pmatrix}
-2\\
2
\end{pmatrix}
\end{aligned}
$$

Therefore,

$$
\boxed{RSx=
\begin{pmatrix}
-2\\
2
\end{pmatrix}}
$$

We first scale the vector and then rotate it $90^\circ$ counterclockwise.

---

### Step 2: Compute $SRx$

First, calculate $Rx$:

$$
\begin{aligned}
Rx
&=
\begin{pmatrix}
0 & -1\\
1 & 0
\end{pmatrix}
\begin{pmatrix}
1\\
2
\end{pmatrix}\\
&=
\begin{pmatrix}
-2\\
1
\end{pmatrix}
\end{aligned}
$$

Now multiply the result by $S$:

$$
\begin{aligned}
SRx
&=
\begin{pmatrix}
2 & 0\\
0 & 1
\end{pmatrix}
\begin{pmatrix}
-2\\
1
\end{pmatrix}\\
&=
\begin{pmatrix}
-4\\
1
\end{pmatrix}
\end{aligned}
$$

Therefore,

$$
\boxed{SRx=
\begin{pmatrix}
-4\\
1
\end{pmatrix}}
$$

We first rotate the vector and then apply nonuniform scaling.

---

### Step 3: Compare the Results

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
\end{pmatrix}
$$

Since the two vectors are different,

$$
\boxed{RSx\neq SRx}
$$

### Step 4: Geometric Explanation

- **For $RSx$:** We first stretch the vector horizontally by a factor of $2$, changing $(1,2)$ into $(2,2)$. Then we rotate it $90^\circ$ counterclockwise, obtaining $(-2,2)$.
- **For $SRx$:** We first rotate $(1,2)$ into $(-2,1)$. Then we stretch it horizontally by a factor of $2$, obtaining $(-4,1)$.

The order matters because nonuniform scaling changes the horizontal coordinate differently from the vertical coordinate. Rotating first changes which part of the vector is affected by the scaling.

---

### Step 5: Plot the Transformations

The following Python code plots the original vector and the vectors obtained after each transformation.


import matplotlib.pyplot as plt

# Original vector
x = (1, 2)

# After scaling: Sx
Sx = (2, 2)

# After rotation: RSx
RSx = (-2, 2)

# After rotation: Rx
Rx = (-2, 1)

# After scaling: SRx
SRx = (-4, 1)

# Create the plot
fig, ax = plt.subplots(figsize=(8, 8))

vectors = [
    (x, "Original vector x"),
    (Sx, "Scaled vector Sx"),
    (RSx, "RSx: Scale then rotate"),
    (Rx, "Rotated vector Rx"),
    (SRx, "SRx: Rotate then scale"),
]

for (vx, vy), label in vectors:
    ax.quiver(
        0, 0, vx, vy,
        angles="xy",
        scale_units="xy",
        scale=1,
        label=label
    )

# Coordinate axes and grid
ax.axhline(0, linewidth=0.8)
ax.axvline(0, linewidth=0.8)
ax.set_xlim(-5, 3)
ax.set_ylim(-1, 4)
ax.set_aspect("equal", adjustable="box")
ax.set_xlabel("x-coordinate")
ax.set_ylabel("y-coordinate")
ax.set_title("Composition of Scaling and Rotation")
ax.grid(True)
ax.legend(loc="best")

plt.show()
