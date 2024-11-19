# BEGIN PROB

**\[Eligible for midterm redemption\]**

You are given a dataset with the following data points and want to fit a
variety of hypothesis functions to predict $y$ from features $u$ and
$v$:

$$\begin{array}{|c|c|c|}
\hline
u & v & y \\
\hline
1 & 3  & 4  \\
3 & 0  & 6  \\
2 & 2  & 5  \\
4 & -4 & 8  \\
5 & -1 & 11 \\
\hline
\end{array}$$

You are also provided with the following hypothesis functions, used to
construct design matrices:

1.  $H_A(u, v) = w_0 + w_1 u + w_2 u^2 + w_3 u^3$

2.  $H_B(u, v) = w_0 u + w_1 u^2 + w_2 u^3 + w_3 u v$

3.  $H_C(u, v) = w_0 + w_1 u + w_2 v + w_3 v^2$

4.  $H_D(u, v) = w_0 + w_1 u + w_2 u^3 + w_3 u v$

$$X_1 = \begin{bmatrix}
    1 &  1 & 1 & 1 \\
    1 &  3 & 9 & 27 \\
    1 &  2 & 4 & 8 \\
    1 &  4 & 16 & 64 \\
    1 &  5 & 25 & 125
    \end{bmatrix} \ \ \ 
    X_2 = \begin{bmatrix}
    1 & 1 & 1   & 3 \\
    1 & 3 & 27  & 0 \\
    1 & 2 & 8   & 4 \\
    1 & 4 & 64  & -16 \\
    1 & 5 & 125 & -5
    \end{bmatrix}$$ $$X_3 = \begin{bmatrix}
    1 & 1 & 1 & 3 \\
    3 & 9 & 27 & 0 \\
    2 & 4 & 8 & 4 \\
    4 & 16 & 64 & -16 \\
    5 & 25 & 125 & -5
    \end{bmatrix} \ \ \ 
    X_4 = \begin{bmatrix}
    1 & 1 & 3  & 9 \\
    1 & 3 & 0  & 0 \\
    1 & 2 & 2  & 4 \\
    1 & 4 & -4 & 16 \\
    1 & 5 & -1 & 1
    \end{bmatrix}$$

# BEGIN SUBPROB

Which design matrix corresponds to $H_A(u, v)$?

( ) $X_1$
( ) $X_2$
( ) $X_3$
( ) $X_4$

# BEGIN SOLUTION

$X_1$

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

Which design matrix corresponds to $H_B(u, v)$?

( ) $X_1$
( ) $X_2$
( ) $X_3$
( ) $X_4$

# BEGIN SOLUTION

$X_3$

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

Which design matrix corresponds to $H_C(u, v)$?

( ) $X_1$
( ) $X_2$
( ) $X_3$
( ) $X_4$

# BEGIN SOLUTION

$X_4$

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

Which design matrix corresponds to $H_D(u, v)$?

( ) $X_1$
( ) $X_2$
( ) $X_3$
( ) $X_4$

# BEGIN SOLUTION

$X_2$

# END SOLUTION

# END SUBPROB

The following hypothesis functions are repeated from the previous page,
for your convenience, plus an additional hypothesis function $H_E$:

1.  $H_A(u, v) = w_0 + w_1 u + w_2 u^2 + w_3 u^3$

2.  $H_B(u, v) = w_0 u + w_1 u^2 + w_2 u^3 + w_3 u v$

3.  $H_C(u, v) = w_0 + w_1 u + w_2 v + w_3 v^2$

4.  $H_D(u, v) = w_0 + w_1 u + w_2 u^3 + w_3 u v$

5.  $H_E(u, v) = w_0 + w_1 u + w_2 u^2 + w_3 u^3 + w_4 v + w_5 v^2 + w_6 u v$

# BEGIN SUBPROB

Which of the five hypothesis functions above has the lowest mean squared
error on this dataset? Choose a hypothesis function $H(\cdot)$ and
briefly justify your answer in the space below.


( ) $H_A(u, v)$
( ) $H_B(u, v)$
( ) $H_C(u, v)$
( ) $H_D(u, v)$
( )$H_E(u, v)$

# BEGIN SOLUTION

Correct: $$H_E(u, v)$$ includes all features so it can (at least) express any lower-MSE hypothesis function like $$H_A, H_B, H_C, H_D$$. Because $$H_E$$ is the most "flexible" hypothesis function, it's also the most expressive and can fit our data the best, with the lowest mean squared error.

TODO

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

Suppose we use the lowest-MSE hypothesis function chosen above to make a
prediction for a new point $(u_\text{new}, v_\text{new}) = (10, 15)$. Is
this prediction likely to be accurate? Justify your answer.

# BEGIN SOLUTION

Argues "no" and provides justification: because of overfitting or extrapolation issues: if the lowest-MSE hypothesis function has too many terms, it may overfit (think of a high-degree polynomial overfitting a linear trend).

TODO

# END SOLUTION

# END SUBPROB

# END PROB