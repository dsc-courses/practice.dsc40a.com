# BEGIN PROB

<i>Source: [Summer Session 2 2024 Final](../ss2-24-final/index.html), Problem 4a-f</i>

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

We can easily create the design matrix from $H_A(u, v) = w_0 + w_1 u + w_2 u^2 + w_3 u^3$ by viewing the order of variables and how they are being manipulated. We can see there is a $w_0$ term, which means that the first column should be a vector of ones.

This means we know:

$$X_? = \begin{bmatrix}
    1 &  ? & ? & ? \\
    1 &  ? & ? & ? \\
    1 &  ? & ? & ? \\
    1 &  ? & ? & ? \\
    1 &  ? & ? & ?
    \end{bmatrix}$$

This immediately eliminates $X_3$. We now see that the second column should be $\vec u$. We are told the values inside of the vector at the top, which means we get:

$$X_? = \begin{bmatrix}
    1 &  1 & ? & ? \\
    1 &  3 & ? & ? \\
    1 &  2 & ? & ? \\
    1 &  4 & ? & ? \\
    1 &  5 & ? & ?
    \end{bmatrix}$$

This does not eliminate any of our values, so we look to see the next column will be $\vec u^2$. This means:

$$X_? = \begin{bmatrix}
    1 &  1 & (1)^2 & ? \\
    1 &  3 & (3)^2 & ? \\
    1 &  2 & (2)^2 & ? \\
    1 &  4 & (4)^2 & ? \\
    1 &  5 & (5)^2 & ?
    \end{bmatrix} = \begin{bmatrix}
    1 &  1 & 1 & ? \\
    1 &  3 & 9 & ? \\
    1 &  2 & 4 & ? \\
    1 &  4 & 16 & ? \\
    1 &  5 & 25 & ?
    \end{bmatrix}$$

Here we can now eliminate $X_2$ and $X_4$, so we know the answer must be $X_1$!

<average>100</average>

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

We can easily create the design matrix from $H_B(u, v) = w_0 u + w_1 u^2 + w_2 u^3 + w_3 u v$ by viewing the order of variables and how they are being manipulated. We can see there is a $w_0$ term that is being modified, which means that the first column should be a vector of ones multiplied by $\vec u$.

This means we know:

$$X_? = \begin{bmatrix}
    1 * 1 &  ? & ? & ? \\
    1 * 3 &  ? & ? & ? \\
    1 * 2 &  ? & ? & ? \\
    1 *4 &  ? & ? & ? \\
    1 * 5 &  ? & ? & ?
    \end{bmatrix} = \begin{bmatrix}
    1 &  ? & ? & ? \\
    3 &  ? & ? & ? \\
    2 &  ? & ? & ? \\
    4 &  ? & ? & ? \\
    5 &  ? & ? & ?
    \end{bmatrix}$$

We can see the only design matrix with this first column is $X_3$.

<average>100</average>

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

We can easily create the design matrix from $H_C(u, v) = w_0 + w_1 u + w_2 v + w_3 v^2$ by viewing the order of variables and how they are being manipulated. We can see there is a $w_0$ term, which means that the first column should be a vector of ones.

This means we know:

$$X_? = \begin{bmatrix}
    1 &  ? & ? & ? \\
    1 &  ? & ? & ? \\
    1 &  ? & ? & ? \\
    1 &  ? & ? & ? \\
    1 &  ? & ? & ?
    \end{bmatrix}$$

This immediately eliminates $X_3$. We now see that the second column should be $\vec u$. We are told the values inside of the vector at the top, which means we get:

$$X_? = \begin{bmatrix}
    1 &  1 & ? & ? \\
    1 &  3 & ? & ? \\
    1 &  2 & ? & ? \\
    1 &  4 & ? & ? \\
    1 &  5 & ? & ?
    \end{bmatrix}$$

This does not eliminate any of our values, so we look to see the next column will be $\vec v$. This means:

$$X_? = \begin{bmatrix}
    1 &  1 & 3 & ? \\
    1 &  3 & 0 & ? \\
    1 &  2 & 2 & ? \\
    1 &  4 & -4 & ? \\
    1 &  5 & -1 & ?
    \end{bmatrix}$$

Here we can eliminate $X_1$ and $X_2$, which means our answer is $X_4$.

<average>100</average>

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

We can easily create the design matrix from $H_D(u, v) = w_0 + w_1 u + w_2 u^3 + w_3 u v$ by viewing the order of variables and how they are being manipulated. We can see there is a $w_0$ term, which means that the first column should be a vector of ones.

This means we know:

$$X_? = \begin{bmatrix}
    1 &  ? & ? & ? \\
    1 &  ? & ? & ? \\
    1 &  ? & ? & ? \\
    1 &  ? & ? & ? \\
    1 &  ? & ? & ?
    \end{bmatrix}$$

This immediately eliminates $X_3$. We now see that the second column should be $\vec u$. We are told the values inside of the vector at the top, which means we get:

$$X_? = \begin{bmatrix}
    1 &  1 & ? & ? \\
    1 &  3 & ? & ? \\
    1 &  2 & ? & ? \\
    1 &  4 & ? & ? \\
    1 &  5 & ? & ?
    \end{bmatrix}$$

We cannot eliminate any of the design matrices, so we move to the next column, which is $\vec u^3$. This means:

$$X_? = \begin{bmatrix}
    1 &  1 & (1)^3 & ? \\
    1 &  3 & (3)^3 & ? \\
    1 &  2 & (2)^3 & ? \\
    1 &  4 & (4)^3 & ? \\
    1 &  5 & (5)^3 & ?
    \end{bmatrix}
    = \begin{bmatrix}
    1 &  1 & 1 & ? \\
    1 &  3 & 27 & ? \\
    1 &  2 & 8 & ? \\
    1 &  4 & 64 & ? \\
    1 &  5 & 125 & ?
    \end{bmatrix}$$

Now we can eliminate the design matrices $X_1$ and $X_4$, which means the answer is $X_2$.

<average>100</average>

# END SOLUTION

# END SUBPROB

The following hypothesis functions are repeated from the previous subparts, for your convenience, plus an additional hypothesis function $H_E$:

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
( ) $H_E(u, v)$

# BEGIN SOLUTION

$H_E(u, v)$

$H_E(u, v)$ contains the most information. $H_E$ has $\vec u$ and $\vec v$.This means we have information about both variables. We also see it has every component present in the other functions ($H_A, H_B, H_C, H_D$). This makes $H_E$ the most expressive, which will allow it to fit our data the best.

<average>56</average>

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

Suppose we use the lowest-MSE hypothesis function chosen above to make a
prediction for a new point $(u_\text{new}, v_\text{new}) = (10, 15)$. Is
this prediction likely to be accurate? Justify your answer.

# BEGIN SOLUTION

No

This prediction is not likely to be accurate due to overfitting or extrapolation issues. If there are too many terms there is a higher chance the function is overfitting the training data and will not generalize well to new points. You can think of a high-degree polynomial overfitting a linear trend.

<average>77</average>

# END SOLUTION

# END SUBPROB

# END PROB