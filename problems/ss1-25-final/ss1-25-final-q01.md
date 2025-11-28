# BEGIN PROB

<i>Source: DSC 40A Midterm Take-Home Exam, August 1, 2025, Exercise 1</i>

Consider the following dataset of scalar-valued training examples:

$$
\begin{array}{c|c|c|c}
x_1 & x_2 & x_3 & x_4\\\hline
1 & 2 & 2 & 4
\end{array}
$$

We model the collection of $x_i$'s using the constant model $f(c;\, x) = c$.

# BEGIN SUBPROB

(a) Recall the Huber loss function

$$
L_{\rm Huber}(c; x_i) = 
\begin{cases}
\frac{1}{2}(c - x_i)^2, & \text{if } |c - x_i| \leq \frac{1}{2}, \\
\frac{1}{2}|c - x_i| - \frac{1}{8}, & \text{if } |c - x_i| > \frac{1}{2}.
\end{cases}
$$

Prove that the empirical risk function $R_{\rm Huber}(c)$ associated with the Huber loss is convex. Is it strictly convex?

# BEGIN SOLUTION

<!-- Write solution here -->

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

(b) Implement four iterations (not including initial guess) of gradient descent with step size $\eta = 1$ and initial guess $c_0 = \frac{3}{2}$ to find approximate minimizer $c^\ast_{\rm Huber}$. Include a table of $(c_t, R_{\rm Huber}(c_t), R_{\rm Huber}'(c_t))$ for $t=0,1,\dots,4$.

# BEGIN SOLUTION

<!-- Write solution with table here -->

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

(c) Compute the minimizers $c^\ast_{\rm abs}$ and $c^\ast_{\rm sq}$ for the mean absolute error and mean squared error, respectively, and rank $c^\ast_{\rm Huber}, c^\ast_{\rm abs}, c^\ast_{\rm sq}$ from least to greatest.

# BEGIN SOLUTION

<!-- Write solution here -->

# END SOLUTION

# END SUBPROB

# END PROB
