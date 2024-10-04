# BEGIN PROB

Consider a dataset of $n$ values, $y_1, y_2, \dots, y_n$, all of which are non-negative. We are interested in fitting a constant model, $H(x) = h$, to the data using the ``Jack" loss function, defined as:

$L_{\text{Jack}}(y_i, h) =
\begin{cases} 
\alpha \cdot (y_i - h)^2 & \text{if } y_i \geq h, \\
\beta \cdot |y_i - h|^3 & \text{if } y_i < h,
\end{cases}$

where $\alpha$ and $\beta$ are positive constants that weight the squared and cubic loss components differently depending on whether the prediction $h$ underestimates or overestimates the true value $y_i$.

# BEGIN SUBPROB

Find $\frac{d L_\text{Jack}}{d h}$, the derivative of the Jack loss function with respect to $h$. Show your work, and put a $\boxed{\text{box}}$ around your final answer.

\textit{Hint: The derivative of a piecewise function is also a piecewise function.}

# BEGIN SOLUTION

TODO

# END SOLUTION
    


# END SUBPROB


# BEGIN SUBPROB

Prove that for the constant prediction $h^*$ minimizing empirical risk for the Jack loss function, the following quantities sum to 0:

1) the sum of the derivatives of the losses for the overestimated values (when $h^* > y_i$), and
2) the sum of the derivatives of the losses for the underestimated values (when $h^* \leq y_i$).

_Hint: You do not need to solve for the optimal value of $h^*$. Instead, walk through the general process of minimizing a risk function, and think about the equations you come across._

# BEGIN SOLUTION

TODO

# END SOLUTION



# END SUBPROB

# BEGIN SUBPROB

For any set of values $y_1, y_2, ..., y_n$ in sorted order $y_1 \leq y_2 \leq ... \leq y_n$, evaluate $h^*$ when $\alpha = 0$.

( ) 0
( ) Median({$y_i$})
( ) Any number $\leq y_1$
( ) Any number $\geq y_n$
( ) $\overline y$
( ) Impossible to tell

# BEGIN SOLUTION

Any number $\leq y_1$

# END SOLUTION



# END SUBPROB

# BEGIN SUBPROB

For any set of values $y_1, y_2, ..., y_n$ in sorted order $y_1 \leq y_2 \leq ... \leq y_n$, evaluate $h^*$ when $\beta = 0$.

( ) 0
( ) Median({$y_i$})
( ) Any number $\leq y_1$
( ) Any number $\geq y_n$
( ) $\overline y$
( ) Impossible to tell

# BEGIN SOLUTION

Any number $\geq y_n$

# END SOLUTION



# END SUBPROB
    

# END PROB