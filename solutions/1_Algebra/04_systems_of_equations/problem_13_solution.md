# Exercise 13. Does Every Equation Add New Information?

Consider the system

$$
x_1+x_2=10,\qquad x_2+x_3=8,\qquad x_1-x_3=2.
$$

Solve it and check whether all three equations are independently necessary to describe the solution set. If one follows from the others, show this by calculation.

## Solution

Subtract the second equation from the first:

$$
(x_1+x_2)-(x_2+x_3)=10-8
\quad\Longrightarrow\quad x_1-x_3=2.
$$

Thus the third equation follows from the first two and is redundant. Let $x_2=t$. The first two equations then give

$$
x_1=10-t,\qquad x_3=8-t.
$$

All solutions are $(x_1,x_2,x_3)=(10-t,t,8-t)$ for $t\in\mathbb{R}$. The first two equations are sufficient; the third imposes no additional restriction.