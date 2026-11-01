## Question

### Problem 8. Number of Requests Handled by a Server

The rate at which requests arrive at a server during the first 5 minutes is described by the function

$$
r(t)=100+20t\quad [\mathrm{requests/min}],\qquad 0\le t\le5.
$$

1. Compute the total number of requests that arrived during this time.
2. Compute the average rate of incoming requests over this interval.
3. Compare the average rate with the values $r(0)$ and $r(5)$.

## Solution

### 1. Total number of requests

The total number of requests is the integral of the rate over time:

$$
\int_0^5 (100+20t)\,dt.
$$

Compute:

$$
\int_0^5 (100+20t)\,dt = \left[100t+10t^2\right]_0^5.
$$

Evaluate:

$$
100(5)+10(25)=500+250=750.
$$

So the total number of requests is

$$
\boxed{750}.
$$

### 2. Average rate of incoming requests

The average rate over the interval is

$$
\frac{1}{5-0}\int_0^5 (100+20t)\,dt = \frac{750}{5}=150.
$$

Thus the average rate is

$$
\boxed{150\text{ requests/min}}.
$$

### 3. Compare with $r(0)$ and $r(5)$

$$
r(0)=100,
\qquad
r(5)=100+20(5)=200.
$$

So,

$$
100<150<200.
$$

This makes sense because the rate function is linear and increasing. The average value of a linear function on an interval is the midpoint of its endpoint values.

Hence,

$$
\text{average rate}=\frac{r(0)+r(5)}{2}=\frac{100+200}{2}=150.
$$
