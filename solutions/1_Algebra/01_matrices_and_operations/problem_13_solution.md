### Exercise 13. A Recurrence Written in Matrix Form

Given:

$$
F=
\begin{pmatrix}
1 & 1\\
1 & 0
\end{pmatrix}
$$

We need to compute $F^2$, $F^3$, $F^4$, and $F^5$, compare the results with the Fibonacci sequence, and explain how multiplying $F$ by a vector performs one recurrence step.

### Step 1: Compute $F^2$

By definition,

$$
F^2=F\cdot F
$$

Therefore,

$$
\begin{aligned}
F^2
&=
\begin{pmatrix}
1 & 1\\
1 & 0
\end{pmatrix}
\begin{pmatrix}
1 & 1\\
1 & 0
\end{pmatrix}\\
&=
\begin{pmatrix}
1(1)+1(1) & 1(1)+1(0)\\
1(1)+0(1) & 1(1)+0(0)
\end{pmatrix}\\
&=
\begin{pmatrix}
2 & 1\\
1 & 1
\end{pmatrix}
\end{aligned}
$$

Thus,

$$
\boxed{
F^2=
\begin{pmatrix}
2 & 1\\
1 & 1
\end{pmatrix}
}
$$

### Step 2: Compute $F^3$

We know that

$$
F^3=F^2F
$$

Substituting the value of $F^2$:

$$
\begin{aligned}
F^3
&=
\begin{pmatrix}
2 & 1\\
1 & 1
\end{pmatrix}
\begin{pmatrix}
1 & 1\\
1 & 0
\end{pmatrix}\\
&=
\begin{pmatrix}
2(1)+1(1) & 2(1)+1(0)\\
1(1)+1(1) & 1(1)+1(0)
\end{pmatrix}\\
&=
\begin{pmatrix}
3 & 2\\
2 & 1
\end{pmatrix}
\end{aligned}
$$

Thus,

$$
\boxed{
F^3=
\begin{pmatrix}
3 & 2\\
2 & 1
\end{pmatrix}
}
$$

### Step 3: Compute $F^4$

We know that

$$
F^4=F^3F
$$

Therefore,

$$
\begin{aligned}
F^4
&=
\begin{pmatrix}
3 & 2\\
2 & 1
\end{pmatrix}
\begin{pmatrix}
1 & 1\\
1 & 0
\end{pmatrix}\\
&=
\begin{pmatrix}
3(1)+2(1) & 3(1)+2(0)\\
2(1)+1(1) & 2(1)+1(0)
\end{pmatrix}\\
&=
\begin{pmatrix}
5 & 3\\
3 & 2
\end{pmatrix}
\end{aligned}
$$

Thus,

$$
\boxed{
F^4=
\begin{pmatrix}
5 & 3\\
3 & 2
\end{pmatrix}
}
$$

### Step 4: Compute $F^5$

We know that

$$
F^5=F^4F
$$

Therefore,

$$
\begin{aligned}
F^5
&=
\begin{pmatrix}
5 & 3\\
3 & 2
\end{pmatrix}
\begin{pmatrix}
1 & 1\\
1 & 0
\end{pmatrix}\\
&=
\begin{pmatrix}
5(1)+3(1) & 5(
