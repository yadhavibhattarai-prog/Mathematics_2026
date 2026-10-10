### Exercise 8. Row Operations and Their Reversibility

Given:

$$
A=
\begin{pmatrix}
1 & 2 & -1 \\
2 & 4 & 1 \\
-1 & 1 & 3
\end{pmatrix}
$$

### Step 1: Apply $R_2 \leftarrow R_2-2R_1$

The first row is:

$$
R_1=(1,2,-1)
$$

The second row is:

$$
R_2=(2,4,1)
$$

Subtract twice the first row from the second row:

$$
\begin{aligned}
R_2-2R_1
&=(2,4,1)-2(1,2,-1)\\
&=(2,4,1)-(2,4,-2)\\
&=(0,0,3)
\end{aligned}
$$

The matrix after Step 1 is:

$$
A_1=
\begin{pmatrix}
1 & 2 & -1\\
0 & 0 & 3\\
-1 & 1 & 3
\end{pmatrix}
$$

**Reverse operation:** $R_2 \leftarrow R_2+2R_1$

Adding twice the first row back to the second row restores the original second row.

---

### Step 2: Apply $R_3 \leftarrow R_3+R_1$

The third row is:

$$
R_3=(-1,1,3)
$$

Add the first row to the third row:

$$
\begin{aligned}
R_3+R_1
&=(-1,1,3)+(1,2,-1)\\
&=(0,3,2)
\end{aligned}
$$

The matrix after Step 2 is:

$$
A_2=
\begin{pmatrix}
1 & 2 & -1\\
0 & 0 & 3\\
0 & 3 & 2
\end{pmatrix}
$$

**Reverse operation:** $R_3 \leftarrow R_3-R_1$

Subtracting the first row from the third row restores the previous third row.

---

### Step 3: Interchange $R_2$ and $R_3$

Swap the second and third rows:

$$
A_3=
\begin{pmatrix}
1 & 2 & -1\\
0 & 3 & 2\\
0 & 0 & 3
\end{pmatrix}
$$

**Reverse operation:** Interchange $R_2$ and $R_3$ again.

Swapping the same two rows a second time restores the previous matrix.

---

### Final Answer

The matrices after each operation are:

$$
A_1=
\begin{pmatrix}
1 & 2 & -1\\
0 & 0 & 3\\
-1 & 1 & 3
\end{pmatrix}
$$

$$
A_2=
\begin{pmatrix}
1 & 2 & -1\\
0 & 0 & 3\\
0 & 3 & 2
\end{pmatrix}
$$

$$
A_3=
\begin{pmatrix}
1 & 2 & -1\\
0 & 3 & 2\\
0 & 0 & 3
\end{pmatrix}
$$

| Row operation | Reversing operation |
|---|---|
| $R_2 \leftarrow R_2-2R_1$ | $R_2 \leftarrow R_2+2R_1$ |
| $R_3 \leftarrow R_3+R_1$ | $R_3 \leftarrow R_3-R_1$ |
| Swap $R_2$ and $R_3$ | Swap $R_2$ and $R_3$ again |

### Explanation

Elementary row operations are **reversible** because each operation has an inverse operation that restores the previous matrix. This property is important in Gaussian elimination, where row operations simplify matrices while preserving the solutions of the corresponding system of linear equations.
