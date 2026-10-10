### Exercise 10. Columns of a Matrix Product

Given:

$$
A=
\begin{pmatrix}
1 & 2 & 0\\
0 & 1 & 1
\end{pmatrix},
\qquad
B=
\begin{pmatrix}
1 & 2\\
-1 & 0\\
3 & 1
\end{pmatrix}
$$

Denote the columns of $B$ by $b_1$ and $b_2$.

Therefore,

$$
b_1=
\begin{pmatrix}
1\\
-1\\
3
\end{pmatrix},
\qquad
b_2=
\begin{pmatrix}
2\\
0\\
1
\end{pmatrix}
$$

### Step 1: Compute $Ab_1$

Multiply matrix $A$ by the first column of $B$:

$$
\begin{aligned}
Ab_1
&=
\begin{pmatrix}
1 & 2 & 0\\
0 & 1 & 1
\end{pmatrix}
\begin{pmatrix}
1\\
-1\\
3
\end{pmatrix}\\
&=
\begin{pmatrix}
1(1)+2(-1)+0(3)\\
0(1)+1(-1)+1(3)
\end{pmatrix}\\
&=
\begin{pmatrix}
1-2+0\\
0-1+3
\end{pmatrix}\\
&=
\begin{pmatrix}
-1\\
2
\end{pmatrix}
\end{aligned}
$$

Therefore,

$$
\boxed{
Ab_1=
\begin{pmatrix}
-1\\
2
\end{pmatrix}
}
$$

### Step 2: Compute $Ab_2$

Multiply matrix $A$ by the second column of $B$:

$$
\begin{aligned}
Ab_2
&=
\begin{pmatrix}
1 & 2 & 0\\
0 & 1 & 1
\end{pmatrix}
\begin{pmatrix}
2\\
0\\
1
\end{pmatrix}\\
&=
\begin{pmatrix}
1(2)+2(0)+0(1)\\
0(2)+1(0)+1(1)
\end{pmatrix}\\
&=
\begin{pmatrix}
2+0+0\\
0+0+1
\end{pmatrix}\\
&=
\begin{pmatrix}
2\\
1
\end{pmatrix}
\end{aligned}
$$

Therefore,

$$
\boxed{
Ab_2=
\begin{pmatrix}
2\\
1
\end{pmatrix}
}
$$

### Step 3: Compute the Matrix $AB$

Multiply matrix $A$ by matrix $B$:

$$
AB=
\begin{pmatrix}
1 & 2 & 0\\
0 & 1 & 1
\end{pmatrix}
\begin{pmatrix}
1 & 2\\
-1 & 0\\
3 & 1
\end{pmatrix}
$$

Calculate each entry using the row-by-column method:

$$
\begin{aligned}
(AB)_{11}&=1(1)+2(-1)+0(3)=-1\\
(AB)_{12}&=1(2)+2(0)+0(1)=2\\
(AB)_{21}&=0(1)+1(-1)+1(3)=2\\
(AB)_{22}&=0(2)+1(0)+1(1)=1
\end{aligned}
$$

Thus,

$$
\boxed{
AB=
\begin{pmatrix}
-1 & 2\\
2 & 1
\end{pmatrix}
}
$$

### Step 4: Compare the Results

From Steps 1 and 2, we obtained:

$$
Ab_1=
\begin{pmatrix}
-1\\
2
\end{pmatrix},
\qquad
Ab_2=
\begin{pmatrix}
2\\
1
\end{pmatrix}
$$

Placing these two vectors side by side gives:

$$
\begin{pmatrix}
Ab_1 & Ab_2
\end{pmatrix}
=
\begin{pmatrix}
-1 & 2\\
2 & 1
\end{pmatrix}
$$

This is exactly the matrix $AB$:

$$
\boxed{AB=\begin{pmatrix}Ab_1 & Ab_2\end{pmatrix}}
$$

### Explanation

The columns of $AB$ are exactly the vectors $Ab_1$ and $Ab_2$ because **matrix multiplication applies matrix $A$ to each column of matrix $B$ separately**.

In general, if

$$
B=\begin{pmatrix}b_1 & b_2 & \cdots & b_n\end{pmatrix},
$$

then

$$
\boxed{AB=\begin{pmatrix}Ab_1 & Ab_2 & \cdots & Ab_n\end{pmatrix}}
$$

This means we can compute a matrix product by multiplying $A$ by each column of $B$ and
