# BEGIN PROB

Consider the dataset $x_1 = 1, x_2 = 2, x_3 = 3, x_4 = 4, x_5 = 5$.

# BEGIN SUBPROB

Which single element of the dataset would you change, and to what value,
to make $h^* = 4$ the single minimizing value for the following loss
function and corresponding empirical risk? Bubble in your choice of
$x_i$, if possible, and provide the new value of that $x_i$. If no such $x_i$ is possible, bubble in "Not possible\" and
explain why.
$$L(y_i, h) = \begin{cases} 0 & y_i = h \\ 1 & y_i \neq h \end{cases}$$

( ) $x_1$
( ) $x_2$
( ) $x_3$
( ) $x_4$
( ) $x_5$
( ) Not possible

Include an explanation.

# BEGIN SOLUTION

$x_1 = 4$ or $x_2 = 4$ or $x_3 = 4$ or $x_5 = 4$

Recall from lecture 0-1 loss (
$$L(y_i, h) = \begin{cases} 0 & y_i = h \\ 1 & y_i \neq h \end{cases}$$
) is minimized by the mode. This means we want to maximize the number of matches between $h$ and $y_i$. If $h^* = 4$ then we want to change values that are not equal to $4$ into $4$. This means any answer that is not $x_4$ can be changed to equal $4$ and it is possible.

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

Suppose we must modify $x_5$. What should the new value of $x_5$ be to make $h^* = 6$ for the following loss function and corresponding empirical risk?

$$L(y_i, h) = (y_i - h)^2$$

# BEGIN SOLUTION

$x_5$ should be modified to 20

We know that $L(y_i, h) = (y_i - h)^2$ is minimized by the mean. This means $h^* = \frac{1}{n} \sum_{i = 1}^n x_i$.

We can make the equation $h^* =6$ by writing $6 = \frac{1 + 2 + 3 + 4 + x_5'}{5}$. From here we simply solve for $x_5'$.

\begin{align*}
6 &= \frac{1 + 2 + 3 + 4 + x_5'}{5}\\
30 &= 1 + 2 + 3 + 4 + x_5'\\
30 &= 10 + x_5 \\
20 &= x_5
\end{align*}

Here we can see that $x_5$ should be changed to 20.

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

Suppose we must modify $x_1$. What should the new value of $x_1$ be to make $h^* = 6$ for the following loss function and corresponding
empirical risk?

$$L(y_i, h) = (y_i - h)^2$$

# BEGIN SOLUTION

$x_1$ should be modified to 16

Once again we know that $L(y_i, h) = (y_i - h)^2$ is minimized by the mean. This means $h^* = \frac{1}{n} \sum_{i = 1}^n x_i$.

We can make the equation $h^* =6$ by writing $6 = \frac{x_1' + 2 + 3 + 4 + 5}{5}$. From here we simply solve for $x_1'$.

\begin{align*}
6 &= \frac{x_1' + 2 + 3 + 4 + 5}{5}\\
30 &= x_1 + 2 + 3 + 4 + 5\\
30 &= x_1 + 14 \\
16 &= x_1
\end{align*}

Here we can see that $x_1$ should be changed to 16.

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

Consider the dataset $x_1 = 1, x_2 = 2, x_3 = 3, x_4 = 4, x_5 = 5$.

Which single element of the dataset would you change, and to what value,
to make $h^* = 4$ for the following loss function and corresponding
empirical risk? Bubble in your choice of $x_i$, if possible, and provide
the new value of that $x_i$ in the box below. If no such $x_i$ is
possible, bubble in "Not possible\" and explain why in the box below.
$$L(y_i, h) = |y_i - h|$$

( ) $x_1$
( ) $x_2$
( ) $x_3$
( ) $x_4$
( ) $x_5$
( ) Not possible

Include an explanation.

# BEGIN SOLUTION

$x_3 = 4$

This is absolute loss and is minimized by the median. This means we need to turn whatever the current median is into $4$.

When we look at the dataset ($x_1 = 1, x_2 = 2, x_3 = 3, x_4 = 4, x_5 = 5$) we can see the current median is $x_3 = 3$. This means all we need to do is change the $x_3$ to $4$.

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

Which single element of the dataset would you change, and to what value,
to make $h^* = 5$ for the following loss function and corresponding
empirical risk? Bubble in your choice of $x_i$, if possible, and provide
the new value of that $x_i$ in the box below. If no such $x_i$ is
possible, bubble in "Not possible\" and explain why in the box below.
$$L(y_i, h) = |y_i - h|$$

( ) $x_1$
( ) $x_2$
( ) $x_3$
( ) $x_4$
( ) $x_5$
( ) Not possible

Include an explanation.

# BEGIN SOLUTION

Not possible

This is absolute loss and is minimized by the median. This means we need to turn whatever the current median is into $4$.

When we look at the dataset ($x_1 = 1, x_2 = 2, x_3 = 3, x_4 = 4, x_5 = 5$) we can see the current median is $x_3 = 3$. However, if we change $x_3 = 5$ then the dataset would look like: $x_1 = 1, x_2 = 2, x_4 = 4, x_3 = 5, x_5 = 5$, which would make the median equal to 4. There is no way to make the median $5$ by only changing a single value.

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

Suppose we **delete** $x_2$, so the dataset is
$x_1 = 1, x_3=3, x_4=4, x_5=5$. What is the new value of $h^*$ for
following loss function and corresponding empirical risk?
$$L(y_i, h) = (y_i - h)^2$$

# BEGIN SOLUTION

The mean of the dataset: $\frac{13}{4}$

Once again we know that $L(y_i, h) = (y_i - h)^2$ is minimized by the mean. This means $h^* = \frac{1}{n} \sum_{i = 1}^n x_i$.

If we delete $x_2$ this means our equation becomes $\frac{1 + 3 + 4 + 5}{4} = \frac{13}{4}$.

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

Suppose we **delete** $x_3$, so the dataset is
$x_1 = 1, x_2=2, x_4=4, x_5=5$. Which of the following values of $h^*$
minimize the following loss function and corresponding empirical risk?
$$L(y_i, h) = |y_i - h|$$

[ ] 1
[ ] 1.5
[ ] 2
[ ] 2.5
[ ] 3
[ ] 3.5
[ ] 4
[ ] 4.5
[ ] 5

# BEGIN SOLUTION

2, 2.5, 3, 3.5, 4

Once again, recall $L(y_i, h) = |y_i - h|$ is minimized by the median. The new dataset is even and has a median between $2$ and $4$, which means any answer in-between (and including) these values should be selected.

# END SOLUTION

# END SUBPROB

# END PROB