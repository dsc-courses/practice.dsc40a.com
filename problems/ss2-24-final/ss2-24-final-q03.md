# BEGIN PROB

<i>Source: [Summer Session 2 2024 Final](../ss2-24-final/index.html), Problem 3a-g</i>

Consider the following vectors in $\mathbb{R}^3$, where
$\alpha \in \mathbb{R}$ is a scalar:

$$\vec{v}_1 = \begin{bmatrix} 0 \\ 1 \\ 1 \end{bmatrix}, \quad 
\vec{v}_2 = \begin{bmatrix} 1 \\ 0 \\ 1 \end{bmatrix}, \quad 
\vec{v}_3 = \begin{bmatrix} \alpha \\ 1 \\ 2 \end{bmatrix}$$

# BEGIN SUBPROB

For what value(s) of $\alpha$ are $\vec{v}_1, \vec{v}_2,$ and
$\vec{v}_3$ linearly independent? Show your work, and put your answer in
a box.

# BEGIN SOLUTION

The vectors are linearly independent for any $\alpha \neq 1$.

To be linearly independent it means there is not a linear combination between any of the vectors. We can see that if we add $\vec v_1$ and $\vec v_2$ it looks almost like $\vec v_3$, so as long as we can make it so $\alpha \neq 1$ then the vectors will be independent.

<average>69</average>

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

For what value(s) of $\alpha$ are $\vec{v}_1$ and $\vec{v}_3$
orthogonal? Show your work, and put your answer in a box.

# BEGIN SOLUTION

We know for $\vec v_1$ and $\vec v_3$ to be orthogonal their dot product should equal zero.

$$\vec v_1 \cdot \vec v_3 = (0)(\alpha) + (1)(1) + (1)(2) = 0$$

There are no values of $\alpha$ for which $\vec{v}_1, \vec{v}_3$ are orthogonal. We can see $(0)(\alpha) = 0$, which means that we cannot manipulate $\alpha$ in any way to make the vectors orthogonal.

<average>88</average>

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

For what value(s) of $\alpha$ are $\vec{v}_2$ and $\vec{v}_3$
orthogonal? Show your work, and put your answer in a box.

# BEGIN SOLUTION

$\alpha = -2$

We know for $\vec v_2$ and $\vec v_3$ to be orthogonal their dot product should equal zero.

The dot product is:

$$
\vec v_2 \cdot \vec v_3 = (1)(\alpha) + (0)(1) + (1)(2)
$$

So we can do:

\begin{align*}
0 &= (1)(\alpha) + (0)(1) + (1)(2)\\
0 &=\alpha + 0 + 2\\
-2 &= \alpha
\end{align*}

We can clearly see when $\alpha = -2$ then the dot product will equal zero.

<average>100</average>

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

Regardless of your answer above, assume in this part that $\alpha = 3$.
Is the vector $\begin{bmatrix}
3 \\
5 \\
8
\end{bmatrix}$ in $\textbf{span}(\vec{v}_1, \vec{v}_2, \vec{v}_3)$?

( ) Yes
( ) No

# BEGIN SOLUTION

Yes

If $\alpha = 3$ and all three vectors are independent from one another then any vector in $\mathbb{R}^3$ is in the span of 3 linearly independent vectors in $\mathbb{R}^3$.

<average>94</average>

# END SOLUTION

# END SUBPROB

*The following information is repeated from the previous page, for your
convenience.*

Consider the following vectors in $\mathbb{R}^3$, where
$\alpha \in \mathbb{R}$ is some scalar:

$$\vec{v}_1 = \begin{bmatrix} 0 \\ 1 \\ 1 \end{bmatrix}, \quad 
\vec{v}_2 = \begin{bmatrix} 1 \\ 0 \\ 1 \end{bmatrix}, \quad 
\vec{v}_3 = \begin{bmatrix} \alpha \\ 1 \\ 2 \end{bmatrix}$$

# BEGIN SUBPROB

What is the projection of the vector $\begin{bmatrix}
3 \\
5 \\
8
\end{bmatrix}$ onto $\vec{v}_1$? Provide your answer in the form of a
vector. Show your work, and put your answer in a box.

# BEGIN SOLUTION

$\begin{bmatrix}0 \\ 6.5 \\ 6.5 \end{bmatrix}$

We follow the equation  $\frac{\begin{bmatrix}3 \\ 5 \\ 8\end{bmatrix} \cdot \vec v_1}{\vec v_1 \cdot \vec v_1} \vec v_1$ to find the projection of $\begin{bmatrix}3 \\ 5 \\ 8\end{bmatrix}$ onto $\vec{v_1}$:

