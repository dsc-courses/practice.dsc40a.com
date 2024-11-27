# BEGIN PROB

<i>Source: [Summer Session 2 2024 Final](../ss2-24-final/index.html), Problem 2a-e</i>

Consider a dataset of 4 values, $y_1 < y_2 < y_3 < y_4$, with a mean of
6.

Let $Y_\text{abs}(h) = \frac{1}{4} \sum_{i = 1}^4 |y_i - h|$ represent
the mean absolute error of a constant prediction $h$ on this dataset of
4 values.

Similarly, consider another dataset of 3 values, $x_1 < x_2 < x_3$, that
also has a mean of 6.

Let $X_\text{abs}(h) = \frac{1}{3} \sum_{i = 1}^3 |x_i - h|$ represent
the mean absolute error of a constant prediction $h$ on this dataset of
3 values.

Suppose that $x_1 < y_1$, $y_4 < x_2$, and that $T_\text{abs}(h)$
represents the mean **absolute** error of a constant prediction $h$ on
the combined dataset of 7 values, $x_1, y_1, ..., y_4, x_2, x_3$. We
denote these 7 values as $\{ z_1, z_2, z_3, z_4, z_5, z_6, z_7 \}$.

# BEGIN SUBPROB

What value of $h$ minimizes the following empirical risk function?
$$Z(h) = \frac{1}{7} \sum_{i = 1}^7 (h - z_i)$$

( ) $-\infty$
( ) 0
( ) 6
( ) $y_3$
( ) Any value between $y_3$ and $y_4$

# BEGIN SOLUTION

$Z(h) = \frac{1}{7} \sum_{i = 1}^7 (h - z_i)$ is minimized when $h$ is as small as possible. If $h$ is smaller than $z_i$ then it will make a negative risk! This means the smaller $h$ is the smaller the difference will be!

When looking at our answers available the smallest risk would be $h^* = -\infty$.

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

What value of $h$ minimizes **mean absolute error**, $T_\text{abs}(h)$?

( ) $-\infty$
( ) 0
( ) 6
( ) $y_3$
( ) Any value between $y_3$ and $y_4$
( ) $\infty$

# BEGIN SOLUTION

$y_3$, the median of the dataset.

Recall $h^*$ for $T_\text{abs}(h)$ is the median of the dataset!

Our dataset is: $x_1, y_1, y_2, y_3, y_4, x_2, x_3$. Our median is $y_3$, which means $h^* = y_3$.

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

Suppose the slope of $T_\text{abs}(h)$ is $-\frac{1}{7}$ at some $h_p$.
*Hint: think about what values of $h$ could have this slope.*

Suppose the dataset is now modified by moving the $\{x_i\}$ such that\
$y_1 < y_2 < y_3 < y_4 < x_1 < x_2 < x_3$. What would the slope of
$T_\text{abs}(h)$ be **at the point whose $x$-value is $h_p$**, given
this assumption?

# BEGIN SOLUTION

$$-\frac{3}{7}$$

Slope of $T_{abs}(h)$ is equal to $\frac{1}{7} * \text{(number of points to the left of h - number of points to the right of h)}$. If the slope of $T_{abs}(h)$ was originally $-\frac{1}{7}$, there must have been four points to the right of h and 3 points to the left of h, meaning $y_2<h<y_3$. It follows that in the modified dataset there are 5 points to the right of h and 2 points to the left of h, meaning the slope of $T_{abs}(h)$ must be $-\frac{3}{7}$

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

*The following information is repeated from the previous page, for your
convenience.*

Consider a dataset of 4 values, $y_1 < y_2 < y_3 < y_4$, with a mean of 6. Let $Y_\text{abs}(h) = \frac{1}{4} \sum_{i = 1}^4 |y_i - h|$
represent the mean absolute error of a constant prediction $h$ on this
dataset of 4 values.

Similarly, consider another dataset of 3 values, $x_1 < x_2 < x_3$, that
also has a mean of 6. Let
$X_\text{abs}(h) = \frac{1}{3} \sum_{i = 1}^3 |x_i - h|$ represent the
mean absolute error of a constant prediction $h$ on this dataset of 3
values.

Suppose that $x_1 < y_1$, $y_4 < x_2$, and that $T_\text{abs}(h)$
represents the mean **absolute** error of a constant prediction $h$ on
the combined dataset of 7 values, $x_1, y_1, ..., y_4, x_2, x_3$. We
denote these 7 values as $\{ z_1, z_2, z_3, z_4, z_5, z_6, z_7 \}$.

Suppose the slope of $T_\text{abs}(h)$ is $-\frac{1}{7}$ at some $h_p$.
*Hint: think about what values of $h$ could have this slope.*

