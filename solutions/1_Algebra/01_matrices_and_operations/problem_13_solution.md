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
5(1)+3(1) & 5(1)+3(0)\\
3(1)+2(1) & 3(1)+2(0)
\end{pmatrix}\\
&=
\begin{pmatrix}
8 & 5\\
5 & 3
\end{pmatrix}
\end{aligned}
$$

Thus,

$$
\boxed{
F^5=
\begin{pmatrix}
8 & 5\\
5 & 3
\end{pmatrix}
}
$$

### Step 5: Compare the Results with the Fibonacci Sequence

The Fibonacci sequence is:

$$
0,1,1,2,3,5,8,\ldots
$$

Each term is obtained by adding the two preceding terms:

$$
F_n=F_{n-1}+F_{n-2}
$$

The computed matrix powers are:

$$
F^1=
\begin{pmatrix}
1 & 1\\
1 & 0
\end{pmatrix}
$$

$$
F^2=
\begin{pmatrix}
2 & 1\\
1 & 1
\end{pmatrix}
$$

$$
F^3=
\begin{pmatrix}
3 & 2\\
2 & 1
\end{pmatrix}
$$

$$
F^4=
\begin{pmatrix}
5 & 3\\
3 & 2
\end{pmatrix}
$$

$$
F^5=
\begin{pmatrix}
8 & 5\\
5 & 3
\end{pmatrix}
$$

Notice that the entries follow the Fibonacci sequence. Specifically, for $n\geq 1$,

$$
\boxed{
F^n=
\begin{pmatrix}
F_{n+1} & F_n\\
F_n & F_{n-1}
\end{pmatrix}
}
$$

Here, $F_0=0$ and $F_1=1$ denote the Fibonacci numbers.

For example,

$$
F^5=
\begin{pmatrix}
F_6 & F_5\\
F_5 & F_4
\end{pmatrix}
=
\begin{pmatrix}
8 & 5\\
5 & 3
\end{pmatrix}
$$

This shows that **the entries of the powers of matrix $F$ are Fibonacci numbers**.

### Step 6: Compute $F\begin{pmatrix}a\\b\end{pmatrix}$

Let the vector be:

$$
x=
\begin{pmatrix}
a\\
b
\end{pmatrix}
$$

Multiply it by $F$:

$$
\begin{aligned}
Fx
&=
\begin{pmatrix}
1 & 1\\
1 & 0
\end{pmatrix}
\begin{pmatrix}
a\\
b
\end{pmatrix}\\
&=
\begin{pmatrix}
1(a)+1(b)\\
1(a)+0(b)
\end{pmatrix}\\
&=
\begin{pmatrix}
a+b\\
a
\end{pmatrix}
\end{aligned}
$$

Therefore,

$$
\boxed{
F
\begin{pmatrix}
a\\
b
\end{pmatrix}
=
\begin{pmatrix}
a+b\\
a
\end{pmatrix}
}
$$

### Step 7: Explain the Recurrence Step

Suppose the vector contains two consecutive terms of a sequence:

$$
x=
\begin{pmatrix}
a\\
b
\end{pmatrix}
$$

Multiplication by $F$ produces:

$$
\begin{pmatrix}
a\\
b
\end{pmatrix}
\longrightarrow
\begin{pmatrix}
a+b\\
a
\end{pmatrix}
$$

This performs two actions:

1. **Create the next term:** Add the two existing terms to obtain $a+b$.
2. **Keep the previous term:** Move $a$ into the second position so it can be used in the next step.

For example, starting with the vector

$$
\begin{pmatrix}
1\\
0
\end{pmatrix},
$$

we obtain:

$$
\begin{pmatrix}
1 & 1\\
1 & 0
\end{pmatrix}
\begin{pmatrix}
1\\
0
\end{pmatrix}
=
\begin{pmatrix}
1\\
1
\end{pmatrix}
$$

The next step gives:

$$
\begin{pmatrix}
1 & 1\\
1 & 0
\end{pmatrix}
\begin{pmatrix}
1\\
1
\end{pmatrix}
=
\begin{pmatrix}
2\\
1
\end{pmatrix}
$$

Continuing:

$$
\begin{pmatrix}
2\\
1
\end{pmatrix}
\longrightarrow
\begin{pmatrix}
3\\
2
\end{pmatrix}
\longrightarrow
\begin{pmatrix}
5\\
3
\end{pmatrix}
\longrightarrow
\begin{pmatrix}
8\\
5
\end{pmatrix}
$$

The Fibonacci numbers are generated one step at a time.

### Final Answer

The matrix powers are:

$$
\boxed{
F^2=
\begin{pmatrix}
2 & 1\\
1 & 1
\end{pmatrix},
\quad
F^3=
\begin{pmatrix}
3 & 2\\
2 & 1
\end{pmatrix}
}
$$

$$
\boxed{
F^4=
\begin{pmatrix}
5 & 3\\
3 & 2
\end{pmatrix},
\quad
F^5=
\begin{pmatrix}
8 & 5\\
5 & 3
\end{pmatrix}
}
$$

The general relationship is:

$$
\boxed{
F^n=
\begin{pmatrix}
F_{n+1} & F_n\\
F_n & F_{n-1}
\end{pmatrix}
}
$$

The recurrence step is:

$$
\boxed{
F
\begin{pmatrix}
a\\
b
\end{pmatrix}
=
\begin{pmatrix}
a+b\\
a
\end{pmatrix}
}
$$

**Conclusion:** Matrix multiplication can represent a recurrence relation. Repeatedly multiplying by $F$ generates consecutive Fibonacci numbers by adding the current pair and carrying one term forward to the next step.
