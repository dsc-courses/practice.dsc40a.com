# BEGIN PROB

Suppose we want to fit a hypothesis function of the form: $$H(x) = w_0 + w_1 x^{(1)} + w_2 x^{(2)} + w_3 (x^{(1)})^2 + w_4 (x^{(1)} x^{(2)})^2$$
\vspace{-0.3cm}
Our dataset looks like this: 

| $x^{(1)}$ | $x^{(2)}$ | $y$ |
|-----------|------------|-----|
| 1         | 6          | 7   |
| -3        | 8          | 2   |
| 4         | 1          | 9   |
| -2        | 7          | 5   |
| 0         | 4          | 6   |

# BEGIN SUBPROB

Suppose we found $w_2^* = 15.6$ using multiple linear regression. Now, suppose we rescaled our data so feature vector $\vec{x^{(2)}}$ became $\left[60,\  80,\  10,\  70,\  40\right]^T$, and performed multiple linear regression in the same setting. What would the new value of $w_2^*$ (the weight on feature $x^{(2)}$ in $H(x)$) be? You do not need to simplify your answer.

# BEGIN SOLUTION

$w_2^* = 1.56$

Recall in linear regression, when a feature is rescaled by a factor of $c$, the corresponding weight is inversely scaled by $\frac{1}{c}$. This is because the coefficient adjusts to maintain the overall contribution of the feature to the prediction. In this problem we can see that $x^{(2)}$ has been scaled by a factor of 10! It changed from $\left[6,\  8,\  1,\  7,\  4\right]^T$ to $\left[60,\  80,\  10,\  70,\  40\right]^T$. This means our $w_2$ will be scaled by $\frac{1}{10}$. We can easily calculate $\frac{1}{10}w_2^* = \frac{1}{10}\cdot 15.6 = 1.56$.

<average>81</average>

# END SOLUTION


# END SUBPROB


# BEGIN SUBPROB

Suppose we found $w_4^* = 72$ using multiple linear regression. Now, suppose we rescaled our data so feature vector $\vec{x^{(1)}}$ became $\left[ \frac{1}{2},\  -\frac{3}{2},\  2,\  -1,\  0 \right]$ and $\vec{x^{(2)}}$ now became $\left[36, \ 48, \   6, \ 42, \ 24\right]^T$, and performed multiple linear regression in the same setting. What would the new value of $w_4^*$ (the weight on feature $(x^{(1)} x^{(2)})^2$ in $H(x)$) be? You do not need to simplify your answer.

# BEGIN SOLUTION

$w_4^* = \frac{72}{(\frac{6}{2})^2}$

Similar to the first part of the problem we need to find how $\vec{x^{(1)}}$ and $\vec{x^{(2)}}$ changed. We can then inversely scale $w_4^*$ by those values.

Let's start with $\vec{x^{(1)}}$. Originally $\vec{x^{(1)}}$ was $\left[1,\  -3,\  4,\  -2,\  0\right]^T$, but it becomes $\left[ \frac{1}{2},\  -\frac{3}{2},\  2,\  -1,\  0 \right]$. We can see the values were scaled by $\frac{1}{2}$.

We can now look at $\vec{x^{(2)}}$. Originally $\vec{x^{(2)}}$ was $\left[6,\  8,\  1,\  7,\  4\right]^T$, but it becomes $\left[36, \ 48, \   6, \ 42, \ 24\right]^T$. We can see the values were scaled by $6$.

We know $w_4^*$ is attached to the variable $(x^{(1)} x^{(2)})^2$. This means we need to multiply the scaled values we found and then square it. $(\frac{1}{2} \cdot 6)^2 = (3)^2 = 9$.

From here we simply inversely scale $w_4^*$. Originally $w_4^* = 72$, so we multiply by $\frac{1}{9}$ to get $72 \cdot \frac{1}{9} = \frac{72}{9}$ (which is equal to $\frac{72}{(\frac{6}{2})^2}$).

<average>35</average>

# END SOLUTION



# END SUBPROB

# BEGIN SUBPROB

Suppose we found $w_0^* = 4.47$ using multiple linear regression. Now, suppose our observation vector $\vec{y}$ now became $\left[12, \ 7, \ 14, \ 10, \ 11\right]^T$, and performed multiple linear regression in the same setting. What would the new value of $w_0^*$ be? You do not need to simplify your answer.

# BEGIN SOLUTION

$w_0^* = 9.47$

Recall $w_0^*$ is the intercept term and represents the value of the prediction $H(x)$ when all the features ($\vec{x^{(1)}}$ and $\vec{x^{(2)}}$) are zero. If all other features (the w_1^* and w_2^*) remain unchanged then the intercept adjusts to reflect the shifts in the mean of the observed $\vec y$.

Our original $\vec y$ was $\left[7, \ 2, \ 9, \ 5, \ 6\right]^T$, but became $\left[12, \ 7, \ 14, \ 10, \ 11\right]^T$. We need to calculate the original $\vec y$'s mean and the new $\vec y$'s mean.

Old $\vec y$'s mean:
$$
\frac{7 + 2 + 9 + 5 + 6}{5} = \frac{29}{5} = 5.8
$$

New $\vec y$'s mean:
$$
\frac{12 + 7 + 14 + 10 + 11}{5} = \frac{54}{5} = 10.8
$$

Our new $w_0^*$ is found by taking the old one and adding the difference of $10.8 - 5.8$. This means: $w_0^* = 4.47 + (10.8 - 5.8) = 4.47 + 5 = 9.47$.

<average>62</average>

# END SOLUTION



# END SUBPROB

# BEGIN SUBPROB

Suppose we found $w_1^* = 0.428$ using multiple linear regression. Now, suppose our observation vector $\vec{y}$ now became $\left[12, \ 7, \ 14, \ 10, \ 11\right]^T$, and performed multiple linear regression in the same setting. What would the new value of $w_1^*$ (the weight on feature $x^{(1)}$ in $H(x)$) be? You do not need to simplify your answer.

# BEGIN SOLUTION

$w_1^* = 0.428$

Our old $\vec y$ was $\left[7, \ 2, \ 9, \ 5, \ 6\right]^T$ and our new $\vec y$ is $\left[12, \ 7, \ 14, \ 10, \ 11\right]^T$. We can see that our old $\vec y$ has five added to each value to get our new $\vec y$.

Recall the slope ($w_1^*$) does not change if our $y_i$ shifts by a constant amount! This means $w_1^* = 0.428$.

<average>50</average>

# END SOLUTION


# END SUBPROB
    

# END PROB