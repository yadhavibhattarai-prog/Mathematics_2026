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
2(1)+0(2)\\
0(1)+1(2)
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
R(Sx)\\
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
0(2)-1(2)\\
1(2)+0(2)
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

This means we first scale the vector and then rotate it \(90^\circ\) counterclockwise.

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
0(1)-1(2)\\
1(1)+0(2)
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
S(Rx)\\
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
2(-2)+0(1)\\
0(-2)+1(1)
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

This means we first rotate the vector and then apply nonuniform scaling.

---

### Step 3: Compare the Results

We obtained:

$$
RSx=
\begin{pmatrix}
-2\\
2
\end{pmatrix}
$$

and

$$
SRx=
\begin{pmatrix}
-4\\
1
\end{pmatrix}
$$

Since

$$
\begin{pmatrix}
-2\\
2
\end{pmatrix}
\neq
\begin{pmatrix}
-4\\
1
\end{pmatrix},
$$

we conclude that

$$
\boxed{RSx\neq SRx}
$$

### Step 4: Geometric Explanation

The order of transformations matters because **nonuniform scaling and rotation generally do not commute**.

- **For $RSx$:** We first stretch the vector horizontally by a factor of $2$, changing $(1,2)$ into $(2,2)$. Then we rotate it \(90^\circ\) counterclockwise, obtaining $(-2,2)$.
- **For $SRx$:** We first rotate $(1,2)$ into $(-2,1)$. Then we stretch it horizontally by a factor of $2$, obtaining $(-4,1)$.

The results differ because the scaling operation doubles the horizontal coordinate. Rotating before scaling changes which coordinate is affected by that scaling.

### Final Answer

$$
\boxed{RSx=
\begin{pmatrix}
-2\\
2
\end{pmatrix},
\qquad
SRx=
\begin{pmatrix}
-4\\
1
\end{pmatrix}}
$$

Therefore, the order of transformations matters. Applying scaling and then rotation produces a different result from applying rotation and then scaling. This illustrates why matrix multiplication is generally **noncommutative**:

$$
\boxed{RS\neq SR}
$$
