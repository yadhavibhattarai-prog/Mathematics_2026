# Exercise 13. Do Four Points Lie in One Plane?

Given $A=(0,0,0)$, $B=(1,2,0)$, $C=(0,1,1)$, and $D=(2,5,1)$: (1) construct $\overrightarrow{AB}$ and $\overrightarrow{AC}$; (2) find $n=\overrightarrow{AB}\times\overrightarrow{AC}$; (3) construct $\overrightarrow{AD}$ and check whether $\overrightarrow{AD}\cdot n=0$; and (4) decide whether $D$ lies in the plane through $A,B,C$, justifying the criterion.

## Solution

The in-plane candidates are

$$\overrightarrow{AB}=(1,2,0),\qquad \overrightarrow{AC}=(0,1,1).$$

Their cross product is

$$n=\overrightarrow{AB}\times\overrightarrow{AC}=(2,-1,1).$$

Also $\overrightarrow{AD}=(2,5,1)$. I compute

$$\overrightarrow{AD}\cdot n=2\cdot2+5(-1)+1\cdot1=4-5+1=0.$$

Since this value is zero, $\overrightarrow{AD}$ is perpendicular to the normal, so $D$ lies in the plane through $A,B,C$. The criterion is that a displacement within the plane must have zero dot product with its normal.