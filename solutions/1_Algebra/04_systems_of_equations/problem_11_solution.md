# Exercise 11. A Parameter in a System of Three Equations

Analyze the number of solutions depending on $t$:

$$
\begin{cases}
x+y+z=1, \\
x+ty+z=2, \\
x+y+tz=3.
\end{cases}
$$

Use the matrix method and separately analyze the parameter values for which a standard calculation step ceases to be valid.

## Solution

### Step 1: Write the augmented matrix

The augmented matrix is

$$
\left[
\begin{array}{ccc|c}
1 & 1 & 1 & 1 \\
1 & t & 1 & 2 \\
1 & 1 & t & 3
\end{array}
\right].
$$

### Step 2: Use row operations

Subtract row 1 from rows 2 and 3:

$$
R_2\leftarrow R_2-R_1,\qquad R_3\leftarrow R_3-R_1.
$$

This gives

$$
\left[
\begin{array}{ccc|c}
1 & 1 & 1 & 1 \\
0 & t-1 & 0 & 1 \\
0 & 0 & t-1 & 2
\end{array}
\right].
$$

### Step 3: Check the exceptional value

If $t=1$, the last two rows become

$$
\left[
\begin{array}{ccc|c}
0 & 0 & 0 & 1 \\
0 & 0 & 0 & 2
\end{array}
\right],
$$
which represents the contradictions $0=1$ and $0=2$.

Therefore, when $t=1$, the system has no solution.

### Step 4: Solve when $t\ne1$

If $t\ne1$, the second and third rows give

$$
y=\frac{1}{t-1},\qquad z=\frac{2}{t-1}.
$$

Substitute these values into the first row, which represents $x+y+z=1$:

$$
x+y+z=1
\quad\Rightarrow\quad
x=1-y-z=1-\frac{1}{t-1}-\frac{2}{t-1}=1-\frac{3}{t-1}.
$$

Thus, for every $t\ne1$, there is exactly one solution:

$$
\boxed{\left(1-\frac{3}{t-1},\;\frac{1}{t-1},\;\frac{2}{t-1}\right)}.
$$

### Final conclusion

- If $t=1$: no solution.
- If $t\ne1$: exactly one solution.
