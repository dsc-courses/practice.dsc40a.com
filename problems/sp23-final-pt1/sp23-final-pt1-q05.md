# BEGIN PROB

\[(11 points)\] Suppose we want to predict how long it takes to run a
Jupyter notebook on Datahub. For 100 different Jupyter notebooks, we
collect the following 5 pieces of information:

-   **cells**: number of cells in the notebook

-   **lines**: number of lines of code

-   **max iterations**: largest number of iterations in any loop in the
    notebook, or 1 if there are no loops

-   **variables**: number of variables defined in the notebook

-   **runtime**: number of seconds for the notebook to run on Datahub

Then we use multiple regression to fit a prediction rule of the form
$$H(\text{cells, lines, max iterations, variables}) =  w_0 + w_1 \cdot \text{cells} \cdot \text{lines} + w_2 \cdot (\text{max iterations})^{\text{variables} - 10}$$

# BEGIN SUBPROB

(3 points) What are the dimensions of the design matrix $X$?

::: center
rows $\times$ columns
:::

# BEGIN SOLUTION

# END SOLUTION

# END SUBPROB # BEGIN SUBPROB

(2 points) In **one sentence**, what does the entry in row 3, column 2
of the design matrix X represent? (Count rows and columns starting at 1,
not 0).

::: responsebox
1in This entry represents the product of the number of cells and number
of lines of code for the third Jupyter notebook in the training dataset.
:::

# BEGIN SOLUTION

# END SOLUTION

# END SUBPROB # BEGIN SUBPROB

(6 points) Now we solve the normal equations and find the solution to be
$$\begin{aligned}
            \vec{w}^* &= \begin{bmatrix} w_0^* \\ w_1^* \\ w_2^* \end{bmatrix}.
            \intertext{Define a new vector}
            \vec{w}^{\circ} &= \begin{bmatrix} w_0^{\circ} \\ w_1^{\circ} \\ w_2^{\circ} \end{bmatrix} = \begin{bmatrix} w_0^*+3 \\ w_1^*-4 \\ w_2^*-6 \end{bmatrix}
            
\end{aligned}$$ and consider the two prediction rules $$\begin{aligned}
        H^*(\text{cells, lines, max iterations, variables}) &=  w_0^* + w_1^* \cdot \text{cells} \cdot \text{lines} + w_2^* \cdot (\text{max iterations})^{\text{variables} - 10}\\
        H^{\circ}(\text{cells, lines, max iterations, variables}) &=  w_0^{\circ} + w_1^{\circ} \cdot \text{cells} \cdot \text{lines} + w_2^{\circ} \cdot (\text{max iterations})^{\text{variables} - 10}
        
\end{aligned}$$ Let MSE represent the mean squared error of a prediction
rule, and let MAE represent the mean absolute error of a prediction
rule. Select the symbol that should go in each blank.

**1.** (3 points) MSE$(H^*)$ MSE$(H^{\circ})$

( ) $\leq$ ( ) $\geq$ ( ) $=$

**2.** (3 points) $(\text{MAE}(H^{\circ}))^2$ MSE$(H^{\circ})$

( ) $\leq$ ( ) $\geq$ ( ) $=$

# BEGIN SOLUTION

# END SOLUTION

# END SUBPROB

# END PROB