# BEGIN PROB

<i>Source: [Summer Session 2 2024 Midterm](../ss2-24-midterm/index.html), Problem 2a-b</i>

Prove the following statement or provide a counterexample: 

# BEGIN SUBPROB

If a vector $\vec{v}$ is orthogonal to a vector $\vec{w}$, then $\vec{v}$ is also orthogonal to the projection of an arbitrary vector $\vec{u}$ onto $\vec{w}$.

# BEGIN SOLUTION

The statement above is true.

Let the following information hold:

- $c$ is a scalar.
- $c\vec{w}$ is the projection of $\vec{u}$ onto $\vec{w}$.

When a vector is orthogonal to another their dot product will equal zero. This means $\vec{v} \cdot \vec{w} = 0$.

From lecture we know:
$$c\vec{w} = \frac{\vec{w} \cdot \vec{u}}{\vec{w} \cdot \vec{w}} \cdot \vec{w}$$

So, now we can solve $c\vec{w} \cdot \vec{v} = \frac{\vec{w} \cdot \vec{u} \cdot \vec{w} \cdot \vec{v}}{\vec{w} \cdot \vec{w}}$. The numerator becomes zero because $\vec{v} \cdot \vec{w} = 0$ and anything multiplied by zero will also be zero. This means the projection of $\vec{u}$ onto $\vec{w}$ is orthogonal to $\vec v$.

<average>52</average>

# END SOLUTION


# END SUBPROB


# BEGIN SUBPROB

If a vector $\vec{v}$ is orthogonal to a vector $\vec{w}$, then $\vec{v}$ is also orthogonal to the projection of $\vec{w}$ onto an arbitrary vector $\vec{u}$.

# BEGIN SOLUTION

The statement above is false.

Let the following hold:

- $\vec v = \begin{bmatrix} 1 \\ 2 \end{bmatrix}$
- $\vec w = \begin{bmatrix} -2 \\ 1 \end{bmatrix}$
- $\vec u = \begin{bmatrix} 0 \\ 1 \end{bmatrix}$

Let's check if $\vec w \cdot \vec v = 0$.
$$
(1)(-2)+(1)(2) = 0
$$
That works! Now we can calculate the projection of $\vec w$ onto $\vec u$.

\begin{align*}
\frac{\vec w \cdot \vec u}{\vec u \cdot \vec u}\vec u &= \frac{(-2)(0)+(1)(1)}{(0)(0)+(1)(1)} \cdot \begin{bmatrix} 0 \\ 1 \end{bmatrix}\\
&= -1 \cdot \begin{bmatrix} 0 \\ 1 \end{bmatrix}\\
&= \begin{bmatrix} 0 \\ -1 \end{bmatrix}
\end{align*}

Now we can check to see if $\vec v \cdot$ the projection of $\vec w$ onto $\vec u$ is equal to zero.

\begin{align*}
&\begin{bmatrix} 0 \\ -1 \end{bmatrix} \cdot \begin{bmatrix} 1 \\ 2 \end{bmatrix}\\
&= (0)(1) + (2)(-1) = -1\\
&\text{and } -1 \neq 0
\end{align*}

We can see that $\vec v \cdot$ the projection of $\vec w$ onto $\vec u$ is not equal to zero.


<average>50</average>

# END SOLUTION
    


# END SUBPROB


# END PROB