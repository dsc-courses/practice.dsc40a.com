# BEGIN PROB

<i>Originally Problem 5c on the Spring 2023 Final Part 1</i>

Now we solve the normal equations and find the solution to be
<!-- $$ -->
\begin{aligned}
            \vec{w}^* &= \begin{bmatrix} w_0^* \\ w_1^* \\ w_2^* \end{bmatrix}
\end{aligned}
<!-- $$ -->
Define a new vector:
<!-- $$ -->
\begin{aligned}
            \vec{w}^{\circ} &= \begin{bmatrix} w_0^{\circ} \\ w_1^{\circ} \\ w_2^{\circ} \end{bmatrix} = \begin{bmatrix} w_0^*+3 \\ w_1^*-4 \\ w_2^*-6 \end{bmatrix}
            
\end{aligned}
<!-- $$ -->

and consider the two prediction rules

<!-- $$ -->
\begin{aligned}
        H^*(\text{cells, lines, max iterations, variables}) &=  w_0^* + w_1^* \cdot \text{cells} \cdot \text{lines} + w_2^* \cdot (\text{max iterations})^{\text{variables} - 10}\\
        H^{\circ}(\text{cells, lines, max iterations, variables}) &=  w_0^{\circ} + w_1^{\circ} \cdot \text{cells} \cdot \text{lines} + w_2^{\circ} \cdot (\text{max iterations})^{\text{variables} - 10}
        
\end{aligned}
<!-- $$ -->

Let MSE represent the mean squared error of a prediction
rule, and let MAE represent the mean absolute error of a prediction
rule. Select the symbol that should go in each blank.

# BEGIN SUBPROB

MSE$(H^*)$ MSE$(H^{\circ})$

( ) $\leq$
( ) $\geq$
( ) $=$

# BEGIN SOLUTION

$\leq$

TODO

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

$(\text{MAE}(H^{\circ}))^2$ MSE$(H^{\circ})$

( ) $\leq$
( ) $\geq$
( ) $=$

# BEGIN SOLUTION

$\geq$

TODO

# END SOLUTION

# END SUBPROB

# END PROB