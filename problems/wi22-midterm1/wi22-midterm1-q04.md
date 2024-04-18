# BEGIN PROB

(9 points) Consider the dataset shown below.

::: center
  $x^{(1)}$   $x^{(2)}$   $x^{(3)}$   $y$
  ----------- ----------- ----------- -----
  0           6           8           -5
  3           4           5           7
  5           -1          -3          4
  0           2           1           2
:::

# BEGIN SUBPROB

(5 points) We want to use multiple regression to fit a prediction rule
of the form
$$H(x^{(1)}, x^{(2)}, x^{(3)}) = w_0 + w_1 x^{(1)}x^{(3)} + w_2 (x^{(2)}-x^{(3)})^2.$$
Write down the design matrix $X$ and observation vector $\vec{y}$ for
this scenario. No justification needed.

# BEGIN SOLUTION

# END SOLUTION

# END SUBPROB # BEGIN SOLUTION

The design matrix $X$ and observation vector $\vec{y}$ are given by

::::: center
$X =$

::: bmatrix
1 & 0 & 4\
1 & 15 & 1\
1 & -15 & 4\
1 & 0 & 1
:::

, $y$ =

::: bmatrix
-5\
7\
4\
2
:::
:::::

# END SOLUTION # BEGIN SUBPROB

(4 points) For the $X$ and $\vec{y}$ that you have written down, let
$\vec{w}$ be the optimal parameter vector, which comes from solving the
normal equations $X^TX\vec{w}=X^T\vec{y}$. Let
$\vec{e} = \vec{y} - X \vec{w}$ be the error vector, and let $e_i$ be
the $i$th component of this error vector. Show that
$$4e_1+e_2+4e_3+e_4=0.$$

# BEGIN SOLUTION

# END SOLUTION

# END SUBPROB # BEGIN SOLUTION

We can rewrite the normal equations in terms of the error vector to get
$$\begin{aligned}
    X^TX\vec{w}&=X^T\vec{y} \\
    \vec{0} &= X^T\vec{y} -  X^TX\vec{w}  \\
    \vec{0} &= X^T( \vec{y} - X \vec{w}) \\
    \vec{0} &= X^T\vec{e}.
\end{aligned}$$ In particular, since one row of $X^T$ is

::: bmatrix
4 & 1 & 4 & 1
:::

, when we multiply $\vec{e}$ by this row, the result is zero. This says
that $4e_1+e_2+4e_3+e_4=0$, as desired.

# END SOLUTION

# END PROB