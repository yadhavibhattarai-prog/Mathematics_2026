# Exercise 1. Dominant Terms in a Sequence

## Problem

Compute

$$
\lim_{n\to\infty}\frac{4n^2-3n+1}{2n^2+5n-7}.
$$

Explain why the highest-degree terms determine the result.

---

## Solution

### Step 1: Factor out the highest power of $n$

Both numerator and denominator have degree 2, so divide each by $n^2$:

$$
\frac{4n^2-3n+1}{2n^2+5n-7}
=\frac{n^2\left(4-\frac{3}{n}+\frac{1}{n^2}\right)}{n^2\left(2+\frac{5}{n}-\frac{7}{n^2}\right)}
=\frac{4-\frac{3}{n}+\frac{1}{n^2}}{2+\frac{5}{n}-\frac{7}{n^2}}.
$$

### Step 2: Use the basic limits

For any constant $c$ and any $k\ge 1$:

$$
\lim_{n\to\infty}\frac{c}{n^k}=0.
$$

So

$$
\frac{3}{n}\to 0,\quad \frac{1}{n^2}\to 0,\quad \frac{5}{n}\to 0,\quad \frac{7}{n^2}\to 0.
$$

### Step 3: Apply the limit laws

Since the denominator's limit is $2\neq 0$, the quotient law applies:

$$
\lim_{n\to\infty}\frac{4-\frac{3}{n}+\frac{1}{n^2}}{2+\frac{5}{n}-\frac{7}{n^2}}
=\frac{4-0+0}{2+0-0}=\frac{4}{2}=2.
$$

### Answer

$$
\boxed{\lim_{n\to\infty}\frac{4n^2-3n+1}{2n^2+5n-7}=2}
$$

---

## Why the highest-degree terms determine the result

For large $n$, powers of $n$ grow at very different rates. The ratio of a lower-degree term to the leading term shrinks to zero:

$$
\frac{3n}{4n^2}=\frac{3}{4n}\to 0,
\qquad
\frac{1}{4n^2}\to 0.
$$

So $-3n+1$ becomes negligible compared with $4n^2$, and $5n-7$ becomes negligible compared with $2n^2$. In other words:

$$
4n^2-3n+1 = 4n^2\,(1+o(1)), \qquad 2n^2+5n-7 = 2n^2\,(1+o(1)),
$$

where $o(1)$ denotes a quantity tending to $0$. Therefore

$$
\frac{4n^2-3n+1}{2n^2+5n-7}\sim\frac{4n^2}{2n^2}=2 \quad (n\to\infty).
$$

### Numerical sanity check

| $n$    | $\dfrac{4n^2-3n+1}{2n^2+5n-7}$ |
|--------|-------------------------------|
| 10     | $\dfrac{271}{243}\approx 1.115$ |
| 100    | $\dfrac{39701}{20493}\approx 1.937$ |
| 1000   | $\dfrac{3997001}{2004993}\approx 1.993$ |

The values approach $2$, consistent with the result.

---

## General rule

For polynomials $P(n)$ of degree $p$ with leading coefficient $a_p$ and $Q(n)$ of degree $q$ with leading coefficient $b_q$:

$$
\lim_{n\to\infty}\frac{P(n)}{Q(n)}=
\begin{cases}
\dfrac{a_p}{b_q}, & p=q,\\[2mm]
0, & p<q,\\[1mm]
\pm\infty, & p>q.
\end{cases}
$$

Here $p=q=2$, $a_p=4$, $b_q=2$, so the limit is $4/2=2$.
