# Exercise 1. From a System to a Matrix

Write the system

$$
\begin{cases}
2x-y+z=4, \\
x+3y-2z=1, \\
3x+y+z=7.
\end{cases}
$$

in the form $Ax=b$. Identify the coefficient matrix, the vector of unknowns, and the right-hand side vector. Explain how each row of the matrix corresponds to one equation.

## Solution

Let

$$
A=
\begin{pmatrix}
2&-1&1\\
1&3&-2\\
3&1&1
\end{pmatrix},
\qquad
\mathbf{x}=
\begin{pmatrix}
x\\y\\z
\end{pmatrix},
\qquad
\mathbf{b}=
\begin{pmatrix}
4\\1\\7
\end{pmatrix}.
$$

Then the system is $A\mathbf{x}=\mathbf{b}$. Each row of $A$ lists the coefficients of $x,y,z$ in the corresponding equation, in that order. The matching entry of $\mathbf{b}$ is that equation's right-hand side.