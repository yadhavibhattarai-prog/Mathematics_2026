# Exercise 3: When Can Matrices Be Multiplied?

Given the matrix sizes:

\[
A_{2\times3},\qquad B_{3\times4},\qquad
C_{4\times2},\qquad D_{2\times2}
\]

We need to determine whether the following products are defined:

\[
AB,\quad BA,\quad BC,\quad CB,\quad AC,\quad CA,\quad AD,\quad DA
\]

## Dimension Compatibility Condition

Matrix multiplication is possible only when the number of columns of the first matrix equals the number of rows of the second matrix.

If

\[
A_{m\times n}B_{p\times q}
\]

then the product is defined only if

\[
\boxed{n=p}
\]

When multiplication is possible, the resulting matrix has the size

\[
\boxed{m\times q}
\]

In simple words, the **inside dimensions must match**, and the **outside dimensions give the result**.

## 1. Check \(AB\)

Given:

\[
A_{2\times3},\qquad B_{3\times4}
\]

The number of columns of \(A\) is \(3\), and the number of rows of \(B\) is \(3\).

Since \(3=3\), the product is defined.

The result has the outside dimensions \(2\times4\).

\[
\boxed{AB\text{ is defined; size }2\times4}
\]

## 2. Check \(BA\)

Given:

\[
B_{3\times4},\qquad A_{2\times3}
\]

The number of columns of \(B\) is \(4\), and the number of rows of \(A\) is \(2\).

Since \(4\neq2\), the product is not defined.

\[
\boxed{BA\text{ is not defined}}
\]

## 3. Check \(BC\)

Given:

\[
B_{3\times4},\qquad C_{4\times2}
\]

The number of columns of \(B\) is \(4\), and the number of rows of \(C\) is \(4\).

Since \(4=4\), the product is defined.

The result has the outside dimensions \(3\times2\).

\[
\boxed{BC\text{ is defined; size }3\times2}
\]

## 4. Check \(CB\)

Given:

\[
C_{4\times2},\qquad B_{3\times4}
\]

The number of columns of \(C\) is \(2\), and the number of rows of \(B\) is \(3\).

Since \(2\neq3\), the product is not defined.

\[
\boxed{CB\text{ is not defined}}
\]

## 5. Check \(AC\)

Given:

\[
A_{2\times3},\qquad C_{4\times2}
\]

The number of columns of \(A\) is \(3\), and the number of rows of \(C\) is \(4\).

Since \(3\neq4\), the product is not defined.

\[
\boxed{AC\text{ is not defined}}
\]

## 6. Check \(CA\)

Given:

\[
C_{4\times2},\qquad A_{2\times3}
\]

The number of columns of \(C\) is \(2\), and the number of rows of \(A\) is \(2\).

Since \(2=2\), the product is defined.

The result has the outside dimensions \(4\times3\).

\[
\boxed{CA\text{ is defined; size }4\times3}
\]

## 7. Check \(AD\)

Given:

\[
A_{2\times3},\qquad D_{2\times2}
\]

The number of columns of \(A\) is \(3\), and the number of rows of \(D\) is \(2\).

Since \(3\neq2\), the product is not defined.

\[
\boxed{AD\text{ is not defined}}
\]

## 8. Check \(DA\)

Given:

\[
D_{2\times2},\qquad A_{2\times3}
\]

The number of columns of \(D\) is \(2\), and the number of rows of \(A\) is \(2\).

Since \(2=2\), the product is defined.

The result has the outside dimensions \(2\times3\).

\[
\boxed{DA\text{ is defined; size }2\times3}
\]

## Final Answers

| Product | Dimension check | Defined? | Result size |
|---|---|---|---|
| \(AB\) | \(3=3\) | Yes | \(2\times4\) |
| \(BA\) | \(4\neq2\) | No | — |
| \(BC\) | \(4=4\) | Yes | \(3\times2\) |
| \(CB\) | \(2\neq3\) | No | — |
| \(AC\) | \(3\neq4\) | No | — |
| \(CA\) | \(2=2\) | Yes | \(4\times3\) |
| \(AD\) | \(3\neq2\) | No | — |
| \(DA\) | \(2=2\) | Yes | \(2\times3\) |

**Conclusion:** A matrix product is defined only when the number of columns in the first matrix equals the number of rows in the second matrix. The dimensions of the resulting matrix are determined by the outside dimensions.