\begin{align*}
\frac{\begin{bmatrix}3 \\ 5 \\ 8\end{bmatrix} \cdot \begin{bmatrix}0 \\ 1 \\ 1 \end{bmatrix}}{\begin{bmatrix}0 \\ 1 \\ 1 \end{bmatrix}\cdot \begin{bmatrix}0 \\ 1 \\ 1 \end{bmatrix}} \begin{bmatrix}0 \\ 1 \\ 1 \end{bmatrix} &= \frac{13}{2}  \begin{bmatrix}0 \\ 1 \\ 1 \end{bmatrix}\\
&= \begin{bmatrix}0 \\ 6.5 \\ 6.5 \end{bmatrix}
\end{align*}

<average>58</average>

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

*The following information is repeated from the previous page, for your convenience.*

Consider the following vectors in $\mathbb{R}^3$, where
$\alpha \in \mathbb{R}$ is some scalar:

$$\vec{v}_1 = \begin{bmatrix} 0 \\ 1 \\ 1 \end{bmatrix}, \quad 
\vec{v}_2 = \begin{bmatrix} 1 \\ 0 \\ 1 \end{bmatrix}, \quad 
\vec{v}_3 = \begin{bmatrix} \alpha \\ 1 \\ 2 \end{bmatrix}$$

What is the orthogonal projection of the vector $\begin{bmatrix}
3 \\
15 \\
18
\end{bmatrix}$ onto $\textbf{span}(\vec{v}_1, \vec{v}_2)$? Note that for
$X = \begin{bmatrix}
            0 & 1 \\ 1 & 0 \\ 1 & 1
        \end{bmatrix}$, we have

$$(X^T X) ^{-1}X^T = \begin{bmatrix}
            -\frac{1}{3} & \frac{2}{3} & \frac{1}{3} \\[6pt]
            \frac{2}{3} & -\frac{1}{3} & \frac{1}{3}  
        \end{bmatrix}$$ Write your answer in the form of coefficients
that multiply $\vec{v}_1$ and $\vec{v}_2$ and yield a vector $\vec{p}$
that is the orthogonal projection requested above.

$\vec{p} = \_\_(a)\_\_ \cdot \vec{v}_1 + \_\_(b)\_\_ \cdot \vec{v}_2$

What goes in $\_\_(a)\_\_$ and $\_\_(b)\_\_$?

# BEGIN SOLUTION

To find what goes in $\_\_(a)\_\_$ and $\_\_(b)\_\_$ we need to multiply $(X^T X)^{-1}X^T$ and $\vec y$.

\begin{align*}
\begin{bmatrix} a \\ b \end{bmatrix} &= (X^T X)^{-1}X^T \begin{bmatrix}3 \\ 15 \\ 18\end{bmatrix}\\
\begin{bmatrix} a \\ b \end{bmatrix} &= \begin{bmatrix} -\frac{1}{3}(3) & \frac{2}{3}(15) & \frac{1}{3}(18) \\ \frac{2}{3}(3) & -\frac{1}{3}(15) & \frac{1}{3}(18) \end{bmatrix}\\
\begin{bmatrix} a \\ b \end{bmatrix} &= \begin{bmatrix} -1 + 10 + 15 \\ 2 - 5 + 6 \end{bmatrix}\\
\begin{bmatrix} a \\ b \end{bmatrix} &= \begin{bmatrix} 15 \\ 3 \end{bmatrix}\\
\end{align*}

<average>73</average>

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

Is it true that, for the orthogonal projection $\vec{p}$ from above, the
entries of $\vec{e} = \vec{p} \ - \begin{bmatrix} 3 \\ 15 \\ 18 \end{bmatrix}$ sum
to $0$? Explain why or why not. Your answer must mention characteristics
of $\vec{v}_1,\vec{v}_2,$ and/or $X$ to receive full credit.

( ) Yes
( ) No

Explain your answer

# BEGIN SOLUTION

Yes

*Note: Design matrix $X$ lacks a column of all 1s (and the span of its columns does not include all 1s), so residuals don't necessarily not sum to 0. This means we need more evidence!*

$\vec{p}$ is the orthogonal projection of $\begin{bmatrix}3\\15\\18\end{bmatrix}$ onto $\text{span}(\vec{v_1}, \vec{v_2})$ where $\vec{v_1}$ and $\vec{v_2}$ are the column of the matrix $X$. From the instructions we know: $\vec{e} = \vec{p} \ - \begin{bmatrix} 3 \\ 15 \\ 18 \end{bmatrix}$. This means if $\begin{bmatrix}3\\15\\18\end{bmatrix}$ lies in $\text{span}(\vec{v_1}, \vec{v_2})$ then $\vec{e} = \vec{0}$. We know $\vec{p}$ is exactly $\begin{bmatrix}3\\15\\18\end{bmatrix}$, which means the sum of residuals equals 0.

<average>69</average>

# END SOLUTION

# END SUBPROB

# END PROB