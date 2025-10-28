# BEGIN PROB
<i>Source: [Summer Session 1 2025 Midterm](../ss1-25-midterm/index.html), Problem 2a-e</i>

Consider a dataset $\{(\vec{x}_i, y_i)\}_{i=1}^{n}$ where each $\vec{x}_i \in \mathbb{R}^{d}$ and $y_i \in \mathbb{R}$ for which you decide to fit a multiple linear regression model:

$$
f_1(\vec{w}, b;\, \vec{x}) = \vec{w}^\top x + b,\qquad\vec{w}\in\mathbb{R}^d,\;b\in\mathbb{R}.
$$

After minimizing the MSE, the resulting model has an optimal empirical risk value denoted $R_1$.

Due to fairness constraints related to the nature of the input features, your boss informs you that the last two weights must be the same: $\vec{w}^{(d-1)} =\vec{w}^{(d)}$. Your colleague suggests a simple fix by removing the last two weights and features:

$$
f_2(\vec{w}, b;\, \vec{x}) = \vec{w}^{(1)}\vec{x}^{(1)} +  \vec{w}^{(2)}\vec{x}^{(2)} + \dotsc + \vec{w}^{(d-2)}\vec{x}^{(d-2)} + b.
$$

After training, the resulting model has an optimal empirical risk value denoted $R_2$. On the other hand, you propose the approach of grouping the last two features and using the model formula

$$
f_3(\vec{w}, b;\, \vec{x}) = \vec{w}^{(1)}\vec{x}^{(1)} +  \vec{w}^{(2)}\vec{x}^{(2)} + \dotsc +  \vec{w}^{(d-1)}\left(\vec{x}^{(d-1)} + \vec{x}^{(d)}\right) + b.
$$

After training, the final model has an optimal empirical risk value denoted $R_3$.

# BEGIN SUBPROB

Carefully apply Theorem 2.3.2 ("Optimal Model Parameters for Multiple Linear Regression") to find an expression for the optimal parameters $b^\ast, \vec{w}^\ast$ which minimize the mean squared error for the model $f_2$ and the training data $\{(\vec{x}_i, y_i)\}_{i=1}^{n}$. Your answer may contain the design matrix $\mathbf{Z}$, or any suitably modified version, as needed.

# BEGIN SOLN
# END SOLN

# END SUBPROB

# BEGIN SUBPROB

Using the comparison operators $\{ =, \leq, \geq, <, >\}$, rank the optimal risk values $R_1, R_2, R_3$ from least to greatest. Justify your answer.

# BEGIN SOLN
# END SOLN

# END SUBPROB

Returning to the original model $f_1$, suppose you were asked instead to eliminate the intercept term, leading to the model formula

$$
f_4(\vec{w};\, \vec{x}) = \vec{w}^\top x.
$$

Once again, you train this model by minimizing the associated mean squared error and obtain an optimal MSE denoted $R_4$.

# BEGIN SUBPROB

Explain why $R_1 \leq R_4$.

# BEGIN SOLN
# END SOLN

# END SUBPROB

# BEGIN SUBPROB

Assume the following centering conditions hold:

$$
\sum_{i=1}^{n} \vec{x}_i^{(j)} = 0\text{ for each }1\leq j\leq d,\text{ and }\sum_{i=1}^n y_i = 0.
$$

Prove $R_1 = R_4$.

# BEGIN SOLN
# END SOLN

# END SUBPROB

# BEGIN SUBPROB

Use the setting of $d=1$ (a.k.a. simple linear regression) to draw a sketch which illustrates why the result in Part (d) makes sense geometrically.

# BEGIN SOLN
# END SOLN

# END SUBPROB

# END PROB
