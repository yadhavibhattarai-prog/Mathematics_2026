# Problem 13. A Multi-Layer Composition

For

$$
f(x)=e^{\sin(x^2)}
$$

compute the derivative. First write the layers

$$
x\longrightarrow x^2\longrightarrow \sin(x^2)\longrightarrow e^{\sin(x^2)}
$$

and explain why differentiation moves through them in the reverse order.

> **Why this problem:** it develops the chain rule as a method for working with multiple layers.

## Solution

### 1. The Forward Evaluation Layers

Evaluating the function at an input $x$ proceeds from the inside out through three distinct layers:

$$
x\longrightarrow x^2\longrightarrow \sin(x^2)\longrightarrow e^{\sin(x^2)}
$$

Define the intermediate variables explicitly:
1. **Innermost layer ($u_1$):**
   
$$
u_1 = x^2
$$

2. **Middle layer ($u_2$):**
   
$$
u_2 = \sin(u_1) = \sin(x^2)
$$

3. **Outermost layer ($y$):**
   
$$
y = e^{u_2} = e^{\sin(x^2)}
$$

---

### 2. Why Differentiation Moves in Reverse Order

In Leibniz notation, the multi-layer chain rule expresses the total rate of change as a product of intermediate rates:

$$
\frac{dy}{dx} = \frac{dy}{du_2} \cdot \frac{du_2}{du_1} \cdot \frac{du_1}{dx}
$$

Differentiation moves through the layers in the **reverse order** (from outside to inside):

1. **The outermost envelope determines the primary functional identity:**
   The function presents itself first and foremost as an exponential function $e^{(\dots)}$. Any rate calculation must first determine how an exponential reacts to changes in its exponent:

$$
\frac{dy}{du_2} = e^{u_2}
$$

2. **The chain of sensitivity transfers inwards:**
   The exponent is not an independent parameter; it is controlled by the sine function. The next factor must quantify how the sine reacts to changes in its internal argument:

$$
\frac{du_2}{du_1} = \cos(u_1)
$$

3. **Reaching the root independent variable:**
   Finally, the argument of the sine is controlled by the quadratic term $x^2$. The final factor captures how fast this inner square changes with respect to $x$:

$$
\frac{du_1}{dx} = 2x
$$

While function evaluation proceeds from **input to output** ($x \to u_1 \to u_2 \to y$), the chain rule works by "peeling the onion" from **output sensitivity back to the input** ($y \to u_2 \to u_1 \to x$).

---

### 3. Computation of the Derivatives of Each Layer

- **Layer 3 (outermost):**

$$
\frac{dy}{du_2} = \frac{d}{du_2}\left(e^{u_2}\right) = e^{u_2} = e^{\sin(x^2)}
$$

- **Layer 2 (middle):**

$$
\frac{du_2}{du_1} = \frac{d}{du_1}\left(\sin u_1\right) = \cos u_1 = \cos(x^2)
$$

- **Layer 1 (innermost):**

$$
\frac{du_1}{dx} = \frac{d}{dx}(x^2) = 2x
$$

---

### 4. Combining the Factors

Multiply the three derivatives together:

$$
\begin{aligned}
f'(x) &= \frac{dy}{du_2} \cdot \frac{du_2}{du_1} \cdot \frac{du_1}{dx} \\
&= e^{\sin(x^2)} \cdot \cos(x^2) \cdot 2x \\
&= 2x\cos(x^2)e^{\sin(x^2)}
\end{aligned}
$$

