# System of Linear Equations — Problem 2

## Meet the augmented matrix

We are solving for three mystery numbers, $x$, $y$, and $z$:

$$
\begin{cases}
x+y+z=6, \\
2x-y+z=3, \\
x+2y-z=2.
\end{cases}
$$

A **coefficient matrix** is made by collecting just the numbers multiplying the variables:

$$
A=
\begin{pmatrix}
1&1&1\\
2&-1&1\\
1&2&-1
\end{pmatrix}.
$$

The numbers on the right-hand sides go into a column vector,

$$
\mathbf b=
\begin{pmatrix}
6\\3\\2
\end{pmatrix}.
$$

Put the coefficient matrix and that right-hand-side column together, and you get the **augmented matrix**:

$$
\left(
\begin{array}{ccc|c}
1&1&1&6\\
2&-1&1&3\\
1&2&-1&2
\end{array}
\right).
$$

The vertical line is a little fence: the variable-coefficient columns stay on the left, and the answer numbers from the right sides stay on the right. Each row is one original equation.

## Why use a matrix?

Think of the equations as three clues in a number mystery. The matrix is a tidy clue board: it keeps all the numbers in the right places while we simplify the clues. It is easier to eliminate variables by moving rows of numbers around than by repeatedly copying long equations.

We use **Gaussian elimination** to turn the matrix into a simpler one. The legal row moves are:

- swap two rows;
- multiply a row by a nonzero number;
- add a multiple of one row to another row.

These moves do not change the solution: they change how the clues are written, not which values of $x$, $y$, and $z$ satisfy all the clues.

## Solve it, one row move at a time

Start with the augmented matrix. Use the first row to make the $x$-coefficients underneath its first $1$ become zero:

$$
\left(
\begin{array}{ccc|c}
1&1&1&6\\
2&-1&1&3\\
1&2&-1&2
\end{array}
\right)
\xrightarrow{R_2\leftarrow R_2-2R_1,\;R_3\leftarrow R_3-R_1}
\left(
\begin{array}{ccc|c}
1&1&1&6\\
0&-3&-1&-9\\
0&1&-2&-4
\end{array}
\right).
$$

For example, the new second row is the old second row minus twice the first row:
$(2,-1,1\mid3)-2(1,1,1\mid6)=(0,-3,-1\mid-9)$.

Swap rows 2 and 3 so the next pivot (the useful leading number) is the easier number $1$. Then use it to clear the $y$-coefficient below:

$$
\left(
\begin{array}{ccc|c}
1&1&1&6\\
0&1&-2&-4\\
0&-3&-1&-9
\end{array}
\right)
\xrightarrow{R_3\leftarrow R_3+3R_2}
\left(
\begin{array}{ccc|c}
1&1&1&6\\
0&1&-2&-4\\
0&0&-7&-21
\end{array}
\right).
$$

Now the bottom row says $-7z=-21$, so $z=3$. Work upward:

$$
y-2z=-4 \quad\Longrightarrow\quad y-6=-4 \quad\Longrightarrow\quad y=2,
$$

$$
x+y+z=6 \quad\Longrightarrow\quad x+2+3=6 \quad\Longrightarrow\quad x=1.
$$

So the solution is

$$
\boxed{(x,y,z)=(1,2,3)}.
$$

## Check the answer

Put the numbers back into every original equation:

$$
1+2+3=6,\qquad 2(1)-2+3=3,\qquad 1+2(2)-3=2.
$$

All three clues check out! The matrix helped us organize the work, elimination made the unknowns easier to find, and substitution confirmed that our answer is right.
