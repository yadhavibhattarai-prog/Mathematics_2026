# Exercise 3. Vector Normalization

For $v=(3,4)$, find a unit vector $e$ with the same direction and orientation. Check that $\|e\|=1$, reconstruct $v$ as $v=\|v\|e$, and explain what changes during normalization and what remains unchanged.

## Solution

First, $\|v\|=\sqrt{3^2+4^2}=5$. Dividing by this positive length gives the unit vector

$$e=\frac{v}{\|v\|}=\left(\frac35,\frac45\right).$$

Indeed,

$$\|e\|=\sqrt{\frac9{25}+\frac{16}{25}}=1,$$

and reconstruction yields

$$\|v\|e=5\left(\frac35,\frac45\right)=(3,4)=v.$$

Normalization changes the length to one while preserving the direction and orientation because division is by the positive scalar $5$.