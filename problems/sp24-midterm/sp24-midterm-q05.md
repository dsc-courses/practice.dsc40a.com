# BEGIN PROB

<i>Source: [Spring 2024 Midterm](../sp24-midterm/index.html), Problem 4a-c</i>

Suppose we want to fit a hypothesis function of the form:

$$H(x) = w_0 + w_1 x^2$$

Note that this is \textit{not} the simple linear regression hypothesis function, $H(x) = w_0 + w_1x$.

To do so, we will find the optimal parameter vector $\vec{w}^* = \begin{bmatrix} w_0^* \\ w_1^* \end{bmatrix}$ that satisfies the normal equations. The first 5 rows of our dataset are as follows, though note that our dataset has $n$ rows in total.

\begin{table}[H]
\centering
\begin{tabular}{|l|l|}
\hline
$x$ & $y$ \\ \hline
2   & 4   \\ \hline
-1  & 4   \\ \hline
3   & 4  \\ \hline
-7  & 4   \\ \hline
3   & 4   \\ \hline
\end{tabular}
\end{table}

Suppose that $x_1, x_2, ..., x_n$ have a mean of $\bar{x} = 2$ and a variance of $\sigma_x^2 = 10$.

# BEGIN SUBPROB

Write out the first 5 rows of the design matrix, $X$.

# BEGIN SOLUTION

TODO

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

Suppose, just in part (b), that after solving the normal equations, we find $\vec{w}^* = \begin{bmatrix} 2 \\ -5 \end{bmatrix}$. What is the predicted $y$ value for the augmented feature vector $\text{Aug}(\vec{x}) =  \begin{bmatrix} 1 \\ 4 \end{bmatrix}$? Give your answer as an integer with no variables. Show your work, and put 

a $\boxed{\text{box}}$ around your final answer.

# BEGIN SOLUTION

TODO

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

Let $X_\text{tri} = 3 X$. Using the fact that $\sum_{i = 1}^n x_i^2 = n \sigma_x^2 + n \bar{x}^2$, determine the value of the bottom-left value in the matrix $X_\text{tri}^T X_\text{tri}$, i.e. the value in the second row and first column. Give your answer as an expression involving $n$. Show your work, and put a $\boxed{\text{box}}$ around your final answer.

# BEGIN SOLUTION

TODO

# END SOLUTION

# END SUBPROB

# END PROB