# BEGIN PROB

**\[Eligible for midterm redemption\]**

Consider a dataset of 4 values, $y_1 < y_2 < y_3 < y_4$, with a mean of
6.\
Let $Y_\text{abs}(h) = \frac{1}{4} \sum_{i = 1}^4 |y_i - h|$ represent
the mean absolute error of a constant prediction $h$ on this dataset of
4 values.

Similarly, consider another dataset of 3 values, $x_1 < x_2 < x_3$, that
also has a mean of 6.\
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

Without an absolute value sign, the empirical risk is minimized when $$h$$ is as small as possible, so $h^* = -\infty$.

TODO

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

$$y_3$$, the median of the dataset.

TODO

# END SOLUTION

# END SUBPROB

Suppose the slope of $T_\text{abs}(h)$ is $-\frac{1}{7}$ at some $h_p$.
*Hint: think about what values of $h$ could have this slope.*

# BEGIN SUBPROB

Suppose the dataset is now modified by moving the $\{x_i\}$ such that\
$y_1 < y_2 < y_3 < y_4 < x_1 < x_2 < x_3$. What would the slope of
$T_\text{abs}(h)$ be **at the point whose $x$-value is $h_p$**, given
this assumption?

# BEGIN SOLUTION

$$-\frac{3}{7}$$
Explanation: slope of $$T_{abs}(h)$$ (number of points to the left of h - number of points to the right of h) / 7. If the slope of $$T_{abs}(h)$$ was originally $$-\frac17$$, there must have been four points to the right of h and 3 points to the left of h, meaning $$y_2<h<y_3$$. It follows that in the modified dataset there are 5 points to the right of h and 2 points to the left of h, meaning the slope of $$T_{abs}(h)$$ must be $$-\frac37$$

TODO

# END SOLUTION

# END SUBPROB

*The following information is repeated from the previous page, for your
convenience.*

Consider a dataset of 4 values, $y_1 < y_2 < y_3 < y_4$, with a mean of
6. Let $Y_\text{abs}(h) = \frac{1}{4} \sum_{i = 1}^4 |y_i - h|$
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

# BEGIN SUBPROB

Suppose the dataset is now modified by repeating each value $y_i$ such
that it now contains $x_1, y_1, y_1, y_2, y_2, y_3, y_3, y_4, y_4$, in
ascending order; the ordering of the points is the same as the beginning
of this question. What would the slope of $T_\text{abs}(h)$ be **at the
point whose $x$-value is $h_p$**, given this assumption?

# BEGIN SOLUTION

Correct case 1: assumes that $$x_3$$ and $$x_4$$ are still in the dataset and finds the answer to be $$-\frac{1}{11}$$

Correct case 2: does not assume that $$x_3$$ and $$x_4$$ are still in the dataset and finds the answer to be $$\frac{1}{9}$$

TODO

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

Correct, slope of $$T_{abs}(h)$$ < slope of $$Y_{abs}(h)$$ < slope of $$X_{abs}(h)$$

TODO

# END SOLUTION

# END SUBPROB

# END PROB