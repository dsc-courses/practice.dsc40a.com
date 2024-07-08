# BEGIN PROB

Consider a dataset of 3 values, $y_1 < y_2 < y_3$, with a mean of 2. Let
$Y_\text{abs}(h) = \frac{1}{3} \sum_{i = 1}^3 |y_i - h|$ represent the
mean absolute error of a constant prediction $h$ on this dataset of 3
values.

Similarly, consider another dataset of 5 values,
$z_1 < z_2 < z_3 < z_4 < z_5$, with a mean of 12. Let
$Z_\text{abs}(h) = \frac{1}{5} \sum_{i = 1}^5 |z_i - h|$ represent the
mean absolute error of a constant prediction $h$ on this dataset of 5
values.

Suppose that $y_3 < z_1$, and that $T_\text{abs}(h)$ represents the mean
absolute error of a constant prediction $h$ on the combined dataset of 8
values, $y_1, ..., y_3, z_1, ..., z_5$.

# BEGIN SUBPROB

Fill in the blanks:

**"{ i } minimizes $Y_\text{abs}(h)$, { ii } minimizes $Z_\text{abs}(h)$, and
{ iii } minimizes $T_\text{abs}(h)$."**


1.  What goes in blank { i }?

( ) $y_1$
( ) any value between $y_1$ and $y_2$ (inclusive)
( ) $y_2$
( ) $y_3$
( ) $z_1$

2.  What goes in blank { ii }?

( ) $z_1$
( ) $z_2$
( ) any value between $z_2$ and $z_3$ (inclusive)
( ) any value between $z_2$ and $z_4$ (inclusive)
( ) $z_3$

3.  What goes in blank { iii }?

( ) $y_2$
( ) $y_3$
( ) any value between $y_3$ and $z_1$ (inclusive)
( ) any value between $z_1$ and $z_2$ (inclusive)
( ) any value between $z_2$ and $z_3$ (inclusive)

# BEGIN SOLUTION

TODO

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

For any $h$, it is true that:

$$T_\text{abs}(h) = \alpha Y_\text{abs}(h) + \beta Z_\text{abs}(h)$$

for some constants $\alpha$ and $\beta$. What are the values of $\alpha$
and $\beta$? Give your answers as integers or simplified fractions with
no variables.

# BEGIN SOLUTION

TODO

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

Show that $Y_\text{abs}(z_1) = z_1 - 2$.

*Hint: Use the fact that you know the mean of $y_1, y_2, y_3$.*

# BEGIN SOLUTION

TODO

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

Suppose the mean absolute deviation from the median in the full dataset
of 8 values is 6. What is the value of $z_1$?

*Hint: You'll need to use the results from earlier parts of this
question.*

( ) 2 
( ) correct3 
( ) 5 
( ) 6 
( ) 7 
( ) 9 
( ) 11

# BEGIN SOLUTION

TODO

# END SOLUTION

# END SUBPROB

# END PROB