# BEGIN PROB

Let $\vec{x} = \begin{bmatrix} x_1 \\ x_2 \end{bmatrix}$. Consider the
function $g(\vec{x}) = x_1^2 + x_2^2 + x_1 x_2 - 4x_1 - 6x_2 + 8$.

# BEGIN SUBPROB

Find $\nabla g(\vec{x})$, the gradient of $g(\vec{x})$, and use it to
show that
$\nabla g\left( \begin{bmatrix} 1 \\ 2 \end{bmatrix} \right) = \begin{bmatrix} 0 \\ -1 \end{bmatrix}$.


# BEGIN SOLUTION

$\begin{bmatrix} 2x_1 + x_2 - 4 \\ 2x_2 + x_1 - 6 \end{bmatrix}$

TODO

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

We'd like to find the vector $\vec{x}^*$ that minimizes $g(\vec{x})$
using gradient descent. Perform one iteration of gradient descent by
hand, using the initial guess
$\vec{x}^{(0)} = \begin{bmatrix} 1 \\ 2 \end{bmatrix}$ and the learning
rate $\alpha = \frac{1}{4}$. Show your work, and put a
$\boxed{\text{box}}$ around your final answer for $\vec{x}^{(1)}$.

# BEGIN SOLUTION

Correctly finds $$\vec x^{(1)} = \begin{pmatrix} 1 \\ \frac94\end{pmatrix}$$

TODO

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

Given some new function $f(x)$ that is convex, prove that the function
$g(x) = a f(x) + b$ is also convex, where $a$ and $b$ are positive real
constants.

Note: this function $g(\cdot)$ is entirely different from $g(\vec{x})$
on the previous page.

*Hint: Use the fact that we already know $f(x)$ is convex and the formal
definition of convexity: for all
$t\in[0, 1], \ (1-t) f(c) + t f(d) \geq f\left((1-t)c + td\right)$.*


# BEGIN SOLUTION

TODO

# END SOLUTION

# END SUBPROB

# END PROB