# BEGIN PROB
<i>Source: [Summer Session 1 2025 Midterm](../ss1-25-midterm/index.html), Problem 1</i>

Let $\{(x_i,y_i)\}_{i=1}^n$ be a dataset of scalar input-output pairs, and consider the simple linear regression model

$$
f(a, b;\, x) = ax + b,\qquad a, b\in\mathbb{R}.
$$

Let $\gamma > 0$ be a fixed constant which is understood to be separate from the training data and the weights. Define the $\gamma$-risk according to the formula

$$
R_{\gamma}(a, b) = \gamma a^2 + \frac{1}{n}\sum_{i=1}^{n} (y_i - (ax_i + b))^2.
$$

Find closed-form expressions for the global minimizers $a^\ast, b^\ast$ of the $\gamma$-risk for the training data $\{(x_i,y_i)\}_{i=1}^n$. In your solution, you should clearly label and explain each step.

# BEGIN SOLN

### Solution

#### Step 1: Compute Partial Derivatives

We compute the partial derivatives of $R_\gamma(a, b)$ with respect to both parameters.

**Partial derivative with respect to $a$:**

$$
\begin{align*}
\frac{\partial R_\gamma}{\partial a} &= 2\gamma a + \frac{1}{n} \sum_{i=1}^{n} 2(y_i - ax_i - b)(-x_i)\\
&= 2\gamma a - \frac{2}{n} \sum_{i=1}^{n} x_i (y_i - ax_i - b)
\end{align*}
$$

**Partial derivative with respect to $b$:**

$$
\begin{align*}
\frac{\partial R_\gamma}{\partial b} &= \frac{1}{n} \sum_{i=1}^{n} 2(y_i - ax_i - b)(-1)\\
&= -\frac{2}{n} \sum_{i=1}^{n} (y_i - ax_i - b)
\end{align*}
$$

#### Step 2: Set Partial Derivatives to Zero (Normal Equations)

**From $\frac{\partial R_\gamma}{\partial b} = 0$:**

$$
\begin{align*}
-\frac{2}{n} \sum_{i=1}^{n} (y_i - ax_i - b) &= 0\\
\sum_{i=1}^{n} y_i - a\sum_{i=1}^{n} x_i - nb &= 0\\
nb &= \sum_{i=1}^{n} y_i - a\sum_{i=1}^{n} x_i\\
b &= \frac{1}{n}\sum_{i=1}^{n} y_i - \frac{a}{n}\sum_{i=1}^{n} x_i\\
b &= \bar{y} - a\bar{x}
\end{align*}
$$

where $\bar{x} = \frac{1}{n}\sum_{i=1}^{n} x_i$ and $\bar{y} = \frac{1}{n}\sum_{i=1}^{n} y_i$.

**From $\frac{\partial R_\gamma}{\partial a} = 0$:**

$$
\begin{align*}
2\gamma a - \frac{2}{n} \sum_{i=1}^{n} x_i (y_i - ax_i - b) &= 0\\
\gamma a - \frac{1}{n} \sum_{i=1}^{n} x_i y_i + \frac{a}{n}\sum_{i=1}^{n} x_i^2 + \frac{b}{n}\sum_{i=1}^{n} x_i &= 0\\
n\gamma a + a\sum_{i=1}^{n} x_i^2 + b\sum_{i=1}^{n} x_i &= \sum_{i=1}^{n} x_i y_i
\end{align*}
$$

#### Step 3: Solve for $a^*$ by Substituting $b = \bar{y} - a\bar{x}$

Substituting $b = \bar{y} - a\bar{x}$ into the equation above:

$$
\begin{align*}
n\gamma a + a\sum_{i=1}^{n} x_i^2 + (\bar{y} - a\bar{x})\sum_{i=1}^{n} x_i &= \sum_{i=1}^{n} x_i y_i\\
n\gamma a + a\sum_{i=1}^{n} x_i^2 + \bar{y} \cdot n\bar{x} - a\bar{x} \cdot n\bar{x} &= \sum_{i=1}^{n} x_i y_i\\
n\gamma a + a\sum_{i=1}^{n} x_i^2 - an\bar{x}^2 &= \sum_{i=1}^{n} x_i y_i - n\bar{x}\bar{y}\\
a\left(n\gamma + \sum_{i=1}^{n} x_i^2 - n\bar{x}^2\right) &= \sum_{i=1}^{n} x_i y_i - n\bar{x}\bar{y}
\end{align*}
$$

