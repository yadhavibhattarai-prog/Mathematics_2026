# Exercise 7. Choosing a Method Deliberately

Do not solve all of the following systems completely. For each situation, choose the method that best uses its structure and justify your choice:

1. one system with a triangular coefficient matrix

$$
\begin{cases}
2x-y=3, \\
4y=8;
\end{cases}
$$

2. three systems $Ax=b_i$ with the same invertible matrix $A$, when $A^{-1}$ is already known;
3. one $3\times3$ system for which the inverse matrix is not given and the goal is only to find one solution vector.

For case 1, carry out the chosen method completely. For cases 2 and 3, describe the plan and indicate which part of the computation would be reusable or unnecessary. Do not judge a method by its name alone — refer to the number of right-hand sides and the structure of the matrix.

## Solution

1. Use back-substitution, since the system is triangular. The second equation gives $y=2$; substituting into the first gives $2x-2=3$, so $x=5/2$. The solution is $(x,y)=(5/2,2)$.
2. Since $A^{-1}$ is already known and there are three right-hand sides, compute each solution as $x_i=A^{-1}b_i$. The same inverse is reused for all three systems; no elimination of the coefficient matrix is needed.
3. Use Gaussian elimination on the augmented matrix for the single right-hand side. It finds the needed solution directly. Computing the entire inverse would do extra work that is unnecessary when only one solution vector is required.