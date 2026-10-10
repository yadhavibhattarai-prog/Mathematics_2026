
# Exercise 6: Transpose

Given:

$$
A=
\begin{pmatrix}
1 & 2 & 3\\
4 & 5 & 6
\end{pmatrix},
\qquad
B=
\begin{pmatrix}
1 & 0\\
2 & 1\\
-1 & 3
\end{pmatrix}
$$

We need to compute \(A^T\), \(B^T\), and \(AB\). Then verify that

$$
(AB)^T=B^TA^T
$$

## 1. Compute \(A^T\)

The transpose of a matrix is obtained by changing its rows into columns and its columns into rows.

Given:

$$
A=
\begin{pmatrix}
1 & 2 & 3\\
4 & 5 & 6
\end{pmatrix}
$$

The first row \((1,2,3)\) becomes the first column, and the second row \((4,5,6)\) becomes the second column.

Therefore,

$$
\boxed{
A^T=
\begin{pmatrix}
1 & 4\\
2 & 5\\
3 & 6
\end{pmatrix}
}
$$

## 2. Compute \(B^T\)

Given:

$$
B=
\begin{pmatrix}
1 & 0\\
2 & 1\\
-1 & 3
\end{pmatrix}
$$

Changing the rows of \(B\) into columns gives:

$$
\boxed{
B^T=
\begin{pmatrix}
1 & 2 & -1\\
0 & 1 & 3
\end{pmatrix}
}
$$

## 3. Compute \(AB\)

First, check the dimensions:

- Matrix \(A\) has size \(2\times3\).
- Matrix \(B\) has size \(3\times2\).

Since the number of columns of \(A\) equals the number of rows of \(B\), multiplication is possible.

The resulting matrix has size \(2\times2\).

$$
AB=
\begin{pmatrix}
1 & 2 & 3\\
4 & 5 & 6
\end{pmatrix}
\begin{pmatrix}
1 & 0\\
2 & 1\\
-1 & 3
\end{pmatrix}
$$

Calculate each entry:

**First row, first column:**

$$
(1\times1)+(2\times2)+(3\times(-1))
=1+4-3=2
$$

**First row, second column:**

$$
(1\times0)+(2\times1)+(3\times3)
=0+2+9=11
$$

**Second row, first column:**

$$
(4\times1)+(5\times2)+(6\times(-1))
=4+10-6=8
$$

**Second row, second column:**

$$
(4\times0)+(5\times1)+(6\times3)
=0+5+18=23
$$

Therefore,

$$
\boxed{
AB=
\begin{pmatrix}
2 & 11\\
8 & 23
\end{pmatrix}
}
$$

## 4. Compute \((AB)^T\)

From the previous calculation:

$$
AB=
\begin{pmatrix}
2 & 11\\
8 & 23
\end{pmatrix}
$$

Taking the transpose means changing rows into columns.

Therefore,

$$
\boxed{
(AB)^T=
\begin{pmatrix}
2 & 8\\
11 & 23
\end{pmatrix}
}
$$

## 5. Compute \(B^TA^T\)

We have already calculated:

$$
B^T=
\begin{pmatrix}
1 & 2 & -1\\
0 & 1 & 3
\end{pmatrix}
$$

and

$$
A^T=
\begin{pmatrix}
1 & 4\\
2 & 5\\
3 & 6
\end{pmatrix}
$$

Now multiply \(B^T\) by \(A^T\):

$$
B^TA^T=
\begin{pmatrix}
1 & 2 & -1\\
0 & 1 & 3
\end{pmatrix}
\begin{pmatrix}
1 & 4\\
2 & 5\\
3 & 6
\end{pmatrix}
$$

Calculate each entry:

**First row, first column:**

$$
(1\times1)+(2\times2)+(-1\times3)
=1+4-3=2
$$

**First row, second column:**

$$
(1\times4)+(2\times5)+(-1\times6)
=4+10-6=8
$$

**Second row, first column:**

$$
(0\times1)+(1\times2)+(3\times3)
=0+2+9=11
$$

**Second row, second column:**

$$
(0\times4)+(1\times5)+(3\times6)
=0+5+18=23
$$

Therefore,

$$
\boxed{
B^TA^T=
\begin{pmatrix}
2 & 8\\
11 & 23
\end{pmatrix}
}
$$

## 6. Verify the Property

We obtained:

$$
(AB)^T=
\begin{pmatrix}
2 & 8\\
11 & 23
\end{pmatrix}
$$

and

$$
B^TA^T=
\begin{pmatrix}
2 & 8\\
11 & 23
\end{pmatrix}
$$

Both matrices are equal. Therefore,

$$
\boxed{(AB)^T=B^TA^T}
$$

The property is verified.

## 7. Conclusion

The transpose of a matrix changes its rows into columns and its columns into rows.

An important property of matrix multiplication is:

$$
\boxed{(AB)^T=B^TA^T}
$$

This means that when taking the transpose of a product of two matrices, we transpose each matrix and reverse the order of multiplication.

In general, the transpose of a product reverses the order of its factors.