Suppose the dataset is now modified by repeating each value $y_i$ such
that it now contains $x_1, y_1, y_1, y_2, y_2, y_3, y_3, y_4, y_4$, in
ascending order; the ordering of the points is the same as the beginning of this question. What would the slope of $T_\text{abs}(h)$ be **at the point whose $x$-value is $h_p$**, given this assumption?

# BEGIN SOLUTION

There are two answers based on if you believed  $x_2$ and $x_3$ was still in the dataset.

Recall the slope of $T_{abs}(h)$ is equal to $\frac{1}{7} * \text{(number of points to the left of h - number of points to the right of h)}$.

**Correct case 1:** assumes that  $x_2$ and $x_3$ are still in the dataset and finds the answer to be $-\frac{1}{11}$

- In our original dataset the slope at $h_p = - \frac{1}{7}$, this reflects there were four points to the left of $h_p$ and three points to the right of $h_p$
    - This would mean $h_p$ would be in between $y_2$ and $y_3$ of the original dataset ($x_1, y_1, y_2, y_3, y_4, x_2, x_3$)
- Our new dataset would become $x_1, y_1, y_1, y_2, y_2, y_3, y_3, y_4, y_4, x_2, x_3$
- We assume $h_p$ does not change, this means that it would look like: $x_1, y_1, y_1, y_2, y_2, h_p, y_3, y_3, y_4, y_4, x_2, x_3$
- We can see there are five points to the left of $h_p$ and six points to the right of $h_p$, this means we have $\frac{1}{11} (5 - 6) = -\frac{1}{11}$

**Correct case 2:** does not assume that $x_2$ and $x_3$ are still in the dataset and finds the answer to be $\frac{1}{9}$

- In our original dataset the slope at $h_p = - \frac{1}{7}$, this reflects there were four points to the left of $h_p$ and three points to the right of $h_p$
    - This would mean $h_p$ would be in between $y_2$ and $y_3$ of the original dataset ($x_1, y_1, y_2, y_3, y_4, x_2, x_3$)
- Our new dataset would become $x_1, y_1, y_1, y_2, y_2, y_3, y_3, y_4, y_4$
- We assume $h_p$ does not change, this means that it would look like: $x_1, y_1, y_1, y_2, y_2, h_p, y_3, y_3, y_4, y_4$
- We can see there are five points to the left of $h_p$ and four points to the right of $h_p$, this means we have $\frac{1}{9} (5 - 4) = \frac{1}{9}$

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

**At the point whose $x$-value is $h_{p}$**, select the option below
that correctly describes the relationship between the **slopes** of
$Y_\text{abs}(h)$, $X_\text{abs}(h)$, and $T_\text{abs}(h)$,
respectively.

*Hint: We already know the slope of $T_\text{abs}(h)$ at $h_p$.*

( ) $\text{slope of }Y_\text{abs}(h) < \text{slope of } T_\text{abs}(h) < \text{slope of } X_\text{abs}(h)$
( ) $\text{slope of }Y_\text{abs}(h) < \text{slope of } X_\text{abs}(h) < \text{slope of } T_\text{abs}(h)$
( ) $\text{slope of }T_\text{abs}(h) < \text{slope of } X_\text{abs}(h) < \text{slope of } Y_\text{abs}(h)$
( ) $\text{slope of }T_\text{abs}(h) < \text{slope of } Y_\text{abs}(h) < \text{slope of } X_\text{abs}(h)$
( ) $\text{slope of }X_\text{abs}(h) < \text{slope of } T_\text{abs}(h) < \text{slope of } Y_\text{abs}(h)$
( ) $\text{slope of }X_\text{abs}(h) < \text{slope of } Y_\text{abs}(h) < \text{slope of } T_\text{abs}(h)$

# BEGIN SOLUTION

Slope of $T_{abs}(h)$ < slope of $Y_{abs}(h)$ < slope of $X_{abs}(h)$

There is a key insight to make here: the slope of the mean absolute error is influenced by the distribution of points above and below $h$.

$T_{abs}(h)$ represents the combined dataset (both the $x$'s and the $y$'s), so the slope reflects the overall balance between the two datasets. This means the distribution of points above and below $h$ will be smoothed out. As a result the slope will be the least steep.

$Y_{abs}(h)$ represents only the $y$'s. There are 4 $y$ values and we know these points are closer together than the $x$ values. Because the $y$ values are more concentrated the slope will be larger! (Recall that the mean for these 4 points is 6).

$X_{abs}(h)$represents only the $x$'s. There are 3 $x$ values and we know these points are farther apart than the $y$ values. Because the $x$ values are more spread out the slope will be smaller! (Recall that the mean for these 3 points is 6).

# END SOLUTION

# END SUBPROB

# END PROB