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
# END SOLN

# END SUBPROB

# BEGIN SUBPROB

Using the same model as (b), suppose we minimize MSE and find optimal parameters $\vec{\theta}^\ast$. Further suppose we apply a shifting and scaling operation to the training targets, defining

$$
\widetilde{y_i} = \alpha(y_i - \beta),\qquad\alpha,\beta\in\mathbb{R}.
$$

Find formulas for the new optimal parameters, denoted $\vec{\widetilde{\theta}}^\ast$, in terms of the old parameters and $\alpha, \beta$.

# BEGIN SOLN
# END SOLN

# END SUBPROB

# END PROB
