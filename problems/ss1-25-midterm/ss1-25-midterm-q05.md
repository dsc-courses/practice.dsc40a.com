# BEGIN PROB
<i>Source: [Summer Session 1 2025 Midterm](../ss1-25-midterm/index.html), Problem 5a-c</i>

Let $\{(x_i,y_i)\}_{i=1}^n$ be a dataset of scalar input-output pairs.

# BEGIN SUBPROB

Suppose we model $y$ using a simple linear regression model of the form

$$
f(\vec{\theta};\, x) = \vec{\theta}^{(0)} + \vec{\theta}^{(1)}x, \qquad\vec{\theta}\in\mathbb{R}^2.
$$

Prove that the line of best fit (with respect to MSE) passes through the point $(\overline{x}, \overline{y})$.

# BEGIN SOLN
## Solution

We need to show that the optimal parameters $\vec{\theta}^*$ that minimize MSE satisfy $f(\vec{\theta}^*; \overline{x}) = \overline{y}$, where $\overline{x} = \frac{1}{n}\sum_{i=1}^n x_i$ and $\overline{y} = \frac{1}{n}\sum_{i=1}^n y_i$.

**Step 1: Set up the MSE**

The mean squared error for the model $f(\vec{\theta}; x) = \theta^{(0)} + \theta^{(1)}x$ is:

$$\text{MSE}(\vec{\theta}; (x_i, y_i)) = \frac{1}{n}\sum_{i=1}^n (y_i - (\theta^{(0)} + \theta^{(1)}x_i))^2$$

**Step 2: Find the critical points**

To minimize MSE, we take partial derivatives with respect to both parameters and set them equal to zero.

Taking the partial derivative with respect to $\theta^{(0)}$:

$$\frac{\partial \text{MSE}}{\partial \theta^{(0)}} = -\frac{2}{n}\sum_{i=1}^n (y_i - \theta^{(0)} - \theta^{(1)}x_i)$$

Setting this equal to zero:

$$-\frac{2}{n}\sum_{i=1}^n (y_i - \theta^{(0)} - \theta^{(1)}x_i) = 0$$

$$\sum_{i=1}^n y_i - n\theta^{(0)} - \theta^{(1)}\sum_{i=1}^n x_i = 0$$

Taking the partial derivative with respect to $\theta^{(1)}$:

$$\frac{\partial \text{MSE}}{\partial \theta^{(1)}} = -\frac{2}{n}\sum_{i=1}^n (y_i - \theta^{(0)} - \theta^{(1)}x_i)x_i$$

**Step 3: Solve for the optimal parameters**

From the first normal equation:

$$\sum_{i=1}^n y_i = n\theta^{(0)} + \theta^{(1)}\sum_{i=1}^n x_i$$

Dividing both sides by $n$:

$$\frac{1}{n}\sum_{i=1}^n y_i = \theta^{(0)} + \theta^{(1)} \cdot \frac{1}{n}\sum_{i=1}^n x_i$$

This simplifies to:

$$\overline{y} = \theta^{(0)} + \theta^{(1)}\overline{x}$$

**Step 4: Conclusion**

The equation $\overline{y} = \theta^{(0)} + \theta^{(1)}\overline{x}$ is exactly the statement that $f(\vec{\theta}^*; \overline{x}) = \overline{y}$, which means the line of best fit passes through the point $(\overline{x}, \overline{y})$.

Therefore, we have proven that the line of best fit with respect to MSE passes through the point $(\overline{x}, \overline{y})$.

# END SOLN

# END SUBPROB

# BEGIN SUBPROB

Suppose we model $y$ using a simple polynomial regression model of the form

$$
f(\vec{\theta};\, x) = \vec{\theta}^{(0)} + \vec{\theta}^{(1)}x+ \vec{\theta}^{(2)}x^2, \qquad\vec{\theta}\in\mathbb{R}^3.
$$

Prove that the curve of best fit (with respect to MSE) passes through the point $(\overline{x}, \overline{y} + \vec\theta^{\ast(2)}((\overline{x})^2 - \overline{x^2}))$, where

$$
\overline{x^2} = \frac{1}{n}\sum_{i=1}^n x_i^2.
$$

# BEGIN SOLN
## Solution

