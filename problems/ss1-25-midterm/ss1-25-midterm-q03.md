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
## Solution

To find the minimizer $$c_1^*$$, we need to find the critical points by taking the derivative of $$R_1(c)$$ with respect to $$c$$ and setting it equal to zero.

**Step 1: Compute the derivative**

$$\frac{dR_1}{dc} = \frac{d}{dc}\left[\frac{1}{n}\sum_{i=1}^n \alpha_i(c - x_i)^2\right]$$

$$= \frac{1}{n}\sum_{i=1}^n \alpha_i \cdot 2(c - x_i)$$

$$= \frac{2}{n}\sum_{i=1}^n \alpha_i(c - x_i)$$

**Step 2: Set the derivative equal to zero**

$$\frac{2}{n}\sum_{i=1}^n \alpha_i(c - x_i) = 0$$

$$\sum_{i=1}^n \alpha_i(c - x_i) = 0$$

$$\sum_{i=1}^n \alpha_i c - \sum_{i=1}^n \alpha_i x_i = 0$$

$$c\sum_{i=1}^n \alpha_i = \sum_{i=1}^n \alpha_i x_i$$

**Step 3: Solve for $$c$$**

$$c_1^* = \frac{\sum_{i=1}^n \alpha_i x_i}{\sum_{i=1}^n \alpha_i}$$

**Step 4: Verify this is a minimum using the second derivative test**

$$\frac{d^2R_1}{dc^2} = \frac{d}{dc}\left[\frac{2}{n}\sum_{i=1}^n \alpha_i(c - x_i)\right]$$

$$= \frac{2}{n}\sum_{i=1}^n \alpha_i$$

Since $$\alpha_i > 0$$ for all $$i$$, we have $$\frac{d^2R_1}{dc^2} > 0$$, which confirms that $$c_1^*$$ is indeed a minimizer (the function is convex).

**Final Answer:**

$$c_1^* = \frac{\sum_{i=1}^n \alpha_i x_i}{\sum_{i=1}^n \alpha_i}$$

This is the weighted mean of the data points, where each point $$x_i$$ is weighted by $$\alpha_i$$.

# END SOLN

# END SUBPROB

# BEGIN SUBPROB

Find a formula for the minimizer $c_2^\ast$ of the risk function

$$
R_{2}(c) = \frac{1}{n} \sum_{i=1}^n \alpha_i |c - x_i|.
$$

# BEGIN SOLN
## Solution

To find the minimizer $$c_2^*$$, we need to analyze the risk function $$R_2(c) = \frac{1}{n}\sum_{i=1}^n \alpha_i|c - x_i|$$.

**Key observation:** The absolute value function $$|c - x_i|$$ is convex but not differentiable at $$c = x_i$$. The sum of weighted absolute values is minimized at the **weighted median** of the data points.

**Finding the derivative (where it exists):**

For $$c \neq x_i$$ for all $$i$$, we can write:

$$\frac{dR_2}{dc} = \frac{1}{n}\sum_{i=1}^n \alpha_i \cdot \frac{d}{dc}|c - x_i|$$

The derivative of $$|c - x_i|$$ is:

$$\frac{d}{dc}|c - x_i| = \begin{cases} +1 & \text{if } c > x_i \\ -1 & \text{if } c < x_i \end{cases}$$

Therefore:

$$\frac{dR_2}{dc} = \frac{1}{n}\left(\sum_{i: x_i < c} \alpha_i - \sum_{i: x_i > c} \alpha_i\right)$$

**Setting the derivative to zero:**

For a minimum, we want:

$$\sum_{i: x_i < c} \alpha_i = \sum_{i: x_i > c} \alpha_i$$

This means the sum of weights for points below $$c$$ equals the sum of weights for points above $$c$$.

**Weighted Median Formula:**

Without loss of generality, assume the data points are sorted: $$x_1 \leq x_2 \leq \cdots \leq x_n$$.

The minimizer $$c_2^*$$ is the weighted median, defined as the value $$x_k$$ such that:

$$\sum_{i=1}^{k-1} \alpha_i \leq \frac{1}{2}\sum_{i=1}^n \alpha_i \quad \text{and} \quad \sum_{i=k+1}^n \alpha_i \leq \frac{1}{2}\sum_{i=1}^n \alpha_i$$

Equivalently, $$c_2^*$$ is the smallest value $$x_k$$ in the sorted dataset for which:

$$\sum_{i: x_i \leq x_k} \alpha_i \geq \frac{1}{2}\sum_{i=1}^n \alpha_i$$

**Final Answer:**

$$c_2^* = \text{weighted median of } \{x_1, \ldots, x_n\} \text{ with weights } \{\alpha_1, \ldots, \alpha_n\}$$

More precisely, after sorting the data points, $$c_2^* = x_k$$ where $$k$$ is the smallest index satisfying:

$$\sum_{i=1}^k \alpha_i \geq \frac{1}{2}\sum_{j=1}^n \alpha_j$$

# END SOLN

# END SUBPROB

# BEGIN SUBPROB

Which risk function is more sensitive to outliers?

# BEGIN SOLN
## Solution

**$R_1$ is more sensitive to outliers.**

**Explanation:**

The risk function $R_1$ uses squared error $(c - x_i)^2$, while $R_2$ uses absolute error $|c - x_i|$.

When an outlier $x_i$ is far from the model prediction $c$:
- In $R_1$, the contribution is proportional to $(c - x_i)^2$, which grows **quadratically** with the distance
- In $R_2$, the contribution is proportional to $|c - x_i|$, which grows **linearly** with the distance

For example, if an outlier is at distance $d$ from $c$:
- $R_1$ contributes $\alpha_i d^2$
- $R_2$ contributes $\alpha_i d$

Since $d^2 > d$ for $d > 1$, large deviations (outliers) have a disproportionately larger effect on $R_1$ than on $R_2$. This quadratic penalty makes $R_1$ (mean squared error) much more sensitive to outliers compared to $R_2$ (mean absolute error).

Therefore, **$R_1$ is more sensitive to outliers** due to the squaring of errors.

# END SOLN

# END SUBPROB

# END PROB
