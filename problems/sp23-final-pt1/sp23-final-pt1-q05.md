# BEGIN PROB

Suppose we want to predict how long it takes to run a
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

<i>Originally Problem 5a on the Spring 2023 Final Part 1</i>

What are the dimensions of the design matrix $X$? AKA what are $r$ and $c$?

$r$ rows $\times$ $c$ columns

# BEGIN SOLUTION

$100 \text{rows} \times 3 \text{columns}$

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

<i>Originally Problem 5b on the Spring 2023 Final Part 1</i>

In **one sentence**, what does the entry in row 3, column 2
of the design matrix X represent? (Count rows and columns starting at 1,
not 0).

# BEGIN SOLUTION

This entry represents the product of the number of cells and number
of lines of code for the third Jupyter notebook in the training dataset.

# END SOLUTION

# END SUBPROB

# END PROB