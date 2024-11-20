# BEGIN PROB

Let $\vec{x} = \begin{bmatrix} x_1 \\ x_2 \end{bmatrix}$. Consider the
function $g(\vec{x}) = x_1^2 + x_2^2 + x_1 x_2 - 4x_1 - 6x_2 + 8$.

# BEGIN SUBPROB

Find $\nabla g(\vec{x})$, the gradient of $g(\vec{x})$, and use it to
show that
$\nabla g\left( \begin{bmatrix} 1 \\ 2 \end{bmatrix} \right) = \begin{bmatrix} 0 \\ -1 \end{bmatrix}$.


# BEGIN SOLUTION

$\nabla g(\vec{x}) = \begin{bmatrix} 2x_1 + x_2 - 4 \\ 2x_2 + x_1 - 6 \end{bmatrix}$

To calculate the gradient, we take the partial derivatives of $g$ with respect to both $x_1$ and $x_2$, and arrange these partial derivatives as a vector. 
$$\frac{\partial g}{\partial x_1} = 2x_1 + x_2 - 4$$
$$\frac{\partial g}{\partial x_2} = 2x_2 + x_1 - 6$$
Writing these as a vector, we obtain the gradient above.

We can verify that $\nabla g\left( \begin{bmatrix} 1 \\ 2 \end{bmatrix} \right) = \begin{bmatrix} 2(1) + (2) - 4 \\ 2(2) + (1) - 6 \end{bmatrix} = \begin{bmatrix} 0 \\ -1 \end{bmatrix}$.

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

$\vec x^{(1)} = \begin{pmatrix} 1 \\ \frac94\end{pmatrix}$

Our first step of gradient descent is given by the equation: $\vec{x}^{(1)} = \vec{x}^{(0)} - \alpha \nabla g(\vec{x}^{(0)})$.

From the previous problem, we found that $\nabla g\left( \begin{bmatrix} 1 \\ 2 \end{bmatrix} \right) = \begin{bmatrix} 0 \\ -1 \end{bmatrix}$.

Plugging in what we have: $\vec{x}^{(1)} = \begin{bmatrix} 1 \\ 2 \end{bmatrix} - \left(\frac{1}{4} \right) \begin{bmatrix} 0 \\ -1 \end{bmatrix} = \begin{bmatrix} 1 \\ 2 \end{bmatrix} - \begin{bmatrix} 0 \\ - \frac14\end{bmatrix} = \begin{pmatrix} 1 \\ \frac94\end{pmatrix}$

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

To show that $g(x)$ is convex, we want to begin with the expression $(1-t) g(c) + t g(d)$ and use algebra to show it's $\geq g\left((1-t)c + td\right)$.

Let $t\in[0, 1], a\in\mathbb{R}, b\in\mathbb{R}$.

\begin{align*}
(1-t) g(c) + t g(d) &= (1-t)(af(c) + b) + t(af(d) + b)\\
&= (1-t)(af(c)) + (1-t)b + t(af(d)) + tb\\
&= (1-t)(af(c)) + t(af(d)) + b - tb + tb\\
&= a((1-t)f(c) + tf(d)) + b\\
&/geq af((1-t)c + td) + b\\
&= g((1-t)c + td)
\end{align*}

# END SOLUTION

# END SUBPROB

# END PROB