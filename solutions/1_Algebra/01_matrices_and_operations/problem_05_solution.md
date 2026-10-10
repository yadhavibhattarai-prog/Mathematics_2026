
# Exercise 5: Matrix Times Vector

Given:

$$
A=
\begin{pmatrix}
2 & -1\\
1 & 3
\end{pmatrix},
\qquad
x=
\begin{pmatrix}
4\\
2
\end{pmatrix}
$$

We need to compute \(Ax\) and express it as a linear combination of the columns of \(A\), using the coefficients from vector \(x\).

## 1. Compute \(Ax\)

Matrix multiplication is performed by multiplying each row of matrix \(A\) by the column vector \(x\) and adding the corresponding products.

$$
Ax=
\begin{pmatrix}
2 & -1\\
1 & 3
\end{pmatrix}
\begin{pmatrix}
4\\
2
\end{pmatrix}
$$

Calculating the first entry:

$$
(2\times4)+(-1\times2)=8-2=6
$$

Calculating the second entry:

$$
(1\times4)+(3\times2)=4+6=10
$$

Therefore,

$$
\boxed{
Ax=
\begin{pmatrix}
6\\
10
\end{pmatrix}
}
$$

## 2. Express \(Ax\) as a Linear Combination of the Columns of \(A\)

The columns of matrix \(A\) are:

$$
a_1=
\begin{pmatrix}
2\\
1
\end{pmatrix},
\qquad
a_2=
\begin{pmatrix}
-1\\
3
\end{pmatrix}
$$

The vector \(x\) contains the coefficients \(4\) and \(2\).

Therefore, \(Ax\) can be expressed as:

$$
Ax=4a_1+2a_2
$$

Substituting the columns of \(A\):

$$
Ax=
4\begin{pmatrix}
2\\
1
\end{pmatrix}
+
2\begin{pmatrix}
-1\\
3
\end{pmatrix}
$$

Multiplying each column by its corresponding coefficient:

$$
Ax=
\begin{pmatrix}
8\\
4
\end{pmatrix}
+
\begin{pmatrix}
-2\\
6
\end{pmatrix}
$$

Adding the vectors:

$$
Ax=
\begin{pmatrix}
8-2\\
4+6
\end{pmatrix}
=
\begin{pmatrix}
6\\
10
\end{pmatrix}
$$

Thus,

$$
\boxed{
Ax=4\begin{pmatrix}2\\1\end{pmatrix}
+2\begin{pmatrix}-1\\3\end{pmatrix}
=\begin{pmatrix}6\\10\end{pmatrix}
}
$$

## 3. Explanation

Multiplying a matrix by a vector can be understood as a linear combination of the matrix columns.

In this exercise:

- The first column of \(A\) is multiplied by \(4\).
- The second column of \(A\) is multiplied by \(2\).
- The resulting vectors are added together.

The coefficients \(4\) and \(2\) come directly from the vector \(x\).

**Conclusion:** Matrix-vector multiplication combines the columns of a matrix using the entries of the vector as coefficients.

The final answer is:

$$
\boxed{
Ax=
\begin{pmatrix}
6\\
10
\end{pmatrix}
}
$$
