### Exercise 11. When Do Matrices Commute?

Given:

$$
A=
\begin{pmatrix}
1 & 1\\
0 & 1
\end{pmatrix},
\qquad
B=
\begin{pmatrix}
a & b\\
c & d
\end{pmatrix}
$$

We need to find the conditions on $a,b,c,d$ such that $AB=BA$ and describe the general form of all such matrices $B$.

### Step 1: Compute $AB$

$$
\begin{aligned}
AB
&=
\begin{pmatrix}
1 & 1\\
0 & 1
\end{pmatrix}
\begin{pmatrix}
a & b\\
c & d
\end{pmatrix}\\
&=
\begin{pmatrix}
a+c & b+d\\
c & d
\end{pmatrix}
\end{aligned}
$$

### Step 2: Compute $BA$

$$
\begin{aligned}
BA
&=
\begin{pmatrix}
a & b\\
c & d
\end{pmatrix}
\begin{pmatrix}
1 & 1\\
0 & 1
\end{pmatrix}\\
&=
\begin{pmatrix}
a & a+b\\
c & c+d
\end{pmatrix}
\end{aligned}
$$

### Step 3: Set $AB=BA$

For two matrices to be equal, their corresponding entries must be equal.

$$
\begin{pmatrix}
a+c & b+d\\
c & d
\end{pmatrix}
=
\begin{pmatrix}
a & a+b\\
c & c+d
\end{pmatrix}
$$

Comparing entries gives:

$$
\begin{aligned}
a+c&=a\\
b+d&=a+b\\
d&=c+d
\end{aligned}
$$

From the first equation:

$$
a+c=a \implies c=0
$$

From the second equation:

$$
b+d=a+b \implies d=a
$$

The third equation also gives $c=0$.

Therefore, the required conditions are:

$$
\boxed{c=0,\qquad d=a}
$$

There are no restrictions on $a$ or $b$.

### Step 4: Find the General Form of $B$

Substituting $c=0$ and $d=a$ into $B$ gives:

$$
\boxed{
B=
\begin{pmatrix}
a & b\\
0 & a
\end{pmatrix},
\qquad a,b\in\mathbb{R}
}
$$

### Step 5: Verify the Result

Using the general form of $B$:

$$
AB=
\begin{pmatrix}
1 & 1\\
0 & 1
\end{pmatrix}
\begin{pmatrix}
a & b\\
0 & a
\end{pmatrix}
=
\begin{pmatrix}
a & a+b\\
0 & a
\end{pmatrix}
$$

Similarly,

$$
BA=
\begin{pmatrix}
a & b\\
0 & a
\end{pmatrix}
\begin{pmatrix}
1 & 1\\
0 & 1
\end{pmatrix}
=
\begin{pmatrix}
a & a+b\\
0 & a
\end{pmatrix}
$$

Thus,

$$
\boxed{AB=BA}
$$

---

### Step 6: Plot a Visual Example

The following Python code compares the products $AB$ and $BA$ for one matrix that commutes with $A$ and one that does not.

```python
import numpy as np
import matplotlib.pyplot as plt

A = np.array([
    [1, 1],
    [0, 1]
])

# Example 1: B commutes with A
B1 = np.array([
    [2, 3],
    [0, 2]
])

# Example 2: B does not commute with A
B2 = np.array([
    [1, 2],
    [3, 4]
])

matrices = [
    (B1, "Example 1: B commutes with A"),
    (B2, "Example 2: B does not commute with A")
]

fig, axes = plt.subplots(2, 3, figsize=(11, 7))

for i, (B, title) in enumerate(matrices):
    AB = A @ B
    BA = B @ A

    products = [B, AB, BA]
    titles = ["Matrix B", "Product AB", "Product BA"]

    for j, (M, subplot_title) in enumerate(zip(products, titles)):
        ax = axes[i, j]
        ax.imshow(M, cmap="Blues")
        ax.set_title(subplot_title)

        for row in range(M.shape[0]):
            for col in range(M.shape[1]):
                ax.text(
                    col, row, str(M[row, col]),
                    ha="center", va="center"
                )

        ax.set_xticks([0, 1])
        ax.set_yticks([0, 1])

    axes[i, 0].set_ylabel(title)

plt.tight_layout()
plt.savefig("exercise11_plot.png", dpi=300, bbox_inches="tight")
plt.show()
