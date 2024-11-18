# BEGIN PROB

-   For each of the following statements, ***clearly*** bubble **TRUE** or **FALSE**.

-   The **maximum** number of points you can earn on this problem is **10**, so you can get up to two statements incorrect and still earn full credit.

-   You do not need to show any work to earn full credit, but you can provide justification to possibly earn partial credit.

-   **For all statements to follow**, assume $\vec{x}_1, \vec{x}_2, \dotsc, \vec{x}_n\in\mathbb{R}^{d}$ are $d$-dimensional vectors, and each has a scalar response value $y_1,\dotsc, y_n$. Consider the multiple linear regression problem where

\begin{align*}
H(\vec{x}_i) = w_0 + w_1 \vec{x}_i^{(1)} + w_2 \vec{x}_i^{(2)} + \cdots + w_{d}\vec{x}_i^{(d)}.
\end{align*}

-   Let $X$ denote the design matrix and let $\vec{w}^\ast$ denote the
    optimal parameter vector with respect to MSE.

# BEGIN SUBPROB

If $X^TX$ is invertible, the matrix $P = X(X^TX)^{-1}X^T$ satisfies the equations $P^2 = P$ and $P^T = P$.

( ) TRUE
( ) FALSE

# BEGIN SOLUTION

TRUE

To see if this statement is true, we can plug in our definition for $P$ and check if these equations hold using various properties of matrix multiplication.

First, we see $P^2 = (X(X^TX)^{-1}X^T)(X(X^TX)^{-1}X^T) = X(X^TX)^{-1}(X^TX)(X^TX)^{-1}X^T$, using the asociative property. We can notice that $(X^TX)(X^TX)^{-1} = I$. Therefore: $$P^2 = X(X^TX)^{-1}(X^TX)(X^TX)^{-1}X^T = X(X^TX)^{-1}X^T = P$$
So $P^2 = P$ is true.

Next, we check $P^T$. A useful fact for this problem is that for any invertible matrix $A$, we have $(A^{-1})^T = (A^T)^{-1}$. Then we see $$P^T = (X(X^TX)^{-1}X^T)^T = X((X^TX)^{-1})^T X^T = X((X^TX)^T)^{-1} X^T = X(X^TX)^{-1}X^T = P$$
So $P^T = P$ is true.

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

The residual vector $\vec{r} = \vec{y} - X\vec{w}^\ast$ is orthogonal to the rows of $X$.

( ) TRUE
( ) FALSE

# BEGIN SOLUTION

FALSE

The wording here is tricky! Recall the residual vector, $\vec r$, is the same as the error vector $\vec e = \vec y - X \vec w^*$. We know $\vec e$ is orthogonal to the columns of $X$. Recall $X^T(\vec e) = 0$. This means the rows of $X^T \times \vec e$ will give us zero. However, when you transpose $X^T$ to get $X$ then the columns of $X \cdot \vec e = 0$.

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

The equation $\|\vec{x}_i + \vec{w}^\ast\|^2 = \|\vec{x}_i\|^2 + \|\vec{w}^\ast\|^2$ holds for each $1\leq i\leq n$.

( ) TRUE
( ) FALSE

# BEGIN SOLUTION

FALSE

This is not always true. This would be true if $\vec x_i$ and $\vec w^*$ were orthogonal. Here is an example when they are not:

Let the following hold:

- $\vec x_i = \begin{bmatrix} 1 \\ 0 \end{bmatrix}$
- $\vec w^* = \begin{bmatrix} 1 \\ 1 \end{bmatrix}$

Looking at the left side:

\begin{align*}
\|\vec{x}_i + \vec{w}^\ast\|^2 &= \|\begin{bmatrix} 1 \\ 0 \end{bmatrix} + \begin{bmatrix}1 \\ 1\end{bmatrix}\|\\
&= \|\begin{bmatrix} 2 \\ 1 \end{bmatrix}\|\\
&= 2^2 + 1^2\\
&= 4 + 1\\
&= 5
\end{align*}

Looking at the right side:

\begin{align*}
\|\vec{x}_i\|^2 + \|\vec{w}^\ast\|^2 &= \|\begin{bmatrix} 1 \\ 0 \end{bmatrix}\|^2 + \|\begin{bmatrix} 1 \\ 1 \end{bmatrix}\|^2\\
&= 1^2 + (1^2 + 1^2)\\
&= 1 + 2\\
&= 3
\end{align*}

As we know $5 \neq 3$, so it is not always true. $\|\vec{x}_i + \vec{w}^\ast\|^2 \neq \|\vec{x}_i\|^2 + \|\vec{w}^\ast\|^2$

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

The gradient of $f(\vec{w}) = y_i - H(\vec{x}_i)$ with respect to $\vec{w}$ is $\vec{x}_i$.

( ) TRUE
( ) FALSE

# BEGIN SOLUTION

FALSE

Let $H(\vec{x}) = \vec{w} \cdot Aug(\vec{x}) = w_0 + w_1 x^{(1)} + \cdots + w_d x^{(d)}$ be our hypothesis function. We can see that the gradient with respect to $\vec{w}$ is $Aug(\vec{x})$. Since $H$ is multiplied by $-1$ in our function $f(\vec{w})$, the gradient of $f(\vec{w})$ would be $-Aug(\vec{x}_i)$. Therefore, the statement is false.

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

$\vec{w}^\ast$ is the orthogonal projection of $\vec{y}$ onto the span of the columns of $X$.

( ) TRUE
( ) FALSE

# BEGIN SOLUTION

FALSE

$\vec w^*$ represents the vector of coefficients that would give the prest approximation of $\vec y$ (prediction) in terms of the columns of $X$. If $\vec w^*$ were orthogonal to $\vec y$ then it would mean $\vec y$ and $X$ may not have a relation to one another. No matter what $\vec w$ we choose $X \vec w$ could not approximate $\vec y$.

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

The empirical risk function $R_{\mathrm{sq}}$ can be written in the form $R_{\mathrm{sq}}(\vec{w}) = \frac{1}{n}\| X\vec{w}\|^2$.

( ) TRUE
( ) FALSE

# BEGIN SOLUTION

FALSE

An important aspect of risk (and loss) is the difference between the actual value ($\vec y$) and our prediction ($X \vec w$). We want to measure how far away our prediction is from our actual value. This equation only measures the length of $X \vec w$, so it ignores the difference, which means it does not help us quantify how "wrong we are" and is not the same as risk.

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

If $n \geq d+1$ then $(X^TX)^{-1}$ exists.

( ) TRUE
( ) FALSE

# BEGIN SOLUTION

FALSE

This is false because $n \geq d+1$ alone does not guarantee $(X^TX)^{-1}$ = exists.

Recall $X$ is an $n \times d$ matrix (with $n$ samples and $d$ features). For $(X^TX)^{-1}$ to exist $X$ must have $d$ linearly independent columns (span the $d$-dimensional space), which would make $X^TX$ full rank.

# END SOLUTION

# END SUBPROB

# END PROB