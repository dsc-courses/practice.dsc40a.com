# BEGIN PROB

**\[Eligible for midterm redemption\]**

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

Correctly explains that vectors are linearly independent for any $$\alpha \neq 1$$.

TODO

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

For what value(s) of $\alpha$ are $\vec{v}_1$ and $\vec{v}_3$
orthogonal? Show your work, and put your answer in a box.

# BEGIN SOLUTION

Correctly notes there are no values of $$\alpha$$ for which $$\vec{v}_1, \vec{v}_3$$ are orthogonal, as the first component containing $$\alpha$$ is multiplied by 0.

TODO

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

For what value(s) of $\alpha$ are $\vec{v}_2$ and $\vec{v}_3$
orthogonal? Show your work, and put your answer in a box.

# BEGIN SOLUTION

Correctly notes $$\alpha = -2$$ for this question, as this makes the dot product of $$\vec{v_1} \cdot \vec{v_3} = 0$$.

TODO

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

Correct: answered yes because any vector in $$\mathbb{R}^3$$ is in the span of 3 linearly independent vectors in $$\mathbb{R}^3$$.

TODO

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
vector. Show your work, and put your answer in a .

# BEGIN SOLUTION

Correctly projects $\begin{bmatrix}3 \\ 5 \\ 8\end{bmatrix}$ onto $$\vec{v_1}$$: $$\frac{\begin{bmatrix}3 \\ 5 \\ 8\end{bmatrix} \cdot \begin{bmatrix}0 \\ 1 \\ 1 \end{bmatrix}}{\begin{bmatrix}0 \\ 1 \\ 1 \end{bmatrix}\cdot \begin{bmatrix}0 \\ 1 \\ 1 \end{bmatrix}} \begin{bmatrix}0 \\ 1 \\ 1 \end{bmatrix} = \frac{13}{2}  \begin{bmatrix}0 \\ 1 \\ 1 \end{bmatrix} = \begin{bmatrix}0 \\ 6.5 \\ 6.5 \end{bmatrix}$$

TODO

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

Fully correct work using normal equations: $$(X^T X)^{-1}X^T \begin{bmatrix}3 \\ 15 \\ 18\end{bmatrix} = \begin{bmatrix}15 \\ 3 \end{bmatrix}$$.

TODO

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

Is it true that, for the orthogonal projection $\vec{p}$ from above, the
entries of\
$\vec{e} = \vec{p} \ - \begin{bmatrix} 3 \\ 15 \\ 18 \end{bmatrix}$ sum
to $0$? Explain why or why not. Your answer must mention characteristics
of $\vec{v}_1,\vec{v}_2,$ and/or $X$ to receive full credit.

( ) Yes
( ) No

Explain your answer

# BEGIN SOLUTION

Yes

Correctly explains that design matrix $$X$$ lacks a column of all 1s (and the span of its columns does not include all 1s), so residuals don't necessarily not sum to 0. Full credit also given for showing that $$\vec{p}$$ is exactly $$\begin{bmatrix}3\\15\\18\end{bmatrix}$$, so error vector $$\vec{e} = \vec{0}$$, or saying $$\begin{bmatrix}3\\15\\18\end{bmatrix} \in \text{span}(\vec{v_1}, \vec{v_2})$$ .

TODO

# END SOLUTION

# END SUBPROB

# END PROB