Note that $\sum_{i=1}^{n} x_i^2 - n\bar{x}^2 = \sum_{i=1}^{n} (x_i - \bar{x})^2$ and $\sum_{i=1}^{n} x_i y_i - n\bar{x}\bar{y} = \sum_{i=1}^{n} (x_i - \bar{x})(y_i - \bar{y})$.

Therefore:

$$
a^* = \frac{\sum_{i=1}^{n} (x_i - \bar{x})(y_i - \bar{y})}{\sum_{i=1}^{n} (x_i - \bar{x})^2 + n\gamma}
$$

And:

$$
b^* = \bar{y} - a^*\bar{x}
$$

#### Step 4: Verify that $(a^*, b^*)$ is a Minimizer (Second Derivative Test)

To confirm that the critical point is a minimizer, we compute the Hessian matrix and verify that it is positive definite.

**What is the Hessian matrix?**

The Hessian matrix $H$ is a square matrix containing all second-order partial derivatives of a function. For a function $R_\gamma(a, b)$ with two variables, the Hessian is:

$$
H = \begin{pmatrix}
\frac{\partial^2 R_\gamma}{\partial a^2} & \frac{\partial^2 R_\gamma}{\partial a \partial b}\\
\frac{\partial^2 R_\gamma}{\partial b \partial a} & \frac{\partial^2 R_\gamma}{\partial b^2}
\end{pmatrix}
$$

**How does the Hessian determine convexity and minima?**

- If $H$ is **positive definite** everywhere, then $R_\gamma$ is strictly convex, which means any critical point is a global minimum.
- For a $2 \times 2$ matrix, $H$ is positive definite if and only if:
  1. $H_{11} > 0$ (the top-left entry is positive), and
  2. $\det(H) > 0$ (the determinant is positive)

**Second partial derivatives:**

$$
\begin{align*}
\frac{\partial^2 R_\gamma}{\partial a^2} &= 2\gamma + \frac{2}{n}\sum_{i=1}^{n} x_i^2\\
\frac{\partial^2 R_\gamma}{\partial b^2} &= \frac{2}{n}\sum_{i=1}^{n} 1 = 2\\
\frac{\partial^2 R_\gamma}{\partial a \partial b} &= \frac{2}{n}\sum_{i=1}^{n} x_i = 2\bar{x}
\end{align*}
$$

The Hessian matrix is:

$$
H = \begin{pmatrix}
2\gamma + \frac{2}{n}\sum_{i=1}^{n} x_i^2 & 2\bar{x}\\
2\bar{x} & 2
\end{pmatrix}
$$

For the Hessian to be positive definite, we need:

1. $H_{11} = 2\gamma + \frac{2}{n}\sum_{i=1}^{n} x_i^2 > 0$. This is true since $\gamma > 0$ and all terms are non-negative.

2. $\det(H) > 0$:

$$
\begin{align*}
\det(H) &= 2\left(2\gamma + \frac{2}{n}\sum_{i=1}^{n} x_i^2\right) - 4\bar{x}^2\\
&= 4\gamma + \frac{4}{n}\sum_{i=1}^{n} x_i^2 - 4\bar{x}^2\\
&= 4\gamma + \frac{4}{n}\sum_{i=1}^{n} (x_i - \bar{x})^2\\
&> 0
\end{align*}
$$

since $\gamma > 0$.

Therefore, the Hessian is positive definite, confirming that $(a^*, b^*)$ is indeed a global minimizer of $R_\gamma(a, b)$.

### Final Answer

$$
\boxed{a^* = \frac{\sum_{i=1}^{n} (x_i - \bar{x})(y_i - \bar{y})}{\sum_{i=1}^{n} (x_i - \bar{x})^2 + n\gamma}}
$$

$$
\boxed{b^* = \bar{y} - a^*\bar{x}}
$$

where $\bar{x} = \frac{1}{n}\sum_{i=1}^{n} x_i$ and $\bar{y} = \frac{1}{n}\sum_{i=1}^{n} y_i$.

# END SOLN

# END PROB