We need to show that the optimal curve passes through the point $(\bar{x}, \bar{y} + \tilde{\theta}^{*(2)}((\overline{x^2}) - \overline{x}^2))$.

The MSE for the polynomial regression model is:

$\text{MSE}(\vec{\theta}) = \frac{1}{n}\sum_{i=1}^n (y_i - \tilde{\theta}^{(0)} - \tilde{\theta}^{(1)}x_i - \tilde{\theta}^{(2)}x_i^2)^2$

To find the optimal parameters, we take partial derivatives and set them equal to zero.

**Setting $\frac{\partial \text{MSE}}{\partial \tilde{\theta}^{(0)}} = 0$:**

$\frac{\partial \text{MSE}}{\partial \tilde{\theta}^{(0)}} = -\frac{2}{n}\sum_{i=1}^n (y_i - \tilde{\theta}^{(0)} - \tilde{\theta}^{(1)}x_i - \tilde{\theta}^{(2)}x_i^2) = 0$

This gives us:

$\sum_{i=1}^n (y_i - \tilde{\theta}^{(0)} - \tilde{\theta}^{(1)}x_i - \tilde{\theta}^{(2)}x_i^2) = 0$

Expanding:

$\sum_{i=1}^n y_i - n\tilde{\theta}^{*(0)} - \tilde{\theta}^{*(1)}\sum_{i=1}^n x_i - \tilde{\theta}^{*(2)}\sum_{i=1}^n x_i^2 = 0$

Dividing by $n$:

$\bar{y} - \tilde{\theta}^{*(0)} - \tilde{\theta}^{*(1)}\bar{x} - \tilde{\theta}^{*(2)}\overline{x^2} = 0$

Therefore:

$\tilde{\theta}^{*(0)} = \bar{y} - \tilde{\theta}^{*(1)}\bar{x} - \tilde{\theta}^{*(2)}\overline{x^2}$

**Now we evaluate the optimal curve at $x = \bar{x}$:**

$f(\vec{\theta}^*; \bar{x}) = \tilde{\theta}^{*(0)} + \tilde{\theta}^{*(1)}\bar{x} + \tilde{\theta}^{*(2)}\bar{x}^2$

Substituting the expression for $\tilde{\theta}^{*(0)}$:

$f(\vec{\theta}^*; \bar{x}) = (\bar{y} - \tilde{\theta}^{*(1)}\bar{x} - \tilde{\theta}^{*(2)}\overline{x^2}) + \tilde{\theta}^{*(1)}\bar{x} + \tilde{\theta}^{*(2)}\bar{x}^2$

Simplifying:

$f(\vec{\theta}^*; \bar{x}) = \bar{y} - \tilde{\theta}^{*(2)}\overline{x^2} + \tilde{\theta}^{*(2)}\bar{x}^2$

$f(\vec{\theta}^*; \bar{x}) = \bar{y} + \tilde{\theta}^{*(2)}(\bar{x}^2 - \overline{x^2})$

$f(\vec{\theta}^*; \bar{x}) = \bar{y} + \tilde{\theta}^{*(2)}((\overline{x})^2 - \overline{x^2})$

Since $(\overline{x})^2 = \overline{x}^2$, we can rewrite this as:

$f(\vec{\theta}^*; \bar{x}) = \bar{y} + \tilde{\theta}^{*(2)}(\overline{x^2} - \overline{x}^2)$

Note: We use the fact that $\bar{x}^2 - \overline{x^2} = -(\overline{x^2} - \bar{x}^2)$.

Therefore, the curve of best fit passes through the point $(\bar{x}, \bar{y} + \tilde{\theta}^{*(2)}((\overline{x^2}) - \overline{x}^2))$.
# END SOLN

# END SUBPROB

# BEGIN SUBPROB

Using the same model as (b), suppose we minimize MSE and find optimal parameters $\vec{\theta}^\ast$. Further suppose we apply a shifting and scaling operation to the training targets, defining

$$
\widetilde{y_i} = \alpha(y_i - \beta),\qquad\alpha,\beta\in\mathbb{R}.
$$

Find formulas for the new optimal parameters, denoted $\vec{\widetilde{\theta}}^\ast$, in terms of the old parameters and $\alpha, \beta$.

# BEGIN SOLN
## Solution

