# Exercise 2: Addition and Scalar Multiplication

Given:

\[
A=
\begin{pmatrix}
1 & 2\\
-1 & 3
\end{pmatrix},
\qquad
B=
\begin{pmatrix}
4 & -2\\
0 & 5
\end{pmatrix}
\]

We need to compute:

\[
A+B,\qquad A-B,\qquad 3A-2B
\]

## 1. Calculate \(A+B\)

Matrix addition is performed by adding the corresponding entries of both matrices.

\[
A+B=
\begin{pmatrix}
1 & 2\\
-1 & 3
\end{pmatrix}
+
\begin{pmatrix}
4 & -2\\
0 & 5
\end{pmatrix}
\]

Adding the corresponding entries:

\[
A+B=
\begin{pmatrix}
1+4 & 2+(-2)\\
-1+0 & 3+5
\end{pmatrix}
\]

Therefore,

\[
\boxed{
A+B=
\begin{pmatrix}
5 & 0\\
-1 & 8
\end{pmatrix}
}
\]

## 2. Calculate \(A-B\)

Matrix subtraction is performed by subtracting the corresponding entries of the second matrix from the first matrix.

\[
A-B=
\begin{pmatrix}
1 & 2\\
-1 & 3
\end{pmatrix}
-
\begin{pmatrix}
4 & -2\\
0 & 5
\end{pmatrix}
\]

Subtracting the corresponding entries:

\[
A-B=
\begin{pmatrix}
1-4 & 2-(-2)\\
-1-0 & 3-5
\end{pmatrix}
\]

Therefore,

\[
\boxed{
A-B=
\begin{pmatrix}
-3 & 4\\
-1 & -2
\end{pmatrix}
}
\]

## 3. Calculate \(3A-2B\)

First, multiply every entry of matrix \(A\) by \(3\):

\[
3A=
3\begin{pmatrix}
1 & 2\\
-1 & 3
\end{pmatrix}
=
\begin{pmatrix}
3 & 6\\
-3 & 9
\end{pmatrix}
\]

Next, multiply every entry of matrix \(B\) by \(2\):

\[
2B=
2\begin{pmatrix}
4 & -2\\
0 & 5
\end{pmatrix}
=
\begin{pmatrix}
8 & -4\\
0 & 10
\end{pmatrix}
\]

Now subtract \(2B\) from \(3A\):

\[
3A-2B=
\begin{pmatrix}
3 & 6\\
-3 & 9
\end{pmatrix}
-
\begin{pmatrix}
8 & -4\\
0 & 10
\end{pmatrix}
\]

Subtracting the corresponding entries:

\[
3A-2B=
\begin{pmatrix}
3-8 & 6-(-4)\\
-3-0 & 9-10
\end{pmatrix}
\]

Therefore,

\[
\boxed{
3A-2B=
\begin{pmatrix}
-5 & 10\\
-3 & -1
\end{pmatrix}
}
\]

## 4. Why is matrix addition possible only for matrices of the same size?

Matrix addition is possible only when both matrices have the same number of rows and columns because we add their corresponding entries.

For example, a \(2\times 2\) matrix has four entries, and each entry must have a corresponding entry in the other matrix.

If one matrix is \(2\times 2\) and the other is \(2\times 3\), their entries cannot be matched in every position. Therefore, their addition is undefined.

In this exercise, both \(A\) and \(B\) have size \(2\times 2\), so addition and subtraction are possible.

**Conclusion:** Two matrices can be added or subtracted only if they have the same dimensions.

## Final Answers

\[
\boxed{
A+B=
\begin{pmatrix}
5 & 0\\
-1 & 8
\end{pmatrix}
}
\]

\[
\boxed{
A-B=
\begin{pmatrix}
-3 & 4\\
-1 & -2
\end{pmatrix}
}
\]

\[
\boxed{
3A-2B=
\begin{pmatrix}
-5 & 10\\
-3 & -1
\end{pmatrix}
}
\]
