# BEGIN PROB

Consider the usual setup for a multiple regression problem, as follows. Let $\vec{x}_1,\vec{x}_2,\dotsc, \vec{x}_{n}\in\mathbb{R}^d$ be a collection of feature vectors in $\mathbb{R}^d$, and let $X\in\mathbb{R}^{n\times (d+1)}$ be the corresponding design matrix. Each $\vec{x}_i$ has a label $y_i\in\mathbb{R}$, and let $\vec{y}\in\mathbb{R}^n$ be the vector of labels. We wish to fit the data and labels with a linear model
$$H(\vec{x}) = w_0 + w_1\vec{x}^{(1)} + w_2\vec{x}^{(2)}+\dotsc+ w_d\vec{x}^{(d)} \  = \vec{w}^T\mathrm{Aug}(\vec{x}).$$
where $\vec{w}\in\mathbb{R}^{d+1}$ is the vector of coefficients with intercept. Let $\vec{w}^\ast$ denote the optimal parameter vector with respect to mean squared error.

For each statement below, fill in the circle indicating the word(s) or phrase(s) which would make the statement correct if added to the sentence. *You do not need to show your work for full credit, but partial credit may be awarded for supporting calculations and reasoning.*

# BEGIN SUBPROB

At $\vec{w}^\ast$, the residual vector $\vec{y}-X\vec{w}^\ast$ is ________ to the column space of the design matrix $X$.

$\bigcirc$ neither   $\bigcirc$ orthogonal   $\bigcirc$ parallel

# BEGIN SOLUTION

At $\vec{w}^\ast$, the residual vector $\vec{y} - X\vec{w}^\ast$ is **orthogonal** to the column space of $X$. This is derived from the normal equations: 
$$X^T(\vec{y} - X\vec{w}^\ast) = 0,$$ 
which imply that the residuals are perpendicular to the space spanned by the columns of $X$.

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

The optimal parameter vector $w^\ast$ is found by setting the ________ of the mean squared error equal to ________ and solving the resulting equation.

$\bigcirc$ (residuals, $\vec{y}$)   $\bigcirc$ (gradient, the zero vector)   $\bigcirc$ (predicted labels, $X\vec{w}$)

# BEGIN SOLUTION

The optimal parameter vector $\vec{w}^\ast$ is found by setting the **gradient** of the mean squared error to **the zero vector**. The gradient is:
$$\nabla_w \| \vec{y} - X\vec{w} \|^2 = -2X^T(\vec{y} - X\vec{w}),$$ 
and solving $X^T(X\vec{w} - \vec{y}) = 0$ leads to the normal equation, which gives the minimum.

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

If the features in $X$ are linearly ________, the matrix $X^TX$ will be ________, making the normal equation solution possibly undefined.

$\bigcirc$ (dependent, nonsingular)   $\bigcirc$ (independent, singular)   $\bigcirc$ (dependent, noninvertible)

# BEGIN SOLUTION

If the features in $X$ are linearly **dependent**, the matrix $X^TX$ will be **singular (noninvertible)**. Linear dependence implies that the columns of $X$ are not linearly independent, leading to a determinant of zero for $X^TX$, which makes solving the normal equations impossible.

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

If $\vec{c}\in\mathbb{R}^d$ is a fixed vector, and we define $\vec{z}_i' = \vec{x}_i + \vec{c}$, then the *new* optimal parameter vector $\vec{w}'$ for the data $\{\vec{z}_i\}_{i=1}^{n}$ and labels $\vec{y}$ is equal to ________.

$\bigcirc$ $\vec{w}^\ast + \mathrm{Aug}(\vec{c})$   $\bigcirc$ $\vec{w}^\ast$   $\bigcirc$ $\vec{w}^\ast$ except possibly for $w_0$

# BEGIN SOLUTION

The new optimal parameter vector $\vec{w}'$ is **$\vec{w}^\ast$ except possibly for $w_0$**. Adding $\vec{c}$ shifts the features, leaving $w_1, w_2, \dots, w_d$ unchanged but altering the intercept:
$$w_0' = w_0 - \vec{w}^T \vec{c}.$$

(Think of the simple linear regression model - if we shift all the $x_i$'s by constant $c$ this doesn't affect the slope $w_1$ but does affect the intercept $w_0$.)

# END SOLUTION

# END SUBPROB

For the remaining two parts, fill in the circle which contains the **gradient** of each function. *You do not need to show your work for full credit, but partial credit may be awarded for supporting calculations and reasoning.*

# BEGIN SUBPROB

Calculate the gradient with respect to $\vec{x}$ of $F(\vec{x}) = \vec{w}^T\mathrm{Aug}(\vec{x})$.

$\bigcirc$ $\begin{bmatrix} w_1 & w_2 & \dotsc & w_d \end{bmatrix}^T$   $\bigcirc$ $\vec{x}$   $\bigcirc$ $\begin{bmatrix} w_0 & w_1 & \dotsc & w_d \end{bmatrix}^T$

# BEGIN SOLUTION

The gradient of $F(\vec{x}) = \vec{w}^T\mathrm{Aug}(\vec{x})$ with respect to $\vec{x}$ is $\begin{bmatrix} w_1 & w_2 & \dotsc & w_d \end{bmatrix}^T$. The first slot in $\mathrm{Aug}(\vec{x})$ is a constant $1$, which cancels out when differentiating.

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

Calculate the gradient with respect to $\vec{w}$ of $F(\vec{w}) = \|\vec{y}-X\vec{w}\|^2$.

$\bigcirc$ $-2X^TX\vec{w}$   $\bigcirc$ $-2(\vec{y}-X\vec{w})$   $\bigcirc$ $-2X^T(\vec{y}-X\vec{w})$

# BEGIN SOLUTION

First expand the squared norm:
$$F(\vec{w}) = (\vec{y} - X\vec{w})^T (\vec{y} - X\vec{w})$$ 

The gradient of $F(\vec{w})$ with respect to $\vec{w}$ is:
$$\nabla_{\vec{w}} F(\vec{w}) = \nabla_{\vec{w}} \left[ \vec{y}^T\vec{y} - 2\vec{y}^T X\vec{w} + \vec{w}^T X^T X \vec{w} \right]$$

Since $\vec{y}^T\vec{y}$ does not depend on $\vec{w}$, its derivative is zero. The derivative of $-2\vec{y}^T X\vec{w}$ is:
$$\nabla_{\vec{w}} \left( -2\vec{y}^T X\vec{w} \right) = -2 X^T \vec{y}$$

The derivative of $\vec{w}^T X^T X \vec{w}$ is (HW4 Problem 2):
$$\nabla_{\vec{w}} \left( \vec{w}^T X^T X \vec{w} \right) = 2 X^T X \vec{w}$$

Combine the derivatives:
$$\nabla_{\vec{w}} F(\vec{w}) = -2 X^T \vec{y} + 2 X^T X \vec{w}$$

Finally, simplify the expression:
$$\nabla_{\vec{w}} F(\vec{w}) = 2 X^T X \vec{w} - 2 X^T \vec{y} = 2 X^T (X\vec{w} - \vec{y})$$

Therefore, 
$$\nabla_{\vec{w}} F(\vec{w}) = -2 X^T (\vec{y} - X\vec{w})$$

# END SOLUTION

# END SUBPROB

# END PROB