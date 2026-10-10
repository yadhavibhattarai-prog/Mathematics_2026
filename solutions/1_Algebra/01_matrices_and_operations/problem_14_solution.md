# Exercise 14. Rotation Matrices and Angle Addition

## Given

The rotation matrix for an angle $\theta$ is

$$
R(\theta)=
\begin{pmatrix}
\cos\theta & -\sin\theta\\
\sin\theta & \cos\theta
\end{pmatrix}
$$

We want to prove that

$$
R(\alpha)R(\beta)=R(\alpha+\beta)
$$

## Step 1: Write the two rotation matrices

$$
R(\alpha)=
\begin{pmatrix}
\cos\alpha & -\sin\alpha\\
\sin\alpha & \cos\alpha
\end{pmatrix}
$$

$$
R(\beta)=
\begin{pmatrix}
\cos\beta & -\sin\beta\\
\sin\beta & \cos\beta
\end{pmatrix}
$$

## Step 2: Multiply the matrices

Using the matrix multiplication formula

$$
\begin{pmatrix}
a & b\\
c & d
\end{pmatrix}
\begin{pmatrix}
e & f\\
g & h
\end{pmatrix}
=
\begin{pmatrix}
ae+bg & af+bh\\
ce+dg & cf+dh
\end{pmatrix}
$$

we obtain

$$
R(\alpha)R(\beta)=
\begin{pmatrix}
\cos\alpha\cos\beta-\sin\alpha\sin\beta
&
-\cos\alpha\sin\beta-\sin\alpha\cos\beta
\\
\sin\alpha\cos\beta+\cos\alpha\sin\beta
&
-\sin\alpha(-\sin\beta)+\cos\alpha\cos\beta
\end{pmatrix}
$$

Simplifying the bottom-right entry gives

$$
R(\alpha)R(\beta)=
\begin{pmatrix}
\cos\alpha\cos\beta-\sin\alpha\sin\beta
&
-(\cos\alpha\sin\beta+\sin\alpha\cos\beta)
\\
\sin\alpha\cos\beta+\cos\alpha\sin\beta
&
\cos\alpha\cos\
