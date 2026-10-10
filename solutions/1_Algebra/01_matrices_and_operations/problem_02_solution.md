
# Exercise 2: Addition and Scalar Multiplication

Given:

$$
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
$$

We need to compute:

$$
A+B,\qquad A-B,\qquad 3A-2B
$$

## 1. Meaning of Matrix Addition, Subtraction, and Scalar Multiplication

- **Matrix addition:** Add the corresponding entries of two matrices.
- **Matrix subtraction:** Subtract the corresponding entries of the second matrix from the first matrix.
- **Scalar multiplication:** Multiply every entry of a matrix by a single number called a scalar.

### Difference Between These Operations

| Operation | Meaning | Example |
|---|---|---|
| Addition | Add corresponding entries | \(1+4=5\) |
| Subtraction | Subtract corresponding entries | \(1-4=-3\) |
| Scalar multiplication | Multiply every entry by a number | \(3\times1=3\) |

**Important:** Matrix addition and subtraction require matrices of the same size. Scalar multiplication does not require another matrix.

## 2. Calculate \(A+B\)

Matrix addition is performed by adding the corresponding entries of both matrices.

$$
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
$$

Adding the corresponding entries:

$$
A+B=
\begin{pmatrix}
1+4 & 2+(-2)\\
-1+0 & 3+5
\end{pmatrix}
$$

Therefore,

$$
\boxed{
A+B=
\begin{pmatrix}
5 & 0\\
-1 & 8
\end{pmatrix}
}
$$

## 3. Calculate \(A-B\)

Matrix subtraction is performed by subtracting the corresponding entries of the second matrix from the first matrix.

$$
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
$$

Subtracting the corresponding entries:

$$
A-B=
\begin{pmatrix}
1-4 & 2-(-2)\\
-1-0 & 3-5
\end{pmatrix}
$$

Therefore,

$$
\boxed{
A-B=
\begin{pmatrix}
-3 & 4\\
-1 & -2
\end{pmatrix}
}
$$

## 4. Calculate \(3A-2B\)

First, multiply every entry of matrix \(A\) by 3.

$$
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
$$

Next, multiply every entry of matrix \(B\) by 2.

$$
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
$$

Now subtract \(2B\) from \(3A\).

$$
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
$$

Subtracting the corresponding entries:

$$
3A-2B=
\begin{pmatrix}
3-8 & 6-(-4)\\
-3-0 & 9-10
\end{pmatrix}
$$

Therefore,

$$
\boxed{
3A-2B=
\begin{pmatrix}
-5 & 10\\
-3 & -1
\end{pmatrix}
}
$$

## 5. Plot / Visual Representation

Matrices can be represented as grids, where each position contains a numerical value.

### Matrix A

| 1 | 2 |
|---:|---:|
| -1 | 3 |

### Matrix B

| 4 | -2 |
|---:|---:|
| 0 | 5 |

### Matrix Addition: \(A+B\)

Add the values in matching positions.

| \(1+4=5\) | \(2+(-2)=0\) |
|---:|---:|
| \(-1+0=-1\) | \(3+5=8\) |

Result:

$$
\begin{pmatrix}
5 & 0\\
-1 & 8
\end{pmatrix}
$$

### Matrix Subtraction: \(A-B\)

Subtract the values in matching positions.

| \(1-4=-3\) | \(2-(-2)=4\) |
|---:|---:|
| \(-1-0=-1\) | \(3-5=-2\) |

Result:

$$
\begin{pmatrix}
-3 & 4\\
-1 & -2
\end{pmatrix}
$$

### Scalar Multiplication

Multiplying \(A\) by 3 means multiplying every entry by 3.

| \(3\times1=3\) | \(3\times2=6\) |
|---:|---:|
| \(3\times(-1)=-3\) | \(3\times3=9\) |

Result:

$$
3A=
\begin{pmatrix}
3 & 6\\
-3 & 9
\end{pmatrix}
$$

**Note:** These grid tables are visual representations of the operations, not coordinate plots.

## 6. Why Is Matrix Addition Possible Only for Matrices of the Same Size?

Matrix addition is possible only when both matrices have the same number of rows and columns because we add their corresponding entries.

For example, a \(2\times2\) matrix has four entries. Each entry must have a corresponding entry in the other matrix.

If one matrix is \(2\times2\) and the other is \(2\times3\), their entries cannot be matched in every position. Therefore, their addition is undefined.

In this exercise, both \(A\) and \(B\) have size \(2\times2\), so addition and subtraction are possible.

**Conclusion:** Two matrices can be added or subtracted only if they have the same dimensions.

## Final Answers

$$
\boxed{
A+B=
\begin{pmatrix}
5 & 0\\
-1 & 8
\end{pmatrix}
}
$$

$$
\boxed{
A-B=
\begin{pmatrix}
-3 & 4\\
-1 & -2
\end{pmatrix}
}
$$

$$
\boxed{
3A-2B=
\begin{pmatrix}
-5 & 10\\
-3 & -1
\end{pmatrix}
}
$$
