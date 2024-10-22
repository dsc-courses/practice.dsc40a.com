# BEGIN PROB

Suppose we have already fit a multiple regression hypothesis function of the form: $$H(x) = w_0 + w_1 x^{(1)} + w_2 x^{(2)}$$

Now, suppose we add the feature $(x^{(1)} + x^{(2)})$ when performing multiple regression. Below, answer ``Yes/No" to the following questions and rigorously justify why certain behavior will or will not occur. Your answer must mention linear algebra concepts such as rank and linear independence in relation to the design matrix, weight vector $\vec{w^*}$, and hypothesis function $H(x)$.

# BEGIN SUBPROB

Which of the following are true about the new design matrix $X_\text{new}$ with our added feature  $(x^{(1)} + x^{(2)})$?

[ ] The columns of $X_\text{new}$ are linearly independent.
[ ] The columns of $X_\text{new}$ are linearly dependent.
[ ] $\vec{y}$ is orthogonal to all the columns of $X_\text{new}$.
[ ] $\vec{y}$ is orthogonal to all the columns of the original design matrix $X$.
[ ] The columns of $X_\text{new}$ have the same span as the original design matrix $X$.
[ ] $X_\text{new}^TX_\text{new}$ is a full-rank matrix.
[ ] $X_\text{new}^TX_\text{new}$ is not a full-rank matrix.

# BEGIN SOLUTION

The columns of $X_\text{new}$ are linearly dependent.
The columns of $X_\text{new}$ have the same span as the original design matrix $X$.
$X_\text{new}^TX_\text{new}$ is not a full-rank matrix.

Let's go through each of the options and determine if they are true or false.

**The columns of $X_\text{new}$ are linearly independent.**

This statement is false because $(x^{(1)} + x^{(2)})$ is a linear combination of the original features (linearly dependent). This means the added feature does not provide any new, independent information to the model.

**The columns of $X_\text{new}$ are linearly dependent.**

This statement is true because $(x^{(1)} + x^{(2)})$ is a linear combination of the original features.

**$\vec{y}$ is orthogonal to all the columns of $X_\text{new}$.**

This statement is false because there is no justification for othogonality. It is usually not the case that $\vec y$ is orthogonal to the columns of $X_\text{new}$ because the goal of regression is to find a linear relatiionship between the predictors and the response variable. Since we have some regression coefficients ($w_0, w_1, w_2$) this implies there exists a relationship between $\vec y$ and $X_\text{new}$.

**$\vec{y}$ is orthogonal to all the columns of the original design matrix $X$.**

This statement is false because there is no justification for othogonality. It is usually not the case that $\vec y$ is orthogonal to the columns of $X$ because the goal of regression is to find a linear relatiionship between the predictors and the response variable. Since we have some regression coefficients ($w_0, w_1, w_2$) this implies there exists a relationship between $\vec y$ and $X$.

**The columns of $X_\text{new}$ have the same span as the original design matrix $X$.**

This statement is true because $(x^{(1)} + x^{(2)})$ is a linear combination of the original features the span does not change.

**$X_\text{new}^TX_\text{new}$ is a full-rank matrix.**

This statement is false because there is a linearly dependent column!

**$X_\text{new}^TX_\text{new}$ is not a full-rank matrix.**

This statement is true because of linear dependence.


# END SOLUTION
    


# END SUBPROB


# BEGIN SUBPROB

Is there more than one optimal weight vector $\vec{w^*}$ that produces the lowest mean squared error hypothesis function $H(x) = w_0^* + w_1^* x^{(1)} + w_2^* x^{(2)} + w_4^*(x^{(1)} + x^{(2)})$? 

( ) Yes
( ) No

Explain your answer.

# BEGIN SOLUTION

Yes

There can be multiple optimal weight vectors $\vec w^*$ that achieve the lowest mean squared error for the hypothesis function because of the linear dependence between the columns in the design matrix. This results in non-unique solutions for the weight coefficients, allowing for various combinations of weights that produce the same optimal prediction outcome.

# END SOLUTION



# END SUBPROB

# BEGIN SUBPROB

Does the best possible mean squared error of the new hypothesis function differ from that of the previous hypothesis function?

( ) Yes
( ) No

Explain your answer.

# BEGIN SOLUTION

No

When we have a linear combination $(x^{(1)} + x^{(2)})$ we are not enhancing the model's capavility to fit the data in a way that would lower the best possible mean squared error. This means both models are capturing the same underlying relationship between the predictors and the response variable. Making it so that the mean squared error of the new hypothesis function does not differ from that of the previous hypothesis function.

# END SOLUTION

# END SUBPROB

# END PROB