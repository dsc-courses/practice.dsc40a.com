# BEGIN PROB

<i>Originally Problem 5c on the Spring 2023 Final Part 1</i>

Now we solve the normal equations and find the solution to be
\begin{aligned}
            \vec{w}^* &= \begin{bmatrix} w_0^* \\ w_1^* \\ w_2^* \end{bmatrix}
\end{aligned}
Define a new vector:
\begin{aligned}
            \vec{w}^{\circ} &= \begin{bmatrix} w_0^{\circ} \\ w_1^{\circ} \\ w_2^{\circ} \end{bmatrix} = \begin{bmatrix} w_0^*+3 \\ w_1^*-4 \\ w_2^*-6 \end{bmatrix}
            
\end{aligned}

and consider the two prediction rules

\begin{aligned}
        H^*(\text{cells, lines, max iterations, variables}) &=  w_0^* + w_1^* \cdot \text{cells} \cdot \text{lines} + w_2^* \cdot (\text{max iterations})^{\text{variables} - 10}\\
        H^{\circ}(\text{cells, lines, max iterations, variables}) &=  w_0^{\circ} + w_1^{\circ} \cdot \text{cells} \cdot \text{lines} + w_2^{\circ} \cdot (\text{max iterations})^{\text{variables} - 10}
        
\end{aligned}

Let $\text{MSE}$ represent the mean squared error of a prediction
rule, and let $\text{MAE}$ represent the mean absolute error of a prediction
rule. Select the symbol that should go in each blank.

# BEGIN SUBPROB

$\text{MSE}(H^*)$ ___ $\text{MSE}(H^{\circ})$

( ) $\leq$
( ) $\geq$
( ) $=$

# BEGIN SOLUTION

$\leq$

Recall the equation for mean squared error: $\text{MSE}(H(x_i)) = \frac{1}{n}\sum_{i=1}^n(y_i-H(x_i))^2$. We can figure out which is bigger by subtracting  $\text{MSE}(H^{\circ})$ from $\text{MSE}(H^*)$. The difference between the squared differences is:
$$(y_i-H^*(x_i))^2-(y_i-H^{\circ}(x_i))^2$$Notice there is a squared element, which means that the differences of $w^*_0 - w^{\circ}_0$, $w^*_1 - w^{\circ}_1$, and $w^*_2 - w^{\circ}_2$ will appear as squared terms, which are always positive! This means adding these squared differences to $H^*$ will make it at least as large as the squared difference for $H^{\circ}$.

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

$(\text{MAE}(H^{\circ}))^2$ ___ $\text{MSE}(H^{\circ})$

( ) $\leq$
( ) $\geq$
( ) $=$

# BEGIN SOLUTION

$\geq$

Recall the equation for mean absolute error: $\text{MAE}(H(x_i)) = \frac{1}{n}\sum_{i=1}^n|y_i-H(x_i)|$.

This equation looks very similar to the mean squared error! We can actually take the square root of each sides of this equation to learn more about which side is larger:
$$
\begin{align*}
(\text{MAE}(H^\circ))^2 &\_\_\_ \text{MSE}(H^\circ) \\
\sqrt{(\text{MAE}(H^\circ))^2} &\_\_\_ \sqrt{\text{MSE}(H^\circ)} \\
\text{MAE}(H^\circ) &\_\_\_ \sqrt{\text{MSE}(H^\circ)}
\end{align*}
$$

The square root of $\text{MSE}$ is equal to $\text{MAE}$! These two elements are basically the same because squaring a value will lead to non-negatives and then it will be square rooted to match the absolute value from $\text{MAE}$. However the $\text{MSE}$ being square rooted also allows for it to be smaller than the $\text{MSE}$ making the correct symbol $\geq$.

# END SOLUTION

# END SUBPROB

# END PROB