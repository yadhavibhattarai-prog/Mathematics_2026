# Exercise 15. Comparing Directions Using the Cosine of the Angle

Given $a=(1,2,1)$, $b=(2,4,2)$, and $c=(2,0,3)$, compute $\frac{u\cdot v}{\|u\|\,\|v\|}$ for each pair. Order the pairs by increasing angle. Explain why the value for $a,b$ is $1$ even though the vectors have different lengths.

## Solution

For the first pair, $b=2a$, and

$$\frac{a\cdot b}{\|a\|\|b\|}=\frac{12}{\sqrt6\sqrt{24}}=1.$$

This value is one because multiplying by a positive scalar changes length but not direction, so the angle between $a$ and $b$ is zero.

For the pair $a,c$,

$$\frac{a\cdot c}{\|a\|\|c\|}=\frac{5}{\sqrt6\sqrt{13}}=\frac5{\sqrt{78}}.$$

For the remaining pair,

$$\frac{b\cdot c}{\|b\|\|c\|}=\frac{10}{\sqrt{24}\sqrt{13}}=\frac5{\sqrt{78}}.$$

Because cosine decreases as the angle increases on $[0,\pi]$, the increasing-angle order is

$$(a,b)\quad\text{first},\qquad (a,c)=(b,c)\quad\text{tied afterward}.$$