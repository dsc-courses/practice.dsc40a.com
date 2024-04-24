# BEGIN PROB

_Originally Problem 5 on the first Winter 2024 Midterm Exam._

Suppose the following information is given for a linear regression:

:::: center
$X =$

::: bmatrix
1 & 2\
1 & -1\
:::

$\Vec{y} =
    \begin{bmatrix}
    a\\
    b\\
    \end{bmatrix}$ $\Vec{w}^{*} =
    \begin{bmatrix}
    1\\
    2\\
    \end{bmatrix}$
::::

Where X is the design matrix, $\Vec{y}$ is the observation vector, and
$\Vec{w}^{*}$ is the optimal parameter vector. Solve for parameter a and
b using the normal equation, show your work.

# BEGIN SOLUTION

Since $\Vec{w}^{*}$ is the optimal parameter vector, it must satisfy the
Normal Equation: $$\begin{aligned}
        X^{T}X\Vec{w} = X^{T}\Vec{y}
    
\end{aligned}$$ The left hand side of the equation will read:

::::::::: center
$X^{T}X\Vec{w} =$

::: bmatrix
1 & 1\
2 & -1\
:::

::: bmatrix
1 & 2\
1 & -1\
:::

::: bmatrix
1\
2\
:::

=

::: bmatrix
2 & 1\
1 & 5\
:::

::: bmatrix
1\
2\
:::

=

::: bmatrix
4\
11\
:::
:::::::::

The right hand side of the equation is given by:

:::::: center
$X^{T}\vec{y} =$

::: bmatrix
1 & 1\
2 & -1\
:::

::: bmatrix
a\
b\
:::

=

::: bmatrix
a+b\
2a-b\
:::
::::::

By setting the left hand side and right hand side equal to each other,
we will obatin the following system of equations:

::::: center
::: bmatrix
4\
11\
:::

=

::: bmatrix
a+b\
2a-b\
:::
:::::

So we obtained this set of equations: $$\begin{aligned}
        &4 = a + b\\
        &11 = 2a-b
    
\end{aligned}$$ To sole this equation set, we can add them together:
$$\begin{aligned}
       4+11 &= a + b + 2a -b\\
       3a &= 15\\
       a &= 5\\
       b &= -1\\
    
\end{aligned}$$

# END SOLUTION

# END PROB