
# Exercise 7: Identity Matrix, Zero Matrix, and Powers

Given:

$$
A=
\begin{pmatrix}
2 & 1\\
0 & 2
\end{pmatrix}
$$

We need to compute:

$$
AI,\qquad IA,\qquad A+0,\qquad A^2,\qquad A^3
$$

## 1. Compute \(AI\)

The identity matrix of size \(2\times2\) is:

$$
I=
\begin{pmatrix}
1 & 0\\
0 & 1
\end{pmatrix}
$$

Multiplying a matrix by the identity matrix leaves the original matrix unchanged.

$$
AI=
\begin{pmatrix}
2 & 1\\
0 & 2
\end{pmatrix}
\begin{pmatrix}
1 & 0\\
0 & 1
\end{pmatrix}
$$

Calculating the entries:

$$
AI=
\begin{pmatrix}
(2\times1)+(1\times0) & (2\times0)+(1\times1)\\
(0\times1)+(2\times0) & (0\times0)+(2\times1)
\end{pmatrix}
$$

Therefore,

$$
\boxed{
AI=
\begin{pmatrix}
2 & 1\\
0 & 2
\end{pmatrix}
=A
}
$$

## 2. Compute \(IA\)

Using the same identity matrix:

$$
IA=
\begin{pmatrix}
1 & 0\\
0 & 1
\end{pmatrix}
\begin{pmatrix}
2 & 1\\
0 & 2
\end{pmatrix}
$$

Calculating the entries:

$$
IA=
\begin{pmatrix}
(1\times2)+(0\times0) & (1\times1)+(0\times2)\\
(0\times2)+(1\times0) & (0\times1)+(1\times2)
\end{pmatrix}
$$

Therefore,

$$
\boxed{
IA=
\begin{pmatrix}
2 & 1\\
0 & 2
\end{pmatrix}
=A
}
$$

Thus, multiplying \(A\) by the identity matrix on either side leaves \(A\) unchanged.

## 3. Compute \(A+0\)

The zero matrix of size \(2\times2\) is:

$$
0=
\begin{pmatrix}
0 & 0\\
0 & 0
\end{pmatrix}
$$

Adding the zero matrix to \(A\):

$$
A+0=
\begin{pmatrix}
2 & 1\\
0 & 2
\end{pmatrix}
+
\begin{pmatrix}
0 & 0\\
0 & 0
\end{pmatrix}
$$

Adding the corresponding entries:

$$
A+0=
\begin{pmatrix}
2+0 & 1+0\\
0+0 & 2+0
\end{pmatrix}
$$

Therefore,

$$
\boxed{
A+0=
\begin{pmatrix}
2 & 1\\
0 & 2
\end{pmatrix}
=A
}
$$

## 4. Compute \(A^2\)

The power \(A^2\) means multiplying \(A\) by itself.

$$
A^2=A\cdot A
$$

Substituting the matrix:

$$
A^2=
\begin{pmatrix}
2 & 1\\
0 & 2
\end{pmatrix}
\begin{pmatrix}
2 & 1\\
0 & 2
\end{pmatrix}
$$

Calculating each entry:

**First row, first column:**

$$
(2\times2)+(1\times0)=4
$$

**First row, second column:**

$$
(2\times1)+(1\times2)=2+2=4
$$

**Second row, first column:**

$$
(0\times2)+(2\times0)=0
$$

**Second row, second column:**

$$
(0\times1)+(2\times2)=4
$$

Therefore,

$$
\boxed{
A^2=
\begin{pmatrix}
4 & 4\\
0 & 4
\end{pmatrix}
}
$$

## 5. Compute \(A^3\)

The power \(A^3\) means multiplying \(A^2\) by \(A\).

$$
A^3=A^2\cdot A
$$

Substituting the matrices:

$$
A^3=
\begin{pmatrix}
4 & 4\\
0 & 4
\end{pmatrix}
\begin{pmatrix}
2 & 1\\
0 & 2
\end{pmatrix}
$$

Calculating each entry:

**First row, first column:**

$$
(4\times2)+(4\times0)=8
$$

**First row, second column:**

$$
(4\times1)+(4\times2)=4+8=12
$$

**Second row, first column:**

$$
(0\times2)+(4\times0)=0
$$

**Second row, second column:**

$$
(0\times1)+(4\times2)=8
$$

Therefore,

$$
\boxed{
A^3=
\begin{pmatrix}
8 & 12\\
0 & 8
\end{pmatrix}
}
$$

## 6. Explain the Roles of the Identity Matrix and Zero Matrix

### Identity Matrix \(I\)

The identity matrix acts like the number \(1\) in ordinary multiplication.

For any compatible matrix \(A\):

$$
AI=IA=A
$$

Multiplying a matrix by the identity matrix does not change its entries.

### Zero Matrix \(0\)

The zero matrix acts like the number \(0\) in matrix addition.

For any matrix \(A\) of the same size:

$$
A+0=A
$$

Adding the zero matrix does not change the entries of the original matrix.

**Important difference:**

- The identity matrix preserves a matrix under multiplication.
- The zero matrix preserves a matrix under addition.

## 7. Describe the Pattern in Successive Powers of \(A\)

We obtained:

$$
A=
\begin{pmatrix}
2 & 1\\
0 & 2
\end{pmatrix}
$$

$$
A^2=
\begin{pmatrix}
4 & 4\\
0 & 4
\end{pmatrix}
$$

$$
A^3=
\begin{pmatrix}
8 & 12\\
0 & 8
\end{pmatrix}
$$

Observe the following patterns:

1. The bottom-left entry remains \(0\).
2. The diagonal entries are \(2\), \(4\), and \(8\), which are successive powers of \(2\).
3. The top-right entries are \(1\), \(4\), and \(12\).

The pattern can be expressed by the general formula:

$$
\boxed{
A^n=
\begin{pmatrix}
2^n & n2^{n-1}\\
0 & 2^n
\end{pmatrix}
}
$$

for positive integers \(n\).

For example, when \(n=3\):

$$
A^3=
\begin{pmatrix}
2^3 & 3(2^{3-1})\\
0 & 2^3
\end{pmatrix}
=
\begin{pmatrix}
8 & 12\\
0 & 8
\end{pmatrix}
$$

This agrees with our calculation.

## Final Answers

$$
\boxed{
AI=IA=
\begin{pmatrix}
2 & 1\\
0 & 2
\end{pmatrix}
}
$$

$$
\boxed{
A+0=
\begin{pmatrix}
2 & 1\\
0 & 2
\end{pmatrix}
}
$$

$$
\boxed{
A^2=
\begin{pmatrix}
4 & 4\\
0 & 4
\end{pmatrix}
}
$$

$$
\boxed{
A^3=
\begin{pmatrix}
8 & 12\\
0 & 8
\end{pmatrix}
}
$$

**Conclusion:** The identity matrix is the neutral element for matrix multiplication, while the zero matrix is the neutral element for matrix addition. The successive powers of \(A\) follow a regular pattern in which the diagonal entries are powers of \(2\), the bottom-left entry stays zero, and the top-right entry follows \(n2^{n-1}\).
