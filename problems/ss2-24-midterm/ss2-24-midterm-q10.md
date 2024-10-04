# BEGIN PROB

Suppose we want to fit a hypothesis function of the form: $$H(x) = w_0 + w_1 x^{(1)} + w_2 x^{(2)} + w_3 (x^{(1)})^2 + w_4 (x^{(1)} x^{(2)})^2$$

Our dataset looks like this: 

| $x^{(1)}$ | $x^{(2)}$ | $y$ |
|-----------|------------|-----|
| 1         | 6          | 7   |
| -3        | 8          | 2   |
| 4         | 1          | 9   |
| -2        | 7          | 5   |
| 0         | 4          | 6   |


We know we need to find an optimal parameter vector $\vec{w}^* = \left[w_0^* \ \  w_1^* \ \   w_2^* \ \  w_3^* \ \ w_4^* \right]^T$ that satisfies the normal equations. To do so, we build a design matrix, but our columns get all shuffled due to an error with our computer!
Our resulting design matrix is 

$$ X_\text{shuffled} = 
\begin{bmatrix}
36 & 6 & 1 & 1 & 1   \\ 
576 & 8 & -3& 1 & 9  \\ 
16 & 1 & 4 & 1 & 16  \\ 
196 & 7 & -2& 1 & 4  \\ 
0 & 4 & 0 & 1 & 0   
\end{bmatrix}
$$

If we solved the normal equations using this shuffled design matrix $X_\text{shuffled}$, we would not get our parameter vector $\vec{w}^* = \left[w_0^* \ \  w_1^* \ \   w_2^* \ \  w_3^* \ \ w_4^* \right]^T$ in the correct order. Let $\vec{s} = \left[ s_0 \ \ s_1 \ \ s_2 \ \ s_3 \ \ s_4 \right] $ be the parameter vector we find instead. Let's figure out which features correspond to the weight vector $\vec{s}$ that we found using the shuffled design matrix $X_\text{shuffled}$. Fill in the bubbles below.

# BEGIN SUBPROB

First weight $s_0$ after solving normal equations corresponds to the term in $H(x)$:

( ) intercept
( ) $x^{(1)}$
( ) $x^{(2)}$
( ) $(x^{(1)})^2$
( ) $(x^{(1)} x^{(2)})^2$

# BEGIN SOLUTION

$(x^{(1)} x^{(2)})^2$

# END SOLUTION
    


# END SUBPROB


# BEGIN SUBPROB

Second weight $s_1$ after solving normal equations corresponds to the term in $H(x)$:

( ) intercept
( ) $x^{(1)}$
( ) $x^{(2)}$
( ) $(x^{(1)})^2$
( ) $(x^{(1)} x^{(2)})^2$

# BEGIN SOLUTION

$x^{(2)}$

# END SOLUTION



# END SUBPROB

# BEGIN SUBPROB

Third weight $s_2$ after solving normal equations corresponds to the term in $H(x)$:

( ) intercept
( ) $x^{(1)}$
( ) $x^{(2)}$
( ) $(x^{(1)})^2$
( ) $(x^{(1)} x^{(2)})^2$

# BEGIN SOLUTION

$x^{(1)}$

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

Fourth weight $s_3$ after solving normal equations corresponds to the term in $H(x)$:

( ) intercept
( ) $x^{(1)}$
( ) $x^{(2)}$
( ) $(x^{(1)})^2$
( ) $(x^{(1)} x^{(2)})^2$

# BEGIN SOLUTION

intercept

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

Fifth weight $s_4$ after solving normal equations corresponds to the term in $H(x)$:

( ) intercept
( ) $x^{(1)}$
( ) $x^{(2)}$
( ) $(x^{(1)})^2$
( ) $(x^{(1)} x^{(2)})^2$

# BEGIN SOLUTION

intercept

# END SOLUTION

# END SUBPROB
    

# END PROB