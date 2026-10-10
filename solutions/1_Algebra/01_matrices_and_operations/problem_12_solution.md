### Exercise 12. Formula for a Matrix Power

Given:

$$
A=
\begin{pmatrix}
1 & 1\\
0 & 1
\end{pmatrix}
$$

We need to compute $A^2$, $A^3$, and $A^4$, formulate a conjecture for $A^n$, and prove the formula using mathematical induction.

### Step 1: Compute $A^2$

By definition,

$$
A^2=A\cdot A
$$

Therefore,

$$
\begin{aligned}
A^2
&=
\begin{pmatrix}
1 & 1\\
0 & 1
\end{pmatrix}
\begin{pmatrix}
1 & 1\\
0 & 1
\end{pmatrix}\\
&=
\begin{pmatrix}
1(1)+1(0) & 1(1)+1(1)\\
0(1)+1(0) & 0(1)+1(1)
\end{pmatrix}\\
&=
\begin{pmatrix}
1 & 2\\
0 & 1
\end{pmatrix}
\end{aligned}
$$

Thus,

$$
\boxed{
A^2=
\begin{pmatrix}
1 & 2\\
0 & 1
\end{pmatrix}
}
$$

### Step 2: Compute $A^3$

We know that

$$
A^3=A^2A
$$

Substituting the value of $A^2$:

$$
\begin{aligned}
A^3
&=
\begin{pmatrix}
1 & 2\\
0 & 1
\end{pmatrix}
\begin{pmatrix}
1 & 1\\
0 & 1
\end{pmatrix}\\
&=
\begin{pmatrix}
1(1)+2(0) & 1(1)+2(1)\\
0(1)+1(0) & 0(1)+1(1)
\end{pmatrix}\\
&=
\begin{pmatrix}
1 & 3\\
0 & 1
\end{pmatrix}
\end{aligned}
$$

Thus,

$$
\boxed{
A^3=
\begin{pmatrix}
1 & 3\\
0 & 1
\end{pmatrix}
}
$$

### Step 3: Compute $A^4$

We know that

$$
A^4=A^3A
$$

Substituting the value of $A^3$:

$$
\begin{aligned}
A^4
&=
\begin{pmatrix}
1 & 3\\
0 & 1
\end{pmatrix}
\begin{pmatrix}
1 & 1\\
0 & 1
\end{pmatrix}\\
&=
\begin{pmatrix}
1(1)+3(0) & 1(1)+3(1)\\
0(1)+1(0) & 0(1)+1(1)
\end{pmatrix}\\
&=
\begin{pmatrix}
1 & 4\\
0 & 1
\end{pmatrix}
\end{aligned}
$$

Thus,

$$
\boxed{
A^4=
\begin{pmatrix}
1 & 4\\
0 & 1
\end{pmatrix}
}
$$

### Step 4: Identify the Pattern and Formulate a Conjecture

We have obtained:

$$
A^1=
\begin{pmatrix}
1 & 1\\
0 & 1
\end{pmatrix}
$$

$$
A^2=
\begin{pmatrix}
1 & 2\\
0 & 1
\end{pmatrix}
$$

$$
A^3=
\begin{pmatrix}
1 & 3\\
0 & 1
\end{pmatrix}
$$

$$
A^4=
\begin{pmatrix}
1 & 4\\
0 & 1
\end{pmatrix}
$$

The pattern shows that:

- The top-left entry always remains $1$.
- The top-right entry equals the exponent $n$.
- The bottom-left entry always remains $0$.
- The bottom-right entry always remains $1$.

Therefore, we conjecture that for every positive integer $n$,

$$
\boxed{
A^n=
\begin{pmatrix}
1 & n\\
0 & 1
\end{pmatrix}
}
$$

Now we will prove that this formula holds for every positive integer $n$ using mathematical induction.

### Step 5: Prove the Formula Using Mathematical Induction

**Base case: $n=1$**

For $n=1$, the formula gives:

$$
\begin{pmatrix}
1 & 1\\
0 & 1
\end{pmatrix}
$$

This is exactly the original matrix $A$.

Therefore, the formula is true for $n=1$.

**Inductive hypothesis**

Assume that the formula is true for some positive integer $n$. That is, assume:

$$
A^n=
\begin{pmatrix}
1 & n\\
0 & 1
\end{pmatrix}
$$

We must show that the formula is also true for $n+1$.

**Inductive step**

By the definition of matrix powers,

$$
A^{n+1}=A^nA
$$

Using the inductive hypothesis, substitute the assumed formula for $A^n$:

$$
\begin{aligned}
A^{n+1}
&=
\begin{pmatrix}
1 & n\\
0 & 1
\end{pmatrix}
\begin{pmatrix}
1 & 1\\
0 & 1
\end{pmatrix}
\end{aligned}
$$

Multiply the matrices:

$$
\begin{aligned}
A^{n+1}
&=
\begin{pmatrix}
1(1)+n(0) & 1(1)+n(1)\\
0(1)+1(0) & 0(1)+1(1)
\end{pmatrix}\\
&=
\begin{pmatrix}
1 & 1+n\\
0 & 1
\end{pmatrix}\\
&=
\begin{pmatrix}
1 & n+1\\
0 & 1
\end{pmatrix}
\end{aligned}
$$

This is exactly the proposed formula with $n$ replaced by $n+1$.

Therefore, if the formula holds for $n$, it also holds for $n+1$.

Since the formula is true for $n=1$ and the inductive step is valid, **the formula holds for every positive integer $n$**.

### Final Answer

The first four powers are:

$$
\boxed{
A^2=
\begin{pmatrix}
1 & 2\\
0 & 1
\end{pmatrix},
\quad
A^3=
\begin{pmatrix}
1 & 3\\
0 & 1
\end{pmatrix},
\quad
A^4=
\begin{pmatrix}
1 & 4\\
0 & 1
\end{pmatrix}
}
$$

The general formula is:

$$
\boxed{
A^n=
\begin{pmatrix}
1 & n\\
0 & 1
\end{pmatrix},
\qquad n\geq 1
}
$$

**Conclusion:** The pattern suggests that the top-right entry increases by $1$ each time we multiply by $A$. Mathematical induction proves that this pattern continues for every positive integer $n$.
