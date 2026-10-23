### Exercise 3. When Can Matrices Be Multiplied?
The matrix sizes are

$$
A_{2\times3},\qquad B_{3\times4},\qquad C_{4\times2},\qquad D_{2\times2}.
$$

For the products

$$
AB,\quad BA,\quad BC,\quad CB,\quad AC,\quad CA,\quad AD,\quad DA
$$

determine whether they are defined. If so, state the size of the result. Justify each decision using the dimension compatibility condition.

> **Why this exercise:** forces an understanding of dimension compatibility before carrying out any calculation.

## Solution

## Dimension Compatibility Condition

Matrix multiplication is defined only when the number of columns in the first matrix equals the number of rows in the second matrix.

If matrix $A$ has size $m\times n$ and matrix $B$ has size $p\times q$, the product $AB$ is defined if and only if

$$
n = p
$$

When this condition is satisfied, the resulting product matrix has size

$$
m \times q
$$

---

### 1. Check $AB$

Given:

$$
A_{2\times3},\qquad B_{3\times4}
$$

The number of columns of $A$ is 3, and the number of rows of $B$ is 3.

Since $3 = 3$, the condition is satisfied and the product $AB$ is defined.

The resulting matrix has the outer dimensions: $2\times 4$.

---

### 2. Check $BA$

Given:

$$
B_{3\times4},\qquad A_{2\times3}
$$

The number of columns of $B$ is 4, and the number of rows of $A$ is 2.

Since $4 \neq 2$, the inner dimensions do not match, so the product $BA$ is not defined.

---

### 3. Check $BC$

Given:

$$
B_{3\times4},\qquad C_{4\times2}
$$

The number of columns of $B$ is 4, and the number of rows of $C$ is 4.

Since $4 = 4$, the condition is satisfied and the product $BC$ is defined.

The resulting matrix has the outer dimensions: $3\times 2$.

---

### 4. Check $CB$

Given:

$$
C_{4\times2},\qquad B_{3\times4}
$$

The number of columns of $C$ is 2, and the number of rows of $B$ is 3.

Since $2 \neq 3$, the inner dimensions do not match, so the product $CB$ is not defined.

---

### 5. Check $AC$

Given:

$$
A_{2\times3},\qquad C_{4\times2}
$$

The number of columns of $A$ is 3, and the number of rows of $C$ is 4.

Since $3 \neq 4$, the inner dimensions do not match, so the product $AC$ is not defined.

---

### 6. Check $CA$

Given:

$$
C_{4\times2},\qquad A_{2\times3}
$$

The number of columns of $C$ is 2, and the number of rows of $A$ is 2.

Since $2 = 2$, the condition is satisfied and the product $CA$ is defined.

The resulting matrix has the outer dimensions: $4\times 3$.

---

### 7. Check $AD$

Given:

$$
A_{2\times3},\qquad D_{2\times2}
$$

The number of columns of $A$ is 3, and the number of rows of $D$ is 2.

Since $3 \neq 2$, the inner dimensions do not match, so the product $AD$ is not defined.

---

### 8. Check $DA$

Given:

$$
D_{2\times2},\qquad A_{2\times3}
$$

The number of columns of $D$ is 2, and the number of rows of $A$ is 2.

Since $2 = 2$, the condition is satisfied and the product $DA$ is defined.

The resulting matrix has the outer dimensions: $2\times 3$.

---

## Summary of Results

A matrix product is defined when the number of columns in the first matrix equals the number of rows in the second matrix. The resulting matrix takes the row count of the first matrix and the column count of the second matrix.

| Product | Inner dimensions check | Defined? | Result size |
| :--- | :--- | :--- | :--- |
| $AB$ | $3 = 3$ | Yes | $2\times4$ |
| $BA$ | $4 \neq 2$ | No | — |
| $BC$ | $4 = 4$ | Yes | $3\times2$ |
| $CB$ | $2 \neq 3$ | No | — |
| $AC$ | $3 \neq 4$ | No | — |
| $CA$ | $2 = 2$ | Yes | $4\times3$ |
| $AD$ | $3 \neq 2$ | No | — |
| $DA$ | $2 = 2$ | Yes | $2\times3$ |

Therefore, the products $AB$, $BC$, $CA$, and $DA$ are defined, whereas $BA$, $CB$, $AC$, and $AD$ are not defined.
