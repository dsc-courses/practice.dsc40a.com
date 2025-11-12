# BEGIN PROB

For each statement below, fill in the circle indicating the word(s) or phrase(s) which would make the statement correct if added to the sentence. In several statements, $(y_i)_{i=1}^n$ denotes a dataset of real numbers. *You do not need to show your work for full credit, but partial credit may be awarded for supporting calculations and reasoning.*

# BEGIN SUBPROB

If $x^\ast$ is a maximizer for $f(x)$ and $f(x)\geq 0$ for all $x$, then $x^\ast$ is a ________ for $g(x)=3-f(x)^2$.

$\bigcirc$ minimizer   $\bigcirc$ maximizer   $\bigcirc$ neither

# BEGIN SOLUTION

The correct answer is **minimizer**. Note that $g(x) = 3-f(x)^2$ is a monotone decreasing function for $x\geq 0$. Therefore, since $f(x) \leq f(x^\ast)$ for all $x$, $g(f(x)) \geq g(f(x^\ast))$ for all $x$ and this $x^\ast$ is a minimizer for $3-f^2$.

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

Suppose we wish to find a constant predictor for $y$ using either squared or absolute loss. In high-stakes scenarios where outliers are rare but of great importance, it is better to use the ________ function.

$\bigcirc$ absolute loss   $\bigcirc$ squared loss

# BEGIN SOLUTION

The answer is **squared** loss, since it is more sensitive to outliers.

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

Let $(1, 3, 4, 1, 2, -1)$ be a dataset of real numbers. The derivative of the empirical risk for the absolute loss $L_{abs}(h)$ of a constant predictor $h$ for the dataset is ________ when $h=2.5$.

$\bigcirc$ positive   $\bigcirc$ negative   $\bigcirc$ zero

# BEGIN SOLUTION

The derivative of empirical risk for absolute loss is given by
$$R'(h) = \frac{1}{n}\sum_{i=1}^n\mathrm{sign}(h - y_i).$$ 

See lectures 3-4 for a derivation. Thus
$$R'(2.5) = \frac{1}{6}(1 -1 -1 +1 +1 +1) = \frac{1}{3} > 0 .$$

So the correct answer is **positive**.

Alternative solution: Order the dataset: $(-1,1, 1, 2, 3, 4 )$. The loss is minimized in the range [1,2]. The point $h=2.5$ is to the right of this minimum and therefore the function is increasing at this point and the derivative must be positive.

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

Assume a dataset $\{y_i\}_{i=1}^n$ satisfies $y_i\in[0,1]$ for all $i$. Let $h^\ast$ denote the optimal constant predictor for the dataset with respect to squared loss. Assume we sample a new data point $y_{n+1}$ where $y_{n+1}=y_4 - 2$. Then the new minimizer $h'$ is ________ the old minimizer $h^\ast$.

$\bigcirc$ greater than   $\bigcirc$ less than   $\bigcirc$ equal to

# BEGIN SOLUTION

We have that $h^\ast$ is the mean of the original data, and $h'$ is the mean of the new data. Therefore 
$$\begin{aligned}
h' & = \frac{1}{n+1}\sum_{i=1}^{n+1}y_i = \frac{1}{n+1}(y_1+\cdots+y_n + (y_4 - 2)) \\
& = \frac{1}{n+1}(n h^\ast + (y_4 - 2)) \\
& = \frac{n}{n+1}h^\ast + \frac{y_4 - 2}{n+1}
\end{aligned}$$

Note that $y_4 - 2 \leq 1 - 2 = -1 < 0$, so that
$$\begin{aligned}
\frac{n}{n+1}h^\ast + \frac{y_4 - 2}{n+1} < \frac{n}{n+1}h^\ast < h^\ast
\end{aligned}$$

Therefore the correct answer is **less than**.

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

Let $\epsilon > 0$ be any positive real number. Define the smooth loss by the formula
$$L_{\epsilon}(h, y_i) = \sqrt{|y_i - h|^2+ \epsilon^2}.$$

Then the optimal *value* of the empirical risk of $L_{\epsilon}$ is ________ the optimal *value* of the empirical risk of the absolute loss function.

$\bigcirc$ greater than   $\bigcirc$ less than   $\bigcirc$ equal to

# BEGIN SOLUTION

Note that
$$L_{\epsilon}(h, y_i) = \sqrt{|y_i - h|^2+ \epsilon^2} >\sqrt{|y_i - h|^2} = |y_i-h| = L_{abs}(h, y_i).$$

Therefore the minimum value of $L_{\epsilon}$ is **greater** than the minimum value of $L_{abs}$.

# END SOLUTION

# END SUBPROB

# END PROB