We start by setting up the problem. For the polynomial regression model $$f(\vec{\theta}; x) = \theta^{(0)} + \theta^{(1)}x + \theta^{(2)}x^2$$, the design matrix is:

$$\mathbf{Z} = \begin{bmatrix} 1 & x_1 & x_1^2 \\ 1 & x_2 & x_2^2 \\ \vdots & \vdots & \vdots \\ 1 & x_n & x_n^2 \end{bmatrix} \in \mathbb{R}^{n \times 3}$$

and the target vector is:

$$\mathbf{Y} = \begin{bmatrix} y_1 \\ y_2 \\ \vdots \\ y_n \end{bmatrix} \in \mathbb{R}^n$$

**Original optimal parameters:**

Assuming $$(\mathbf{Z}^T\mathbf{Z})^{-1}$$ exists, the optimal parameters for the original problem are:

$$\vec{\theta}^* = (\mathbf{Z}^T\mathbf{Z})^{-1}\mathbf{Z}^T\mathbf{Y}$$

**Transformed target vector:**

When we apply the transformation $$\tilde{y}_i = \alpha(y_i - \beta)$$, the new target vector becomes:

$$\tilde{\mathbf{Y}} = \begin{bmatrix} \tilde{y}_1 \\ \tilde{y}_2 \\ \vdots \\ \tilde{y}_n \end{bmatrix} = \alpha(\mathbf{Y} - \beta\mathbf{1})$$

where $$\mathbf{1} = \begin{bmatrix} 1 \\ 1 \\ \vdots \\ 1 \end{bmatrix} \in \mathbb{R}^n$$.

**New optimal parameters:**

The optimal parameters for the transformed problem are:

$$\tilde{\vec{\theta}}^* = (\mathbf{Z}^T\mathbf{Z})^{-1}\mathbf{Z}^T\tilde{\mathbf{Y}}$$

$$= (\mathbf{Z}^T\mathbf{Z})^{-1}\mathbf{Z}^T[\alpha(\mathbf{Y} - \beta\mathbf{1})]$$

$$= \alpha(\mathbf{Z}^T\mathbf{Z})^{-1}\mathbf{Z}^T\mathbf{Y} - \alpha\beta(\mathbf{Z}^T\mathbf{Z})^{-1}\mathbf{Z}^T\mathbf{1}$$

$$= \alpha\vec{\theta}^* - \alpha\beta(\mathbf{Z}^T\mathbf{Z})^{-1}\mathbf{Z}^T\mathbf{1}$$

**Computing** $$\mathbf{Z}^T\mathbf{1}$$:

$$\mathbf{Z}^T\mathbf{1} = \begin{bmatrix} 1 & 1 & \cdots & 1 \\ x_1 & x_2 & \cdots & x_n \\ x_1^2 & x_2^2 & \cdots & x_n^2 \end{bmatrix} \begin{bmatrix} 1 \\ 1 \\ \vdots \\ 1 \end{bmatrix} = \begin{bmatrix} n \\ \sum_{i=1}^n x_i \\ \sum_{i=1}^n x_i^2 \end{bmatrix}$$

**Final formula:**

Therefore, the new optimal parameters are:

$$\boxed{\tilde{\vec{\theta}}^* = \alpha\vec{\theta}^* - \alpha\beta(\mathbf{Z}^T\mathbf{Z})^{-1}\begin{bmatrix} n \\ \sum_{i=1}^n x_i \\ \sum_{i=1}^n x_i^2 \end{bmatrix}}$$

Alternatively, this can be written more compactly as:

$$\boxed{\tilde{\vec{\theta}}^* = \alpha\vec{\theta}^* - \alpha\beta(\mathbf{Z}^T\mathbf{Z})^{-1}\mathbf{Z}^T\mathbf{1}}$$

**Interpretation:** The transformation $$\tilde{y}_i = \alpha(y_i - \beta)$$ scales the targets by $$\alpha$$ and shifts them by $$-\alpha\beta$$. The optimal parameters scale by $$\alpha$$ (first term) and receive an additional correction term (second term) that depends on both the shift $$\beta$$ and the structure of the design matrix through $$(\mathbf{Z}^T\mathbf{Z})^{-1}\mathbf{Z}^T\mathbf{1}$$.

# END SOLN

# END SUBPROB

# END PROB
