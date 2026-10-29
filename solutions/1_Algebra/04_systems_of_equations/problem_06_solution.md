# Exercise 6. A System with a Parameter — Which Cases Actually Occur?

Analyze, depending on the parameter $a$, the system

$$
\begin{cases}
x+y=2, \\
ax+ay=4.
\end{cases}
$$

Among the three possibilities — exactly one solution, infinitely many solutions, no solution — determine which actually occur and for which values of $a$. If one type cannot occur, explain why.

## Solution

The second left-hand side is $a(x+y)$. The first equation therefore forces the second left-hand side to equal $2a$, so consistency requires $2a=4$, or $a=2$.

- If $a=2$, the second equation is twice the first. The system has infinitely many solutions: $(x,y)=(t,2-t)$ for any real $t$.
- If $a\ne2$, the equations require both $x+y=2$ and $x+y=4/a$ when $a\ne0$, which are incompatible; for $a=0$, the second equation itself is $0=4$, also impossible. Thus there is no solution.

There is no value of $a$ giving exactly one solution: whenever consistent, the equations are dependent and leave one free variable.