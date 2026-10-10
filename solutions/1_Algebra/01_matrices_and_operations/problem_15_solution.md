# Exercise 15. Associativity of Multiplication and Different Calculation Paths

## Given

$$
A=
\begin{pmatrix}
1 & 2 & 0\\
0 & 1 & 1
\end{pmatrix},
\quad
B=
\begin{pmatrix}
1 & 0\\
2 & 1\\
-1 & 3
\end{pmatrix},
\quad
C=
\begin{pmatrix}
2 & 1\\
0 & -1
\end{pmatrix}
$$

We need to compute $(AB)C$ and $A(BC)$, compare the results and the number of intermediate operations, and explain associativity.

## Step 1: Calculate $(AB)C$

First, calculate $AB$.

Using the matrix multiplication rule, multiply each row of $A$ by each column of $B$.

$$
AB=
\begin{pmatrix}
1 & 2 & 0\\
0 & 1 & 1
\end{pmatrix}
\begin{pmatrix}
1 & 0\\
2 & 1\\
-1 & 3
\end{pmatrix}
$$

Calculate each entry:

$$
\begin{aligned}
(AB)_{11}&=1(1)+2(2)+0(-1)=5\\
(AB)_{12}&=1(0)+2(1)+0(3)=2\\
(AB)_{21}&=0(1)+1(2)+1(-1)=1\\
(AB)_{22}&=0(0)+1(1)+1(3)=4
\end{aligned}
$$

Therefore,

$$
AB=
\begin{pmatrix}
5 & 2\\
1 & 4
\end{pmatrix}
$$

Now multiply $AB$ by $C$.

$$
(AB)C=
\begin{pmatrix}
5 & 2\\
1 & 4
\end{pmatrix}
\begin{pmatrix}
2 & 1\\
0 & -1
\end{pmatrix}
$$

Calculate each entry:

$$
\begin{aligned}
((AB)C)_{11}&=5(2)+2(0)=10\\
((AB)C)_{12}&=5(1)+2(-1)=3\\
((AB)C)_{21}&=1(2)+4(0)=2\\
((AB)C)_{22}&=1(1)+4(-1)=-3
\end{aligned}
$$

Thus,

$$
\boxed{
(AB)C=
\begin{pmatrix}
10 & 3\\
2 & -3
\end{pmatrix}
}
$$

## Step 2: Calculate $A(BC)$

First, calculate $BC$.

$$
BC=
\begin{pmatrix}
1 & 0\\
2 & 1\\
-1 & 3
\end{pmatrix}
\begin{pmatrix}
2 & 1\\
0 & -1
\end{pmatrix}
$$

Calculate each entry:

$$
\begin{aligned}
(BC)_{11}&=1(2)+0(0)=2\\
(BC)_{12}&=1(1)+0(-1)=1\\
(BC)_{21}&=2(2)+1(0)=4\\
(BC)_{22}&=2(1)+1(-1)=1\\
(BC)_{31}&=(-1)(2)+3(0)=-2\\
(BC)_{32}&=(-1)(1)+3(-1)=-4
\end{aligned}
$$

Therefore,

$$
BC=
\begin{pmatrix}
2 & 1\\
4 & 1\\
-2 & -4
\end{pmatrix}
$$

Now multiply $A$ by $BC$.

$$
A(BC)=
\begin{pmatrix}
1 & 2 & 0\\
0 & 1 & 1
\end{pmatrix}
\begin{pmatrix}
2 & 1\\
4 & 1\\
-2 & -4
\end{pmatrix}
$$

Calculate each entry:

$$
\begin{aligned}
(A(BC))_{11}&=1(2)+2(4)+0(-2)=10\\
(A(BC))_{12}&=1(1)+2(1)+0(-4)=3\\
(A(BC))_{21}&=0(2)+1(4)+1(-2)=2\\
(A(BC))_{22}&=0(1)+1(1)+1(-4)=-3
\end{aligned}
$$

Thus,

$$
\boxed{
A(BC)=
\begin{pmatrix}
10 & 3\\
2 & -3
\end{pmatrix}
}
$$

## Step 3: Compare the Results

We obtained

$$
(AB)C=
\begin{pmatrix}
10 & 3\\
2 & -3
\end{pmatrix}
$$

and

$$
A(BC)=
\begin{pmatrix}
10 & 3\\
2 & -3
\end{pmatrix}
$$

Therefore,

$$
\boxed{(AB)C=A(BC)}
$$

Both calculation paths produce exactly the same matrix.

## Step 4: Compare the Calculation Paths

There are two possible ways to calculate the product of three matrices.

**Path 1: Multiply $A$ and $B$ first**

$$
A,B \longrightarrow AB
$$

Then multiply the result by $C$:

$$
AB,C \longrightarrow (AB)C
$$

**Path 2: Multiply $B$ and $C$ first**

$$
B,C \longrightarrow BC
$$

Then multiply $A$ by the result:

$$
A,BC \longrightarrow A(BC)
$$

Each path requires two matrix multiplications:

- Path 1: Calculate $AB$, then calculate $(AB)C$.
- Path 2: Calculate $BC$, then calculate $A(BC)$.

Therefore, both paths require **two matrix multiplication operations**. However, the intermediate matrices have different sizes:

- $AB$ is a $2\times2$ matrix.
- $BC$ is a $3\times2$ matrix.

This means the number of arithmetic calculations can differ even though the number of matrix multiplications is the same.

## Step 5: Explain Associativity

Associativity means that when multiplying three matrices, changing the grouping of the matrices does not change the final result.

In general,

$$
\boxed{(AB)C=A(BC)}
$$

In this example, multiplying $A$ by $B$ first and then multiplying by $C$ gives the same result as multiplying $B$ by $C$ first and then multiplying by $A$.

The grouping changes, but the order of the matrices remains $A$, $B$, $C$.

**Important:** Associativity does not mean that we can freely change the order of matrices. It means we can change their grouping without changing the result.

## Conclusion

We have shown that

$$
\boxed{
(AB)C=A(BC)=
\begin{pmatrix}
10 & 3\\
2 & -3
\end{pmatrix}
}
$$

Both calculation paths require two matrix multiplications and produce the same final matrix.

Therefore, this example demonstrates the associativity of matrix multiplication.
