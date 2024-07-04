# BEGIN PROB

**\[Eligible for midterm redemption\]**\]

Suppose we're given a dataset of $n$ points,
$(x_1, y_1), (x_2, y_2), ..., (x_n, y_n)$, where $\bar{x}$ is the mean
of $x_1, x_2, ..., x_n$ and $\bar{y}$ is the mean of
$y_1, y_2, ..., y_n$.

Using this dataset, we create a *transformed* dataset of $n$ points,
$(x_1', y_1'), (x_2', y_2'), ..., (x_n', y_n')$, where:

$$x_i' = 4x_i - 3 \qquad y_i' = y_i + 24$$

That is, the transformed dataset is of the form
$(4x_1 - 3, y_1 + 24), ..., (4x_n - 3, y_n + 24)$.

We decide to fit a simple linear hypothesis function
$H(x') = w_0 + w_1x'$ on the transformed dataset using squared loss. We
find that $w_0^* = 7$ and $w_1^* = 2$, so $H^*(x') = 7 + 2x'$.

# BEGIN SUBPROB

Suppose we were to fit a simple linear hypothesis function through the
original dataset, $(x_1, y_1), (x_2, y_2), ..., (x_n, y_n)$, again using
squared loss. What would the optimal slope be?

( ) 2 ( ) 4 ( ) 6 ( ) 8 ( ) 11 ( ) 12 ( ) 24

# BEGIN SOLUTION

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

Recall, the hypothesis function $H^*$ was fit on the transformed
dataset,

$(x_1', y_1'), (x_2', y_2'), ..., (x_n', y_n')$. $H^*$ happens to pass
through the point $(\bar{x}, \bar{y})$. What is the value of $\bar{x}$?
Give your answer as an integer with no variables.

$\bar{x} =$

# BEGIN SOLUTION

# END SOLUTION

# END SUBPROB

# END PROB