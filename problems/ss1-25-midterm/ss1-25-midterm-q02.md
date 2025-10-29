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

**Solution**

We begin by rewriting the model $f_2$ more explicitly. The model $f_2$ has $d-2$ weight parameters (excluding the intercept $b$):
$$
f_2(\vec{w}, b; \vec{x}) = \sum_{j=1}^{d-2} \vec{w}^{(j)} x^{(j)} + b, \quad \vec{w} \in \mathbb{R}^{d-2}, \, b \in \mathbb{R}.
$$

To apply Theorem 2.3.2, we need to construct the appropriate design matrix and parameter vector.

**Step 1: Define the modified design matrix**

Let $\mathbf{Z}_2 \in \mathbb{R}^{n \times (d-1)}$ be the modified design matrix where each row corresponds to a training example with only the first $d-2$ features plus a column of ones for the intercept:
$$
\mathbf{Z}_2 = \begin{bmatrix}
1 & x_1^{(1)} & x_1^{(2)} & \cdots & x_1^{(d-2)} \\
1 & x_2^{(1)} & x_2^{(2)} & \cdots & x_2^{(d-2)} \\
\vdots & \vdots & \vdots & \ddots & \vdots \\
1 & x_n^{(1)} & x_n^{(2)} & \cdots & x_n^{(d-2)}
\end{bmatrix} \in \mathbb{R}^{n \times (d-1)}.
$$

**Step 2: Define the parameter vector and target vector**

Let $\vec{\theta} \in \mathbb{R}^{d-1}$ be the combined parameter vector:
$$
\vec{\theta} = \begin{bmatrix} b \\ \vec{w}^{(1)} \\ \vec{w}^{(2)} \\ \vdots \\ \vec{w}^{(d-2)} \end{bmatrix}.
$$

Let $\mathbf{Y} \in \mathbb{R}^n$ be the target vector:
$$
\mathbf{Y} = \begin{bmatrix} y_1 \\ y_2 \\ \vdots \\ y_n \end{bmatrix}.
$$

**Step 3: Express the MSE**

The mean squared error can be written as:
$$
\text{MSE}(\vec{\theta}) = \frac{1}{n} \sum_{i=1}^n \left( y_i - \mathbf{Z}_{2,i}^{\top} \vec{\theta} \right)^2 = \frac{1}{n} \|\mathbf{Y} - \mathbf{Z}_2 \vec{\theta}\|_2^2.
$$

**Step 4: Apply Theorem 2.3.2**

To minimize the MSE, we take the gradient with respect to $\vec{\theta}$ and set it equal to zero:
$$
\frac{\partial \text{MSE}}{\partial \vec{\theta}} = -\frac{2}{n} \mathbf{Z}_2^{\top} (\mathbf{Y} - \mathbf{Z}_2 \vec{\theta}) = 0.
$$

This simplifies to the normal equation:
$$
\mathbf{Z}_2^{\top} \mathbf{Z}_2 \vec{\theta} = \mathbf{Z}_2^{\top} \mathbf{Y}.
$$

Assuming $\mathbf{Z}_2^{\top} \mathbf{Z}_2$ is invertible (which holds when $\mathbf{Z}_2$ has full column rank), the unique minimizer is:
$$
\vec{\theta}^* = \left( \mathbf{Z}_2^{\top} \mathbf{Z}_2 \right)^{-1} \mathbf{Z}_2^{\top} \mathbf{Y}.
$$

**Step 5: Extract optimal parameters**

The optimal parameters are obtained by decomposing $\vec{\theta}^*$:
$$
\begin{bmatrix} b^* \\ \vec{w}^* \end{bmatrix} = \vec{\theta}^* = \left( \mathbf{Z}_2^{\top} \mathbf{Z}_2 \right)^{-1} \mathbf{Z}_2^{\top} \mathbf{Y},
$$
where $b^*$ is the first component and $\vec{w}^* \in \mathbb{R}^{d-2}$ consists of the remaining components.

**Final Answer:**
$$
\boxed{\begin{bmatrix} b^* \\ \vec{w}^* \end{bmatrix} = \left( \mathbf{Z}_2^{\top} \mathbf{Z}_2 \right)^{-1} \mathbf{Z}_2^{\top} \mathbf{Y}}
$$
where $\mathbf{Z}_2 \in \mathbb{R}^{n \times (d-1)}$ is the design matrix containing a column of ones followed by the first $d-2$ features of each training example.

# END SOLN

# END SUBPROB

# BEGIN SUBPROB

Using the comparison operators $\{ =, \leq, \geq, <, >\}$, rank the optimal risk values $R_1, R_2, R_3$ from least to greatest. Justify your answer.

# BEGIN SOLN
## Solution

**Answer:** $R_1 \leq R_3 \leq R_2$

**Justification:**

To compare these three models, we need to analyze their flexibility and representational capacity.

**Comparing $R_1$ and $R_3$:**

Model $f_1$ is the most general model with $d$ independent weight parameters plus an intercept, giving it $(d+1)$ total parameters.

Model $f_3$ can be rewritten as:
$$f_3(\vec{w}, b; \vec{x}) = \vec{w}^{(1)}x^{(1)} + \ldots + \vec{w}^{(d-2)}x^{(d-2)} + \vec{w}^{(d-1)}x^{(d-1)} + \vec{w}^{(d-1)}x^{(d)} + b$$

This is equivalent to $f_1$ with the constraint that $w^{(d-1)} = w^{(d)}$. In other words, $f_3$ is a constrained version of $f_1$.

Since $f_1$ includes all possible models that $f_3$ can represent (by setting $w^{(d-1)} = w^{(d)}$ in $f_1$), the minimum achievable MSE for $f_1$ must be at least as good as (or better than) that of $f_3$. Therefore:

$$R_1 \leq R_3$$

**Comparing $R_3$ and $R_2$:**

Model $f_2$ completely removes the last two features from the model, using only features $x^{(1)}, \ldots, x^{(d-2)}$.

Model $f_3$ uses all $d$ features but groups the last two with a shared coefficient $\vec{w}^{(d-1)}$.

We can show that $f_3$ is more flexible than $f_2$ by noting that $f_2$ is a special case of $f_3$. Specifically, if we set $\vec{w}^{(d-1)} = 0$ in model $f_3$, we get:

$$f_3(\vec{w}, b; \vec{x}) = \vec{w}^{(1)}x^{(1)} + \ldots + \vec{w}^{(d-2)}x^{(d-2)} + 0 \cdot (x^{(d-1)} + x^{(d)}) + b = f_2(\vec{w}, b; \vec{x})$$

Since $f_3$ can represent any model that $f_2$ can represent (plus additional models where $\vec{w}^{(d-1)} \neq 0$), the minimum achievable MSE for $f_3$ must be at least as good as that of $f_2$. Therefore:

$$R_3 \leq R_2$$

**Final Ranking:**

Combining these results, we have:

$$R_1 \leq R_3 \leq R_2$$

This ranking makes intuitive sense: $f_1$ is the most flexible model with the most parameters, allowing it to fit the training data best (lowest MSE). Model $f_3$ is moderately flexible, incorporating information from all features but with a constraint on the last two weights. Model $f_2$ is the least flexible, as it discards potentially useful information by completely removing the last two features.
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
