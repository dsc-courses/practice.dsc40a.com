# BEGIN PROB
<i>Source: [Summer Session 1 2025 Midterm](../ss1-25-midterm/index.html), Problem 3a-c</i>

Let $\{x_i\}_{i=1}^n$ be a training dataset of scalar values, and suppose we wish to use the constant model

$$
f(c;\, x) = c,\qquad c\in\mathbb{R}.
$$

In various situations it can be useful to emphasize some training examples over others (e.g., due to data quality). For this purpose, suppose $\alpha_1, \alpha_2, \dotsc, \alpha_n > 0$ are fixed positive weights which are understood as separate from the training data and model parameters.

# BEGIN SUBPROB

Find a formula for the minimizer $c_1^\ast$ of the risk function

$$
R_{1}(c) = \frac{1}{n} \sum_{i=1}^n \alpha_i(c - x_i)^2.
$$

# BEGIN SOLN
# END SOLN

# END SUBPROB

# BEGIN SUBPROB

Find a formula for the minimizer $c_2^\ast$ of the risk function

$$
R_{2}(c) = \frac{1}{n} \sum_{i=1}^n \alpha_i |c - x_i|.
$$

# BEGIN SOLN
# END SOLN

# END SUBPROB

# BEGIN SUBPROB

Which risk function is more sensitive to outliers?

# BEGIN SOLN
# END SOLN

# END SUBPROB

# END PROB
