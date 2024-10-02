# BEGIN PROB
Consider a dataset of $n$ values, $y_1, y_2, ..., y_n$, all of which are non-negative. We're interested in fitting a constant model, $H(x) = h$, to the data, using the new ``Sun God" loss function:

$$L_\text{sungod}(y_i, h) = w_i \left( y_i^2 - h^2  \right)^2$$

Here, $w_i$ corresponds to the ``weight" assigned to the data point $y_i$, the idea being that different data points can be weighted differently when finding the optimal constant prediction, $h^*$. 

\vspace{0.1in}

For example, for the dataset $y_1 = 1, y_2 = 5, y_3 = 2$, we will end up with different values of $h^*$ when we use the weights $w_1 = w_2 = w_3 = 1$ and when we use weights $w_1 = 8, w_2 = 4, w_3 = 3$.


# BEGIN SUBPROB

 Find $\frac{\partial L_\text{sungod}}{\partial h}$, the derivative of the Sun God loss function with respect to $h$. Show your work, and put a $\boxed{\text{box}}$ around your final answer.

# BEGIN SOLUTION

TODO

# END SOLUTION


# END SUBPROB


# BEGIN SUBPROB

 Prove that the constant prediction that minimizes empirical risk for the Sun God loss function is:

$$h^* = \sqrt{\frac{\sum_{i = 1}^n w_i y_i^2}{\sum_{i = 1}^n w_i}}$$

<!-- % \textit{Just as an example, for the dataset $y_1 = 1, y_2 = 5, y_3 = 2$:
% \begin{itemize}
%     \item Using the weights $w_1 = w_2 = w_3 = 1$, $h^* = \sqrt{10}$.
%     \item Using the weights $w_1 = 8, w_2 = 4, w_3 = 3$, $h^* = \sqrt{8}$.
% \end{itemize}
% } -->

# BEGIN SOLUTION

TODO

# END SOLUTION
    


# END SUBPROB

# BEGIN SUBPROB

 For a dataset of non-negative values $y_1, y_2, ..., y_n$ with weights $w_1, 1, ..., 1$, evaluate: $$\displaystyle \lim_{w_1 \rightarrow \infty} h^*$$

( ) The maximum of $y_1, y_2, ..., y_n$
( ) The mean of $y_1, y_2, ..., y_{n-1}$
( ) The mean of $y_2, y_3, ..., y_n$
( ) The mean of $y_2, y_3, ..., y_n$, multiplied by $\frac{n}{n-1}$
( ) $y_1$
( ) $y_n$

    
# BEGIN SOLUTION

TODO

# END SOLUTION

# END SUBPROB
    

    


# END PROB