# BEGIN PROB

<i>Source: [Spring 2024 Final](../sp24-final/index.html), Problem 2</i>

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

The values of the three blanks are: $y_2$, $z_3$, and any value between $z_1$ and $z_2$ (inclusive).

For the first blank, we know the median of the y-dataset minimizes mean absolute error of a constant prediction on the y-dataset. Since $y_1 < y_2 < y_3$, $y_2$ is the unique minimizer.

For the second blank, we can also use the fact that the median of the z-dataset minimizes mean absolute error of a constant prediction on the z-dataset. Since $z_1 < z_2 < z_3 < z_4 < z_5$, $z_3$ is the unique minimizer.

For the third blank, we know that when there are an odd number of data points in a dataset, any values between the middle two (inclusive) minimize mean absolute error. Here, the middle two in the full dataset of 8 are $z_1$ and $z_2$.

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

For any $h$, it is true that:

$$T_\text{abs}(h) = \alpha Y_\text{abs}(h) + \beta Z_\text{abs}(h)$$

for some constants $\alpha$ and $\beta$. What are the values of $\alpha$
and $\beta$? Give your answers as integers or simplified fractions with
no variables.

# BEGIN SOLUTION

$\alpha = \frac{3}{8}$, $\beta = \frac{5}{8}$.

This comes from the fact that:
$$T_\text{abs}(h) = \frac{3}{8} Y_\text{abs}(h) + \frac{5}{8} Z_\text{abs}(h)$$.

TODO: show algebraic manipulation.

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

Show that $Y_\text{abs}(z_1) = z_1 - 2$.

*Hint: Use the fact that you know the mean of $y_1, y_2, y_3$.*

# BEGIN SOLUTION

TODO: show the proof

Starts with $$Y_\text{abs}(z_1) = \frac{1}{3} \left( | z - y_1 | + | z - y_2 | + |z - y_3| \right)$$, realizes that since $$z_1 > y_3 > y_2 > y_1$$ all of the absolute values can be dropped and writes $$Y_\text{abs}(z_1) = \frac{1}{3} \left( (z_1 - y_1) + (z_1 - y_2) + (z_3 - y_3) \right)$$, and then simplifies this to $$Y_\text{abs}(h) = \frac{1}{3} \left( 3z_1 - (y_1 + y_2 + y_3) \right) = \frac{1}{3} \left( 3z_1 - 3 \cdot \bar{y}\right) = z_1 - \bar{y} = z_1 - 2$$.

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

Suppose the mean absolute deviation from the median in the full dataset
of 8 values is 6. What is the value of $z_1$?

*Hint: You'll need to use the results from earlier parts of this
question.*

( ) $2$ 
( ) $3$ 
( ) $5$ 
( ) $6$ 
( ) $7$ 
( ) $9$ 
( ) $11$

# BEGIN SOLUTION

$3$.

This comes from solving for $$z_1$$ in:

$$\frac{3}{8}(z_1 - 2) + \frac{5}{8}(12 - z_1) = 6$$

TODO: show algebraic manipulation.
# END SOLUTION

# END SUBPROB

# END PROB